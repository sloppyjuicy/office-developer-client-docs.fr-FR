---
title: Multithreading et la Contention de mémoire dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- le multithreading dans excel, la contention de mémoire dans Excel, les fonctions [Excel 2007], thread-safe, thread-safe fonctions de mémoire de thread local [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: fb0eddfff2f34307143bb896fd451de357f2b639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782186"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading et la Contention de mémoire dans Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Versions de Microsoft Excel antérieures à Excel 2007 utilisent un seul thread pour tous les calculs de feuille de calcul. Toutefois, à compter d’Excel 2007, Excel peut être configuré pour utiliser à partir de 1 à des threads simultanés 1024 pour le calcul de la feuille de calcul. Sur un ordinateur multiprocesseur ou multicœur, le nombre de threads par défaut est égal au nombre de processeurs ou cœurs. Par conséquent, thread-safe cellules ou les cellules qui contiennent uniquement des fonctions qui sont thread-safe, pouvant être attribuées à des threads simultanés, soumis à la logique de recalcul habituels de devoir être calculée après leurs antécédents.
  
## <a name="thread-safe-functions"></a>Fonctions de thread-Safe

La plupart des fonctions de feuille de calcul intégré à compter d’Excel 2007 sont thread-safe. Vous pouvez également écrire et enregistrer les fonctions XLL comme étant thread-safe. Excel utilise un seul thread (son thread principal) pour appeler tous les commandes, fonctions non sécurisées, des fonctions **xlAuto** (sauf [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**) et COM et Visual Basic pour les fonctions d’Applications (VBA).
  
Où une fonction XLL retourne une **XLOPER** ou un **XLOPER12** **xlbitDLLFree** pourvue, Excel utilise le même thread sur lequel l’appel de fonction a été effectuée pour appeler **xlAutoFree** ou **xlAutoFree12**. L’appel à **xlAutoFree** ou **xlAutoFree12** est effectué avant le prochain appel de fonction sur ce thread. 
  
Pour les développeurs XLL, voici les avantages pour la création de fonctions de thread-safe :
  
- Ils permettent à Microsoft Excel pour que le plus d’un ordinateur multiprocesseur ou multicœur.
    
- Ils ouvriront la possibilité d’utiliser des serveurs distants beaucoup plus efficace peut être effectuée à l’aide d’un seul thread.
    
Supposons que vous disposez d’un ordinateur à processeur unique qui a été configuré pour utiliser, par exemple, les threads de *N* . Supposons qu’une feuille de calcul est en cours d’exécution que fait un grand nombre d’appels à une fonction XLL qui tour envoie une demande de données ou pour un calcul à réaliser à un serveur distant ou un cluster de serveurs. Soumis à la topologie de l’arborescence de dépendance, Excel peut appeler les heures de la fonction N presque simultanément. L’ou les serveurs sont suffisamment rapide ou en parallèle, à condition que la durée de recalcul de la feuille de calcul peut être réduite en autant qu’un facteur de 1/N. 
  
La question de l’écriture de fonctions de thread-safe gère correctement contention des ressources. Cela signifie généralement que la contention de mémoire, et il peut être divisé en deux problèmes :
  
- Comment créer la mémoire que vous connaissez est utilisé uniquement par ce thread.
    
- Comment s’assurer que mémoire partagée est accessible par plusieurs threads en toute sécurité.
    
La première chose à connaître est quelle mémoire dans une solution XLL est accessible par tous les threads, et ce qui est accessible uniquement par le thread en cours d’exécution.
  
 **Accessible par tous les threads**
  
- Instances de classe, les structures et les variables déclarées en dehors du corps d’une fonction.
    
- Variables statiques déclarées dans le corps d’une fonction.
    
Dans ces deux cas, la mémoire est attribuée dans un bloc de mémoire de la DLL créé pour cette instance de la DLL. Si une autre instance de l’application charge la DLL, il obtient sa propre copie de la mémoire afin qu’il n’existe pas de conflit avec ces ressources en dehors de cette instance de la DLL.
  
 **Accessible uniquement par le thread actuel**
  
- Variables automatiques dans le code de la fonction (y compris les arguments de la fonction).
    
Dans ce cas, mémoire définie à part sur la pile pour chaque instance de l’appel de fonction.
  
> [!NOTE]
> L’étendue de mémoire allouée dynamiquement dépend de l’étendue du pointeur qui pointe vers lui : si le pointeur est accessible par tous les threads, la mémoire est également. Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est efficacement privée ce thread. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Mémoire Accessible par un seul Thread : mémoire locale de Thread

Étant donné que les variables statiques dans le corps d’une fonction sont accessibles par tous les threads, les fonctions qui les utilisent sont clairement pas thread-safe. Une seule instance de la fonction sur un thread peut modifier la valeur pendant une autre instance sur un autre thread est en partant du principe qu’il est complètement différent. 
  
Il existe deux raisons pour déclarer des variables statiques au sein d’une fonction :
  
1. Conserver des données statiques à partir d’un appel à la suivante.
    
2. Un pointeur vers les données statiques en toute sécurité peut être renvoyé par la fonction.
    
Dans le cas de première raison, vous voudrez peut-être des données qui est conservée et a de signification pour tous les appels à la fonction : par exemple un compteur simple qui est incrémenté à chaque fois que la fonction est appelée sur n’importe quel thread, ou une structure qui collecte les données d’utilisation et performances veille appel Ry. La question est comment protéger les données partagées ou la structure de données. Mieux, cela s’effectue à l’aide de section critique comme l’explique la section suivante.
  
Si les données sont destinées uniquement à ce thread, qui peut être le cas pour la raison 1 et est toujours le cas pour la raison 2, la question est la création de mémoire qui persiste, mais n’est pas accessible à partir de ce thread. Une solution consiste à utiliser le stockage local des threads (TLS) API.
  
Par exemple, imaginons une fonction qui retourne un pointeur vers un **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Cette fonction n’est pas thread-safe car un thread peut renvoyer l' statique **XLOPER12** tandis que l’autre est le remplacement. La probabilité de ce problème est accrue si le **XLOPER12** doit être transmis à **xlAutoFree12**. Une solution consiste à allouer un **XLOPER12**, retourner un pointeur et implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même est libérée. Cette approche est utilisée dans la plupart des fonctions exemple indiquées dans la [Gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
```cs
LPXLOPER12 WINAPI mtr_safe_example_1(LPXLOPER12 pxArg)
{
// pxRetVal must be freed later by xlAutoFree12
    LPXLOPER12 pxRetVal = new XLOPER12;
// code sets pxRetVal to a function of pxArg ...
    pxRetVal->xltype |= xlbitDLLFree; // Needed for all types
    return pxRetVal; // xlAutoFree12 must free this
}
```

Cette approche est plus simple à implémenter que celle décrite dans la section suivante, qui repose sur l’API TLS, mais elle présente des inconvénients. Tout d’abord, Excel doit appeler **xlAutoFree**/ **xlAutoFree12** quel que soit le type de l' renvoyée **XLOPER**/ **XLOPER12**. Deuxièmement, un problème est survenu lors de la réponse **XLOPER**/ s**XLOPER12**qui correspondent à la valeur de retour d’un appel à une fonction de rappel API C. Le **XLOPER**/ **XLOPER12** peuvent pointer vers la mémoire doit être libérée par Excel, mais le **XLOPER**/ **XLOPER12** lui-même doit être libérée de la même manière qu’il a été attribué. Si ces un **XLOPER**/ **XLOPER12** doit être utilisée comme valeur de retour d’une fonction de feuille de calcul XLL, il n’existe aucun moyen simple d’informer **xlAutoFree**/ **xlAutoFree12** de la nécessité de libérer les deux pointeurs de manière appropriée. (Définition **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, comme le traitement de **XLOPER/XLOPER12s** dans Excel avec la valeur n’est pas défini et peut changer d’une version à l’autre.) Pour contourner ce problème, la ressource XLL permettre rendre des copies complètes de tous les allouée Excel **XLOPER/XLOPER12s** qu’elle renvoie à la feuille de calcul. 
  
Pour éviter ces limitations consiste à remplir et renvoyer un thread **local/XLOPER12 XLOPER**, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne la libère pas le pointeur **XLOPER/XLOPER12** lui-même. 
  
```cs
LPXLOPER12 get_thread_local_xloper12(void);
LPXLOPER12 WINAPI mtr_safe_example_2(LPXLOPER12 pxArg)
{
    LPXLOPER12 pxRetVal = get_thread_local_xloper12();
// Code sets pxRetVal to a function of pxArg setting xlbitDLLFree or
// xlbitXLFree as required.
    return pxRetVal; // xlAutoFree12 must not free this pointer!
}

```

La question suivante est comment configurer et récupérer la mémoire locale de thread, en d’autres termes, comment implémenter la fonction **get_thread_local_xloper12** dans l’exemple précédent. Cette opération est effectuée à l’aide du stockage TLS (Thread Local) API. La première étape consiste à obtenir un index TLS à l’aide de **TlsAlloc**, qui doit être libéré à l’aide de **TlsFree**. Les deux sont effectuées depuis **DllMain**.
  
```cs
// This implementation just calls a function to set up
// thread-local storage.
BOOL TLS_Action(DWORD Reason); // Could be in another module
BOOL WINAPI DllMain(HINSTANCE hDll, DWORD Reason, void *Reserved)
{
    return TLS_Action(Reason);
}
DWORD TlsIndex; // Module scope only if all TLS access in this module
BOOL TLS_Action(DWORD DllMainCallReason)
{
    switch (DllMainCallReason)
    {
    case DLL_PROCESS_ATTACH: // The DLL is being loaded.
        if((TlsIndex = TlsAlloc()) == TLS_OUT_OF_INDEXES)
            return FALSE;
        break;
    case DLL_PROCESS_DETACH: // The DLL is being unloaded.
        TlsFree(TlsIndex); // Release the TLS index.
        break;
    }
    return TRUE;
}
```

Après avoir obtenu l’index, l’étape suivante consiste à allouer un bloc de mémoire pour chaque thread. La [Documentation de développement Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) recommande cette opération chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et libérer la mémoire sur chaque **DLL_THREAD_DETACH**. Toutefois, ce Conseil serait entraîner votre DLL faire inutiles pour les threads non utilisé pour le recalcul. 
  
Au lieu de cela, il est préférable d’utiliser une stratégie d’affecter à la première utilisation. Tout d’abord, vous devez définir une structure que vous souhaitez allouer pour chaque thread. Pour les exemples précédents qui renvoient **XLOPER** ou **XLOPER12s**, suffit suivantes, mais vous pouvez créer une structure répondant à vos besoins.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La fonction suivante obtient un pointeur vers l’instance locale de thread ou en alloue un s’il s’agit du premier appel.
  
```cs
TLS_data *get_TLS_data(void)
{
// Get a pointer to this thread's static memory.
    void *pTLS = TlsGetValue(TlsIndex);
    if(!pTLS) // No TLS memory for this thread yet
    {
        if((pTLS = calloc(1, sizeof(TLS_data))) == NULL)
        // Display some error message (omitted).
            return NULL;
        TlsSetValue(TlsIndex, pTLS); // Associate with this thread
    }
    return (TLS_data *)pTLS;
}
```

Vous pouvez maintenant voir comment la mémoire **XLOPER/XLOPER12** locale de thread est obtenue : tout d’abord, vous obtenez un pointeur vers l’instance du thread de **TLS_data**, puis vous renvoyez un pointeur vers le **XLOPER/XLOPER12** contenues dans celui-ci, comme suit. 
  
```cs
LPXLOPER get_thread_local_xloper(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper_shared_ret_val);
    return NULL;
}
LPXLOPER12 get_thread_local_xloper12(void)
{
    TLS_data *pTLS = get_TLS_data();
    if(pTLS)
        return &(pTLS->xloper12_shared_ret_val);
    return NULL;
}

```

Les fonctions **mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que les fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel. Toutefois, vous ne pouvez pas mélanger les deux approches dans un XLL. Votre XLL permettre exporter uniquement une implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire requiert une approche différente. Avec **mtr_safe_example_1**, le pointeur passé à **xlAutoFree/xlAutoFree12** doit être libéré avec toutes les données qu’il pointe vers. Avec **mtr_safe_example_2**, uniquement les données désigné doivent être libérées.
  
Windows fournit également une fonction **GetCurrentThreadId**, qui retourne l’ID unique au niveau du système. du thread courant Ainsi, le développeur avec une autre façon de sécuriser le thread de code, ou de passer son thread de comportement spécifique.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Mémoire Accessible uniquement par plusieurs threads : Sections critiques

Vous devez protéger la mémoire en lecture-écriture qui est accessible par plusieurs threads utilisant des sections critiques. Vous avez besoin d’une section critique nommé pour chaque bloc de mémoire que vous souhaitez protéger. Vous pouvez initialiser pendant l’appel à la fonction **xlAutoOpen** et les libérer et leur attribuer la valeur null pendant l’appel à la fonction **xlAutoClose** . Vous devez ensuite contenir chaque accès au bloc protégé au sein d’une paire d’appels à **EnterCriticalSection** et **LeaveCriticalSection**. Un seul thread est autorisé dans la section critique à tout moment. Voici un exemple de l’initialisation, désinitialisation et l’utilisation d’une section appelée **g_csSharedTable**.
  
```cs
CRITICAL_SECTION g_csSharedTable; // global scope (if required)
bool xll_initialised = false; // Only module scope needed
int WINAPI xlAutoOpen(void)
{
    if(xll_initialised)
        return 1;
// Other initialisation omitted
    InitializeCriticalSection(&g_csSharedTable);
    xll_initialised = true;
    return 1;
}
int WINAPI xlAutoClose(void)
{
    if(!xll_initialised)
        return 1;
// Other cleaning up omitted.
    DeleteCriticalSection(&g_csSharedTable);
    xll_initialised = false;
    return 1;
}
#define SHARED_TABLE_SIZE 1000 /* Some value consistent with the table */
bool read_shared_table_element(unsigned int index, double &d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    d = shared_table[index];
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
bool set_shared_table_element(unsigned int index, double d)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTable);
    shared_table[index] = d;
    LeaveCriticalSection(&g_csSharedTable);
    return true;
}
```

Une autre, peut-être plus sûr de protéger un bloc de mémoire consiste à créer une classe qui contient sa propre **CRITICAL_SECTION** et dont constructeur, destructeur et prendre en charge les méthodes d’accesseurs de son utilisation. Cette approche présente l’avantage de protéger les objets qui peuvent être initialisées avant **xlAutoOpen** est exécutée ou survivre après avoir appelé **xlAutoClose** , mais vous devez être attentif à la création de sections critiques trop et le système d’exploitation surcharge à créer. 
  
Lorsque vous avez du code qui doit accéder à plusieurs blocs de mémoire protégés en même temps, vous devez prendre en compte soigneusement l’ordre dans lequel les sections critiques sont entrées et s’est arrêtées. Par exemple, les deux fonctions suivantes peuvent créer un blocage.
  
```cs
// WARNING: Do not copy this code. These two functions
// can produce a deadlock and are provided for
// example and illustration only.
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = shared_table_A[index];
// Critical sections should be exited in the order
// they were entered, NOT as shown here in this
// deliberately wrong illustration.
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
bool copy_shared_table_element_B_to_A(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableB);
    EnterCriticalSection(&g_csSharedTableA);
    shared_table_A[index] = shared_table_B[index];
    LeaveCriticalSection(&g_csSharedTableA);
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Si la première fonction sur un thread entre **g_csSharedTableA** alors que la seconde sur un autre thread passe **g_csSharedTableB**, les deux threads se bloquent. L’approche correcte consiste à entrer dans un ordre cohérent et quitter dans l’ordre inverse, comme suit.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Si possible, il est préférable d’un thread coopération point de vue pour isoler l’accès aux blocs distincts, comme indiqué ici.
  
```cs
bool copy_shared_table_element_A_to_B(unsigned int index)
{
    if(index >= SHARED_TABLE_SIZE) return false;
    EnterCriticalSection(&g_csSharedTableA);
    double d = shared_table_A[index];
    LeaveCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    shared_table_B[index] = d;
    LeaveCriticalSection(&g_csSharedTableB);
    return true;
}
```

Où il y a beaucoup de contention pour une ressource partagée, telles que les demandes d’accès de courte durée fréquents, vous devez envisager à l’aide de la section critique pour faire pivoter. Il s’agit d’une technique qui rend en attente de la ressource moins utilisation intensive du processeur. Pour ce faire, vous pouvez utiliser soit **InitializeCriticalSectionAndSpinCount** lors de l’initialisation de la section ou le **SetCriticalSectionSpinCount** une fois initialisée, pour définir le nombre de fois que le thread effectue une boucle avant d’attendre de ressources Il est disponible. L’opération d’attente étant onéreuse, rotation permet de l’éviter si la ressource est libérée entre-temps. Sur un système à processeur unique, le nombre de rotations est ignoré, mais vous pouvez toujours le spécifier sans nuire à toute l’entreprise. Le Gestionnaire de segments de mémoire utilise un compteur de rotations de 4000. Pour plus d’informations sur l’utilisation de sections critiques, voir la documentation du SDK de Windows. 
  
## <a name="see-also"></a>Voir aussi



[Gestion de la m�moire dans Excel](memory-management-in-excel.md)
  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Gestionnaire de compléments et les fonctions de l’Interface XLL](add-in-manager-and-xll-interface-functions.md)

