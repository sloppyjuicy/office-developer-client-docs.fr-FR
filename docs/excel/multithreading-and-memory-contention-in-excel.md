---
title: Multithreading et contention de mémoire dans Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- multithreading in excel,memory contention in Excel,functions [Excel 2007], thread-safe,thread-safe functions [Excel 2007],thread-local memory [Excel 2007]
localization_priority: Normal
ms.assetid: 86e1e842-f433-4ea9-8b13-ad2515fc50d8
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a385728450fc6519d7f5211c186a9d74e623bf7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301637"
---
# <a name="multithreading-and-memory-contention-in-excel"></a>Multithreading et contention de mémoire dans Excel

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Les versions de Microsoft Excel antérieures à Excel 2007 utilisent un thread unique pour tous les calculs de feuille de calcul. Toutefois, à partir d’Excel 2007, Excel peut être configuré pour utiliser entre 1 et 1 024 threads simultanés pour le calcul de feuille de calcul. Sur un ordinateur multi-processeur ou multi cœur, le nombre de threads par défaut est égal au nombre de processeurs ou de cœurs. Par conséquent, les cellules thread-safe, ou les cellules qui contiennent uniquement des fonctions thread-safe, peuvent être allouées à des threads simultanés, sous réserve de la logique de recalcul habituelle de la nécessité d’être calculées après leurs antécédents.
  
## <a name="thread-safe-functions"></a>Thread-Safe fonctions

La plupart des fonctions de feuille de calcul intégrées à partir d’Excel 2007 sont thread-safe. Vous pouvez également écrire et inscrire des fonctions XLL comme étant thread-safe. Excel utilise un thread (son thread principal) pour appeler toutes les commandes, fonctions non thread-unsafe, **fonctions xlAuto** (à l’exception des fonctions [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**), et COM et Visual Basic pour Applications (VBA).
  
Lorsqu’une fonction XLL renvoie une **xlOPER** ou **XLOPER12** avec un ensemble **xlbitDLLFree,** Excel utilise le même thread sur lequel l’appel de fonction a été effectué pour appeler **xlAutoFree** ou **xlAutoFree12**. L’appel **à xlAutoFree** ou **xlAutoFree12** est effectué avant l’appel de fonction suivant sur ce thread. 
  
Pour les développeurs XLL, il existe des avantages à créer des fonctions thread-safe :
  
- Elles permettent à Excel d’utiliser un ordinateur multi-processeur ou multi cœur.
    
- Ils ouvrent la possibilité d’utiliser des serveurs distants beaucoup plus efficacement qu’avec un thread unique.
    
Supposons que vous disposez d’un ordinateur à processeur unique configuré pour utiliser, par exemple, *des threads N.* Supposons qu’une feuille de calcul soit en cours d’exécution et qu’elle effectue un grand nombre d’appels à une fonction XLL qui à son tour envoie une demande de données ou un calcul à effectuer sur un serveur distant ou un cluster de serveurs. Sous réserve de la topologie de l’arborescence des dépendances, Excel peut appeler la fonction N fois presque simultanément. À condition que le ou les serveurs soient suffisamment rapides ou parallèles, le temps de recalcul de la feuille de calcul peut être réduit de 1/N. 
  
Le problème clé dans l’écriture de fonctions thread-safe consiste à gérer correctement les conflits de ressources. Cela signifie généralement une contention de mémoire et elle peut être décomposée en deux problèmes :
  
- La façon de créer de la mémoire que vous savez sera utilisée uniquement par ce thread.
    
- Comment s’assurer que la mémoire partagée est accessible par plusieurs threads en toute sécurité.
    
La première chose à savoir est la mémoire dans un XLL qui est accessible par tous les threads et ce qui est accessible uniquement par le thread en cours d’exécution.
  
 **Accessible par tous les threads**
  
- Variables, structures et instances de classe déclarées en dehors du corps d’une fonction.
    
- Variables statiques déclarées dans le corps d’une fonction.
    
Dans ces deux cas, la mémoire est mise de côté dans le bloc de mémoire de la DLL créé pour cette instance de la DLL. Si une autre instance d’application charge la DLL, elle obtient sa propre copie de cette mémoire afin qu’il n’y a aucun conflit pour ces ressources en dehors de cette instance de la DLL.
  
 **Accessible uniquement par le thread actuel**
  
- Variables automatiques dans le code de fonction (y compris les arguments de fonction).
    
Dans ce cas, la mémoire est mise de côté sur la pile pour chaque instance de l’appel de fonction.
  
> [!NOTE]
> L’étendue de la mémoire allouée dynamiquement dépend de l’étendue du pointeur qui pointe vers celle-ci : si le pointeur est accessible par tous les threads, la mémoire l’est également. Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est en fait privée à ce thread. 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a>Mémoire accessible par un seul thread : Thread-Local mémoire

Étant donné que les variables statiques dans le corps d’une fonction sont accessibles par tous les threads, les fonctions qui les utilisent ne sont clairement pas thread-safe. Une instance de la fonction sur un thread peut être en train de modifier la valeur, tandis qu’une autre instance sur un autre thread suppose qu’il s’agit d’un sujet complètement différent. 
  
Il existe deux raisons de déclarer des variables statiques au sein d’une fonction :
  
1. Les données statiques persistent d’un appel à l’autre.
    
2. Un pointeur vers des données statiques peut être renvoyé en toute sécurité par la fonction.
    
Dans le cas de la première raison, vous pouvez avoir des données qui persistent et ont une signification pour tous les appels à la fonction : peut-être un compteur simple qui est incrémenté chaque fois que la fonction est appelée sur n’importe quel thread, ou une structure qui collecte les données d’utilisation et de performances sur chaque appel. La question est de savoir comment protéger la structure des données ou des données partagées. Pour ce faire, il est préférable d’utiliser la section critique comme l’explique la section suivante.
  
Si les données sont destinées uniquement à être utilisés par ce thread, ce qui peut être le cas pour la raison 1 et toujours pour la raison 2, la question est de savoir comment créer une mémoire qui persiste mais qui est accessible uniquement à partir de ce thread. Une solution consiste à utiliser l’API de stockage local de thread (TLS).
  
Par exemple, considérez une fonction qui renvoie un pointeur vers une **XLOPER**.
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

Cette fonction n’est pas thread-safe, car un thread peut renvoyer la **XLOPER12** statique, tandis qu’un autre la sur-réécrit. La probabilité que cela se produise est encore plus élevée si **la xlOPER12** doit être passée à **xlAutoFree12**. Une solution consiste à allouer un **XLOPER12,** à renvoyer un pointeur vers celui-ci et à implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même soit libérée. Cette approche est utilisée dans la plupart des exemples de fonctions présentés dans la gestion de [la mémoire dans Excel.](memory-management-in-excel.md)
  
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

Cette approche est plus simple à implémenter que l’approche décrite dans la section suivante, qui repose sur l’API TLS, mais présente certains inconvénients. Tout d’abord, Excel doit appeler **xlAutoFree** /  **xlAutoFree12** quel que soit le type de **xlOPER** /  **XLOPER12 renvoyé.** Deuxièmement, il existe un problème lors du renvoi de **XLOPER** /  **XLOPER12** qui sont la valeur de retour d’un appel à une fonction de rappel d’API C. La **xlOPER** XLOPER12 peut pointer vers la mémoire qui doit être libérée par Excel, mais la /   **XLOPER** /  **XLOPER12** elle-même doit être libérée de la même façon qu’elle a été allouée. Si une **xlOPER** XLOPER12 de ce type doit être utilisée comme valeur de retour d’une fonction de feuille de calcul XLL, il n’existe aucun moyen simple d’informer /   **xlAutoFree** /  **xlAutoFree12** de la nécessité de libérer les deux pointeurs de la manière appropriée. (La définition de **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, car le traitement de **XLOPER/XLOPER12s** dans Excel avec les deux ensembles n’est pas définie et peut changer de version.) Pour contourner ce problème, le XLL peut effectuer des copies détaillées de toutes les **XLOPER/XLOPER12 allouées** par Excel qu’elle renvoie à la feuille de calcul. 
  
Une solution qui évite ces limitations consiste à remplir et renvoyer une **XLOPER/XLOPER12** locale de thread, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne libère pas le pointeur **XLOPER/XLOPER12** lui-même. 
  
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

La question suivante est de savoir comment configurer et récupérer la mémoire locale de thread, en d’autres termes, comment implémenter la fonction get_thread_local_xloper12 **dans** l’exemple précédent. Pour ce faire, utilisez l’API de stockage local de thread (TLS). La première étape consiste à obtenir un index TLS à l’aide de **TlsAlloc**, qui doit finalement être publié à l’aide de **TlsFree**. Les deux sont mieux accomplies à partir **de DllMain**.
  
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

Une fois l’index obtenu, l’étape suivante consiste à allouer un bloc de mémoire pour chaque thread. La [documentation de développement Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) vous recommande de le faire chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et libérant la mémoire sur chaque **DLL_THREAD_DETACH**. Toutefois, le fait de suivre ces conseils entraînerait le travail inutile de votre DLL pour les threads qui ne sont pas utilisés pour le recalcul. 
  
Au lieu de cela, il est préférable d’utiliser une stratégie d’allocation à la première utilisation. Tout d’abord, vous devez définir une structure que vous souhaitez allouer pour chaque thread. Pour les exemples précédents qui retournent **xlOPERs** ou **XLOPER12s,** voici ce qui suffit, mais vous pouvez créer n’importe quelle structure qui répond à vos besoins.
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

La fonction suivante obtient un pointeur vers l’instance thread-local, ou en alloue un s’il s’agit du premier appel.
  
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

Vous pouvez maintenant voir comment la mémoire **XLOPER/XLOPER12** locale du thread est obtenue : tout d’abord, vous obtenez un pointeur vers l’instance **de TLS_data** du thread, puis vous renvoyez un pointeur vers la **XLOPER/XLOPER12** qu’elle contient, comme suit. 
  
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

Les **fonctions mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel. Toutefois, vous ne pouvez pas combiner les deux approches dans une seule XLL. Votre XLL ne peut exporter qu’une seule implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire nécessite une approche différente. Avec **mtr_safe_example_1,** le pointeur transmis à **xlAutoFree/xlAutoFree12** doit être libéré avec toutes les données vers qui il pointe. Avec **mtr_safe_example_2**, seules les données pointées doivent être libérées.
  
Windows fournit également une **fonction GetCurrentThreadId**, qui renvoie l’ID unique à l’échelle du système du thread actuel. Cela permet au développeur de rendre le thread de code sécurisé ou de rendre son thread de comportement spécifique.
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a>Mémoire accessible uniquement par plusieurs threads : sections critiques

Vous devez protéger la mémoire en lecture/écriture accessible par plusieurs threads à l’aide de sections critiques. Vous avez besoin d’une section critique nommée pour chaque bloc de mémoire que vous souhaitez protéger. Vous pouvez initialiser ces derniers pendant l’appel à la fonction **xlAutoOpen,** les libérer et les définir sur null lors de l’appel à la fonction **xlAutoClose.** Vous devez ensuite contenir chaque accès au bloc protégé dans une paire d’appels à **EnterCriticalSection** et **LeaveCriticalSection**. Un seul thread est autorisé dans la section critique à tout moment. Voici un exemple d’initialisation, d’initialisation et d’utilisation d’une section appelée **g_csSharedTable**.
  
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

Un autre moyen, peut-être plus sûr, de protéger un bloc de mémoire consiste à créer une classe qui contient ses propres **CRITICAL_SECTION** et dont le constructeur, le destructeur et les méthodes d’accesseur prennent en charge son utilisation. Cette approche présente l’avantage supplémentaire de protéger les objets qui peuvent être initialisés avant l’utilisation de **xlAutoOpen,** ou de résister après l’appel de **xlAutoClose,** mais vous devez faire attention à la création de trop de sections critiques et à la surcharge du système d’exploitation que cela créerait. 
  
Lorsque vous avez du code qui a besoin d’accéder à plusieurs blocs de mémoire protégée en même temps, vous devez considérer très attentivement l’ordre dans lequel les sections critiques sont entrées et sorties. Par exemple, les deux fonctions suivantes peuvent créer un blocage.
  
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

Si la première fonction d’un thread entre **g_csSharedTableA** tandis que la seconde sur un autre thread entre g_csSharedTableB **,** les deux threads se bloquent. L’approche correcte consiste à entrer dans un ordre cohérent et à quitter dans l’ordre inverse, comme suit.
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

Dans la mesure du possible, il est préférable d’un point de vue de la co-exploitation de thread d’isoler l’accès à des blocs distincts, comme illustré ici.
  
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

En cas de conflit important pour une ressource partagée, telle que des demandes d’accès fréquentes de courte durée, vous devez envisager d’utiliser la capacité de rotation de la section critique. Il s’agit d’une technique qui rend l’attente de la ressource moins intensive en processeur. Pour ce faire, vous pouvez utiliser **InitializeCriticalSectionAndSpinCount** lors de l’initialisation de la section ou **SetCriticalSectionSpinCount** une fois initialisé, pour définir le nombre de boucles du thread avant d’attendre que des ressources deviennent disponibles. L’opération d’attente est coûteuse, donc la rotation évite cela si la ressource est libérée entre-temps. Sur un système de processeur unique, le nombre de rotations est effectivement ignoré, mais vous pouvez toujours le spécifier sans causer de dommages. Le gestionnaire de tas de mémoire utilise un nombre de rotations de 4 000. Pour plus d’informations sur l’utilisation des sections critiques, voir la documentation du SDK Windows. 
  
## <a name="see-also"></a>Voir aussi



[Gestion de la mémoire dans Excel](memory-management-in-excel.md)
  
[Recalcul multithread dans Excel](multithreaded-recalculation-in-excel.md)
  
[Fonctions du Gestionnaire de compléments et de l’interface XLL](add-in-manager-and-xll-interface-functions.md)

