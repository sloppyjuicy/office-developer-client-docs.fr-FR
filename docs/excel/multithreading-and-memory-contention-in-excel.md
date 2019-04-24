---
title: Multithreading et contention de la mémoire dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading dans Excel, contention de mémoire dans Excel, fonctions [Excel 2007], thread-safe, fonctions thread-safe [Excel 2007], mémoire locale de thread [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301637"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading et contention de la mémoire dans Excel

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Les versions de Microsoft Excel antérieures à Excel 2007 utilisent un seul thread pour tous les calculs de feuille de calcul. Toutefois, en commençant dans Excel 2007, Excel peut être configuré pour utiliser de 1 à 1024 threads simultanés pour le calcul de la feuille de calcul. Sur un ordinateur multiprocesseur ou multicœur, le nombre de threads par défaut est égal au nombre de processeurs ou cœurs. Par conséquent, les cellules thread-safe, ou les cellules qui contiennent uniquement des fonctions thread-safe, peuvent être attribuées à des threads simultanés, sous réserve de la logique de Recalculation habituelle de la nécessité de les calculer après leurs antécédents.
  
## <a name="thread-safe-functions"></a>Fonctions thread-safe

La plupart des fonctions de feuille de calcul intégrées commençant dans Excel 2007 sont thread-safe. Vous pouvez également écrire et enregistrer des fonctions XLL comme thread-safe. Excel utilise un thread (son thread principal) pour appeler toutes les commandes, les fonctions non sécurisées de thread, les fonctions **xlAuto** (à l'exception de [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**), ainsi que les fonctions com et Visual Basic pour applications (VBA).
  
Lorsqu'une fonction XLL renvoie un élément **XLOPER** ou **XLOPER12** avec **xlbitDLLFree** , Excel utilise le même thread que celui sur lequel l'appel de la fonction a été effectué pour appeler **xlAutoFree** ou **xlAutoFree12**. L'appel à **xlAutoFree** ou **xlAutoFree12** est effectué avant l'appel de fonction suivant sur ce thread. 
  
Pour les développeurs XLL, il existe des avantages pour la création de fonctions thread-safe:
  
- Elles permettent à Excel de tirer le meilleur parti d'un ordinateur multiprocesseur ou multicœur.
    
- Ils ouvrent la possibilité d'utiliser des serveurs distants de manière bien plus efficace qu'ils ne peuvent le faire à l'aide d'un seul thread.
    
Supposons que vous disposez d'un ordinateur à un seul processeur configuré pour utiliser, disons, *N* threads. Supposons qu'une feuille de calcul est en cours d'exécution et qu'elle effectue un grand nombre d'appels à une fonction XLL qui envoie à son tour une demande de données ou un calcul à effectuer sur un serveur ou un cluster de serveurs distant. Sous réserve de la topologie de l'arborescence des dépendances, Excel peut appeler la fonction N fois presque simultanément. Étant donné que le ou les serveurs sont suffisamment rapides ou parallèles, le temps de recalcul de la feuille de calcul peut être réduit de 1/N. 
  
Le problème clé lors de l'écriture de fonctions thread-safe consiste à gérer correctement la contention des ressources. Cela signifie généralement une contention de mémoire et peut être divisée en deux problèmes:
  
- La façon de créer de la mémoire qui sera utilisée uniquement par ce thread.
    
- Comment s'assurer que plusieurs threads accèdent à la mémoire partagée en toute sécurité.
    
La première chose à savoir est que la mémoire d'une XLL est accessible par tous les threads et ce qui est uniquement accessible par le thread en cours d'exécution.
  
 **Accessible par tous les threads**
  
- Variables, structures et instances de classe déclarées à l'extérieur du corps d'une fonction.
    
- Variables statiques déclarées dans le corps d'une fonction.
    
Dans ces deux cas, la mémoire est réservée dans le bloc de mémoire de la DLL créé pour cette instance de la DLL. Si une autre instance d'application charge la DLL, elle obtient sa propre copie de cette mémoire de sorte qu'il n'existe aucun conflit pour ces ressources provenant de l'extérieur de cette instance de la DLL.
  
 **Accessible uniquement par le thread actuel**
  
- Variables automatiques dans le code de fonction (y compris les arguments de fonction).
    
Dans ce cas, la mémoire est réservée sur la pile pour chaque instance de l'appel de fonction.
  
> [!NOTE]
> L'étendue de la mémoire allouée dynamiquement dépend de la portée du pointeur qui pointe vers elle: si le pointeur est accessible par tous les threads, la mémoire est également. Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est réellement propre à ce thread. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Mémoire accessible par un seul thread: mémoire locale de thread

Étant donné que les variables statiques dans le corps d'une fonction sont accessibles par tous les threads, les fonctions qui les utilisent ne sont manifestement pas thread-safe. Une instance de la fonction sur un thread peut modifier la valeur tandis qu'une autre instance sur un autre thread suppose qu'elle est complètement différente. 
  
Il existe deux raisons pour déclarer des variables statiques au sein d'une fonction:
  
1. Les données statiques sont conservées d'un appel à l'autre.
    
2. Un pointeur vers des données statiques peut être retourné en toute sécurité par la fonction.
    
Dans le cas d'une première raison, vous pouvez souhaiter avoir des données qui persistent et ont une signification pour tous les appels à la fonction: un simple compteur qui est peut-être incrémenté chaque fois que la fonction est appelée sur un thread ou une structure qui collecte les données d'utilisation et de performances en veille. appel Ry. La question est de savoir comment protéger les données partagées ou la structure des données. Pour ce faire, vous devez utiliser la section critique, comme décrit dans la section suivante.
  
Si les données sont destinées uniquement à être utilisées par ce thread, ce qui peut être le cas pour la raison 1 et est toujours le cas pour la raison 2, la question est la façon de créer de la mémoire qui persiste, mais qui n'est accessible qu'à partir de ce thread. Une solution consiste à utiliser l'API de stockage local de thread (TLS).
  
Prenons l'exemple d'une fonction qui renvoie un pointeur vers un **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Cette fonction n'est pas thread-safe, car un thread peut renvoyer le **XLOPER12** statique, tandis qu'un autre peut le remplacer. La probabilité que cela se produise est encore plus importante si la version de **XLOPER12** doit être passée à **xlAutoFree12**. Une solution consiste à allouer un **XLOPER12**, renvoyer un pointeur vers celui-ci et implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même soit libérée. Cette approche est utilisée dans de nombreux exemples de fonctions illustrés dans la [gestion de la mémoire dans Excel](memory-management-in-excel.md).
  
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

Cette approche est plus simple à mettre en œuvre que l'approche décrite dans la section suivante, qui repose sur l'API TLS, mais présente quelques inconvénients. Tout d'abord, Excel doit appeler **xlAutoFree**/ **xlAutoFree12** quel que soit le type de l' **XLOPER**/ **XLOPER12**. Deuxièmement, il y a un problème lors du renvoi des savesets **XLOPER**/ **** de la valeur de retour d'un appel à une fonction de rappel de l'API C. La demande **XLOPER**/ **** peut pointer vers la mémoire qui doit être libérée par Excel, mais la méthode **XLOPER**/ **** propre elle-même doit être libérée de la même façon qu'elle. Si une telle **expression XLOPER**/ **** doit être utilisée comme valeur de retour d'une fonction de feuille de calcul XLL, il n'existe pas de moyen simple d'informer **xlAutoFree**/ **xlAutoFree12** de la nécessité de libérer les deux pointeurs de manière appropriée. (Le fait de définir à la fois **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, car le traitement de **XLOPER/XLOPER12** dans Excel avec les deux ensembles n'est pas défini et peut passer de la version à la version.) Pour contourner ce problème, le XLL peut effectuer des copies complètes de tous les **XLOPER/XLOPER12** alloués par Excel qu'il renvoie à la feuille de calcul. 
  
Une solution qui évite ces limitations est de remplir et de renvoyer une structure **XLOPER/XLOPER12**locale de thread, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne libère pas le pointeur **XLOPER/XLOPER12** lui-même. 
  
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

La question suivante concerne la configuration et la récupération de la mémoire locale de thread, en d'autres termes, comment implémenter la fonction **get_thread_local_xloper12** dans l'exemple précédent. Cette opération est réalisée à l'aide de l'API de stockage local des threads (TLS). La première étape consiste à obtenir un index TLS à l'aide de **TlsAlloc**, qui doit finalement être publié à l'aide de **TlsFree**. Les deux sont les mieux effectués à partir de **DllMain**.
  
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

Une fois l'index obtenu, l'étape suivante consiste à allouer un bloc de mémoire pour chaque thread. La [documentation de développement Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommande d'effectuer cette opération chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et de libérer de la mémoire sur chaque **DLL_THREAD_DETACH**. Toutefois, à la suite de ce Conseil, votre DLL n'effectuera pas de travail inutile pour les threads qui n'ont pas été utilisés pour le recalcul. 
  
Au lieu de cela, il est préférable d'utiliser une stratégie d'allocation à la première utilisation. Tout d'abord, vous devez définir une structure que vous souhaitez allouer à chaque thread. Pour les exemples précédents qui renvoient **XLOPER** ou **XLOPER12**, les éléments suivants suffisent, mais vous pouvez créer une structure qui répond à vos besoins.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La fonction suivante obtient un pointeur vers l'instance locale de thread ou alloue une s'il s'agit du premier appel.
  
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

À présent, vous pouvez voir comment la mémoire locale **XLOPER/XLOPER12** est obtenue: tout d'abord, vous obtenez un pointeur vers l'instance de la thread de **TLS_data**, puis vous renvoyez un pointeur vers l'élément **XLOPER/XLOPER12** qu'elle contient, comme suit. 
  
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

Les fonctions **mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel. Toutefois, vous ne pouvez pas mélanger les deux approches dans une XLL. Votre XLL ne peut exporter qu'une seule implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire requiert une approche différente. Avec **mtr_safe_example_1**, le pointeur transmis à **xlAutoFree/xlAutoFree12** doit être libéré en même temps que les données vers lesquelles il pointe. Avec **mtr_safe_example_2**, seules les données ciblées doivent être libérées.
  
Windows fournit également une fonction **GetCurrentThreadID**, qui renvoie l'ID système unique du thread actuel. Cela permet au développeur d'utiliser une autre méthode pour mettre en danger les threads de code ou de définir son comportement de thread propre.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Mémoire accessible uniquement par plus d'un thread: sections critiques

Vous devez protéger la mémoire en lecture/écriture accessible par plusieurs threads à l'aide de sections critiques. Vous avez besoin d'une section critique nommée pour chaque bloc de mémoire que vous souhaitez protéger. Vous pouvez les initialiser pendant l'appel à la fonction **xlAutoOpen** , puis les publier et les définir sur null pendant l'appel de la fonction **xlAutoClose** . Vous devez ensuite contenir chaque accès au bloc protégé dans une paire d'appels vers **EnterCriticalSection** et **LeaveCriticalSection**. Un seul thread est autorisé à la section critique à tout moment. Voici un exemple de l'initialisation, de l'échec d'initialisation et de l'utilisation d'une section appelée **g_csSharedTable**.
  
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

Un autre moyen plus sûr de protéger un bloc de mémoire consiste à créer une classe qui contient son propre **critical_section** et dont les méthodes de constructeur, de destructeur et d'accesseur prennent en charge leur utilisation. Cette approche présente l'avantage supplémentaire de protéger les objets qui peuvent être initialisés avant l'exécution d' **xlAutoOpen** ou survivent après l'appel de **xlAutoClose** , mais vous devez être attentif à la création d'un trop grand nombre de sections critiques et du système d'exploitation charge de travail créée. 
  
Lorsque vous avez du code qui a besoin d'accéder à plusieurs blocs de mémoire protégée en même temps, vous devez tenir compte de l'ordre dans lequel les sections critiques sont entrées et sorties. Par exemple, les deux fonctions suivantes peuvent créer un blocage.
  
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

Si la première fonction sur un thread entre **g_csSharedTableA** tandis que la seconde sur un autre, entre **g_csSharedTableB**, les deux threads se bloquent. L'approche correcte consiste à entrer un ordre cohérent et à quitter l'ordre inverse, comme suit.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Dans la mesure du possible, il est préférable d'avoir un point de vue de la co-opération de thread pour isoler l'accès à des blocs distincts, comme illustré ici.
  
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

Lorsqu'il existe beaucoup de contention pour une ressource partagée, telle que des demandes d'accès de courte durée fréquentes, vous devez envisager d'utiliser la fonctionnalité de la section critique pour faire tourner. Il s'agit d'une technique qui rend l'attente de ressources moins gourmandes en processeur. Pour ce faire, vous pouvez utiliser l'un ou l'autre **InitializeCriticalSectionAndSpinCount** lors de l'initialisation de la section ou de **SetCriticalSectionSpinCount** une fois initialisé, afin de définir le nombre de boucles du thread avant d'attendre que les ressources deviennent possibles. L'opération d'attente est coûteuse, ce qui évite cela si la ressource est libérée entre temps. Sur un système à processeur unique, le nombre de spins est effectivement ignoré, mais vous pouvez toujours le spécifier sans nuire. Le gestionnaire de tas de mémoire utilise un nombre de spins de 4000. Pour plus d'informations sur l'utilisation des sections critiques, reportez-vous à la documentation du kit de développement logiciel Windows. 
  
## <a name="see-also"></a>Voir aussi



[Gestion de la m�moire dans Excel](memory-management-in-excel.md)
  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

