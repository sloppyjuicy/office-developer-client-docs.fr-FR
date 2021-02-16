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
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="04674-104">Multithreading et contention de mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="04674-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="04674-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="04674-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="04674-106">Les versions de Microsoft Excel antérieures à Excel 2007 utilisent un thread unique pour tous les calculs de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="04674-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="04674-107">Toutefois, à partir d’Excel 2007, Excel peut être configuré pour utiliser entre 1 et 1 024 threads simultanés pour le calcul de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="04674-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="04674-108">Sur un ordinateur multi-processeur ou multi cœur, le nombre de threads par défaut est égal au nombre de processeurs ou de cœurs.</span><span class="sxs-lookup"><span data-stu-id="04674-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="04674-109">Par conséquent, les cellules thread-safe, ou les cellules qui contiennent uniquement des fonctions thread-safe, peuvent être allouées à des threads simultanés, sous réserve de la logique de recalcul habituelle de la nécessité d’être calculées après leurs antécédents.</span><span class="sxs-lookup"><span data-stu-id="04674-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="04674-110">Thread-Safe fonctions</span><span class="sxs-lookup"><span data-stu-id="04674-110">Thread-Safe Functions</span></span>

<span data-ttu-id="04674-111">La plupart des fonctions de feuille de calcul intégrées à partir d’Excel 2007 sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="04674-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="04674-112">Vous pouvez également écrire et inscrire des fonctions XLL comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="04674-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="04674-113">Excel utilise un thread (son thread principal) pour appeler toutes les commandes, fonctions non thread-unsafe, **fonctions xlAuto** (à l’exception des fonctions [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**), et COM et Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="04674-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="04674-114">Lorsqu’une fonction XLL renvoie une **xlOPER** ou **XLOPER12** avec un ensemble **xlbitDLLFree,** Excel utilise le même thread sur lequel l’appel de fonction a été effectué pour appeler **xlAutoFree** ou **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="04674-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="04674-115">L’appel **à xlAutoFree** ou **xlAutoFree12** est effectué avant l’appel de fonction suivant sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="04674-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="04674-116">Pour les développeurs XLL, il existe des avantages à créer des fonctions thread-safe :</span><span class="sxs-lookup"><span data-stu-id="04674-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="04674-117">Elles permettent à Excel d’utiliser un ordinateur multi-processeur ou multi cœur.</span><span class="sxs-lookup"><span data-stu-id="04674-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="04674-118">Ils ouvrent la possibilité d’utiliser des serveurs distants beaucoup plus efficacement qu’avec un thread unique.</span><span class="sxs-lookup"><span data-stu-id="04674-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="04674-119">Supposons que vous disposez d’un ordinateur à processeur unique configuré pour utiliser, par exemple, *des threads N.*</span><span class="sxs-lookup"><span data-stu-id="04674-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="04674-120">Supposons qu’une feuille de calcul soit en cours d’exécution et qu’elle effectue un grand nombre d’appels à une fonction XLL qui à son tour envoie une demande de données ou un calcul à effectuer sur un serveur distant ou un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="04674-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="04674-121">Sous réserve de la topologie de l’arborescence des dépendances, Excel peut appeler la fonction N fois presque simultanément.</span><span class="sxs-lookup"><span data-stu-id="04674-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="04674-122">À condition que le ou les serveurs soient suffisamment rapides ou parallèles, le temps de recalcul de la feuille de calcul peut être réduit de 1/N.</span><span class="sxs-lookup"><span data-stu-id="04674-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="04674-123">Le problème clé dans l’écriture de fonctions thread-safe consiste à gérer correctement les conflits de ressources.</span><span class="sxs-lookup"><span data-stu-id="04674-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="04674-124">Cela signifie généralement une contention de mémoire et elle peut être décomposée en deux problèmes :</span><span class="sxs-lookup"><span data-stu-id="04674-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="04674-125">La façon de créer de la mémoire que vous savez sera utilisée uniquement par ce thread.</span><span class="sxs-lookup"><span data-stu-id="04674-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="04674-126">Comment s’assurer que la mémoire partagée est accessible par plusieurs threads en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="04674-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="04674-127">La première chose à savoir est la mémoire dans un XLL qui est accessible par tous les threads et ce qui est accessible uniquement par le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="04674-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="04674-128">**Accessible par tous les threads**</span><span class="sxs-lookup"><span data-stu-id="04674-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="04674-129">Variables, structures et instances de classe déclarées en dehors du corps d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="04674-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="04674-130">Variables statiques déclarées dans le corps d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="04674-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="04674-131">Dans ces deux cas, la mémoire est mise de côté dans le bloc de mémoire de la DLL créé pour cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="04674-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="04674-132">Si une autre instance d’application charge la DLL, elle obtient sa propre copie de cette mémoire afin qu’il n’y a aucun conflit pour ces ressources en dehors de cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="04674-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="04674-133">**Accessible uniquement par le thread actuel**</span><span class="sxs-lookup"><span data-stu-id="04674-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="04674-134">Variables automatiques dans le code de fonction (y compris les arguments de fonction).</span><span class="sxs-lookup"><span data-stu-id="04674-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="04674-135">Dans ce cas, la mémoire est mise de côté sur la pile pour chaque instance de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="04674-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="04674-136">L’étendue de la mémoire allouée dynamiquement dépend de l’étendue du pointeur qui pointe vers celle-ci : si le pointeur est accessible par tous les threads, la mémoire l’est également.</span><span class="sxs-lookup"><span data-stu-id="04674-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="04674-137">Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est en fait privée à ce thread.</span><span class="sxs-lookup"><span data-stu-id="04674-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="04674-138">Mémoire accessible par un seul thread : Thread-Local mémoire</span><span class="sxs-lookup"><span data-stu-id="04674-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="04674-139">Étant donné que les variables statiques dans le corps d’une fonction sont accessibles par tous les threads, les fonctions qui les utilisent ne sont clairement pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="04674-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="04674-140">Une instance de la fonction sur un thread peut être en train de modifier la valeur, tandis qu’une autre instance sur un autre thread suppose qu’il s’agit d’un sujet complètement différent.</span><span class="sxs-lookup"><span data-stu-id="04674-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="04674-141">Il existe deux raisons de déclarer des variables statiques au sein d’une fonction :</span><span class="sxs-lookup"><span data-stu-id="04674-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="04674-142">Les données statiques persistent d’un appel à l’autre.</span><span class="sxs-lookup"><span data-stu-id="04674-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="04674-143">Un pointeur vers des données statiques peut être renvoyé en toute sécurité par la fonction.</span><span class="sxs-lookup"><span data-stu-id="04674-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="04674-144">Dans le cas de la première raison, vous pouvez avoir des données qui persistent et ont une signification pour tous les appels à la fonction : peut-être un compteur simple qui est incrémenté chaque fois que la fonction est appelée sur n’importe quel thread, ou une structure qui collecte les données d’utilisation et de performances sur chaque appel.</span><span class="sxs-lookup"><span data-stu-id="04674-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="04674-145">La question est de savoir comment protéger la structure des données ou des données partagées.</span><span class="sxs-lookup"><span data-stu-id="04674-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="04674-146">Pour ce faire, il est préférable d’utiliser la section critique comme l’explique la section suivante.</span><span class="sxs-lookup"><span data-stu-id="04674-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="04674-147">Si les données sont destinées uniquement à être utilisés par ce thread, ce qui peut être le cas pour la raison 1 et toujours pour la raison 2, la question est de savoir comment créer une mémoire qui persiste mais qui est accessible uniquement à partir de ce thread.</span><span class="sxs-lookup"><span data-stu-id="04674-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="04674-148">Une solution consiste à utiliser l’API de stockage local de thread (TLS).</span><span class="sxs-lookup"><span data-stu-id="04674-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="04674-149">Par exemple, considérez une fonction qui renvoie un pointeur vers une **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="04674-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="04674-150">Cette fonction n’est pas thread-safe, car un thread peut renvoyer la **XLOPER12** statique, tandis qu’un autre la sur-réécrit.</span><span class="sxs-lookup"><span data-stu-id="04674-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="04674-151">La probabilité que cela se produise est encore plus élevée si **la xlOPER12** doit être passée à **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="04674-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="04674-152">Une solution consiste à allouer un **XLOPER12,** à renvoyer un pointeur vers celui-ci et à implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même soit libérée.</span><span class="sxs-lookup"><span data-stu-id="04674-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="04674-153">Cette approche est utilisée dans la plupart des exemples de fonctions présentés dans la gestion de [la mémoire dans Excel.](memory-management-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="04674-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="04674-154">Cette approche est plus simple à implémenter que l’approche décrite dans la section suivante, qui repose sur l’API TLS, mais présente certains inconvénients.</span><span class="sxs-lookup"><span data-stu-id="04674-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="04674-155">Tout d’abord, Excel doit appeler **xlAutoFree** /  **xlAutoFree12** quel que soit le type de **xlOPER** /  **XLOPER12 renvoyé.**</span><span class="sxs-lookup"><span data-stu-id="04674-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="04674-156">Deuxièmement, il existe un problème lors du renvoi de **XLOPER** /  **XLOPER12** qui sont la valeur de retour d’un appel à une fonction de rappel d’API C.</span><span class="sxs-lookup"><span data-stu-id="04674-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12** s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="04674-157">La **xlOPER** XLOPER12 peut pointer vers la mémoire qui doit être libérée par Excel, mais la /   **XLOPER** /  **XLOPER12** elle-même doit être libérée de la même façon qu’elle a été allouée.</span><span class="sxs-lookup"><span data-stu-id="04674-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="04674-158">Si une **xlOPER** XLOPER12 de ce type doit être utilisée comme valeur de retour d’une fonction de feuille de calcul XLL, il n’existe aucun moyen simple d’informer /   **xlAutoFree** /  **xlAutoFree12** de la nécessité de libérer les deux pointeurs de la manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="04674-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="04674-159">(La définition de **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, car le traitement de **XLOPER/XLOPER12s** dans Excel avec les deux ensembles n’est pas définie et peut changer de version.) Pour contourner ce problème, le XLL peut effectuer des copies détaillées de toutes les **XLOPER/XLOPER12 allouées** par Excel qu’elle renvoie à la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="04674-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="04674-160">Une solution qui évite ces limitations consiste à remplir et renvoyer une **XLOPER/XLOPER12** locale de thread, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne libère pas le pointeur **XLOPER/XLOPER12** lui-même.</span><span class="sxs-lookup"><span data-stu-id="04674-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="04674-161">La question suivante est de savoir comment configurer et récupérer la mémoire locale de thread, en d’autres termes, comment implémenter la fonction get_thread_local_xloper12 **dans** l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="04674-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="04674-162">Pour ce faire, utilisez l’API de stockage local de thread (TLS).</span><span class="sxs-lookup"><span data-stu-id="04674-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="04674-163">La première étape consiste à obtenir un index TLS à l’aide de **TlsAlloc**, qui doit finalement être publié à l’aide de **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="04674-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="04674-164">Les deux sont mieux accomplies à partir **de DllMain**.</span><span class="sxs-lookup"><span data-stu-id="04674-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="04674-165">Une fois l’index obtenu, l’étape suivante consiste à allouer un bloc de mémoire pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="04674-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="04674-166">La [documentation de développement Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) vous recommande de le faire chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et libérant la mémoire sur chaque **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="04674-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="04674-167">Toutefois, le fait de suivre ces conseils entraînerait le travail inutile de votre DLL pour les threads qui ne sont pas utilisés pour le recalcul.</span><span class="sxs-lookup"><span data-stu-id="04674-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="04674-168">Au lieu de cela, il est préférable d’utiliser une stratégie d’allocation à la première utilisation.</span><span class="sxs-lookup"><span data-stu-id="04674-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="04674-169">Tout d’abord, vous devez définir une structure que vous souhaitez allouer pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="04674-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="04674-170">Pour les exemples précédents qui retournent **xlOPERs** ou **XLOPER12s,** voici ce qui suffit, mais vous pouvez créer n’importe quelle structure qui répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="04674-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="04674-171">La fonction suivante obtient un pointeur vers l’instance thread-local, ou en alloue un s’il s’agit du premier appel.</span><span class="sxs-lookup"><span data-stu-id="04674-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="04674-172">Vous pouvez maintenant voir comment la mémoire **XLOPER/XLOPER12** locale du thread est obtenue : tout d’abord, vous obtenez un pointeur vers l’instance **de TLS_data** du thread, puis vous renvoyez un pointeur vers la **XLOPER/XLOPER12** qu’elle contient, comme suit.</span><span class="sxs-lookup"><span data-stu-id="04674-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="04674-173">Les **fonctions mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel.</span><span class="sxs-lookup"><span data-stu-id="04674-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="04674-174">Toutefois, vous ne pouvez pas combiner les deux approches dans une seule XLL.</span><span class="sxs-lookup"><span data-stu-id="04674-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="04674-175">Votre XLL ne peut exporter qu’une seule implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire nécessite une approche différente.</span><span class="sxs-lookup"><span data-stu-id="04674-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="04674-176">Avec **mtr_safe_example_1,** le pointeur transmis à **xlAutoFree/xlAutoFree12** doit être libéré avec toutes les données vers qui il pointe.</span><span class="sxs-lookup"><span data-stu-id="04674-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="04674-177">Avec **mtr_safe_example_2**, seules les données pointées doivent être libérées.</span><span class="sxs-lookup"><span data-stu-id="04674-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="04674-178">Windows fournit également une **fonction GetCurrentThreadId**, qui renvoie l’ID unique à l’échelle du système du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="04674-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="04674-179">Cela permet au développeur de rendre le thread de code sécurisé ou de rendre son thread de comportement spécifique.</span><span class="sxs-lookup"><span data-stu-id="04674-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="04674-180">Mémoire accessible uniquement par plusieurs threads : sections critiques</span><span class="sxs-lookup"><span data-stu-id="04674-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="04674-181">Vous devez protéger la mémoire en lecture/écriture accessible par plusieurs threads à l’aide de sections critiques.</span><span class="sxs-lookup"><span data-stu-id="04674-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="04674-182">Vous avez besoin d’une section critique nommée pour chaque bloc de mémoire que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="04674-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="04674-183">Vous pouvez initialiser ces derniers pendant l’appel à la fonction **xlAutoOpen,** les libérer et les définir sur null lors de l’appel à la fonction **xlAutoClose.**</span><span class="sxs-lookup"><span data-stu-id="04674-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="04674-184">Vous devez ensuite contenir chaque accès au bloc protégé dans une paire d’appels à **EnterCriticalSection** et **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="04674-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="04674-185">Un seul thread est autorisé dans la section critique à tout moment.</span><span class="sxs-lookup"><span data-stu-id="04674-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="04674-186">Voici un exemple d’initialisation, d’initialisation et d’utilisation d’une section appelée **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="04674-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="04674-187">Un autre moyen, peut-être plus sûr, de protéger un bloc de mémoire consiste à créer une classe qui contient ses propres **CRITICAL_SECTION** et dont le constructeur, le destructeur et les méthodes d’accesseur prennent en charge son utilisation.</span><span class="sxs-lookup"><span data-stu-id="04674-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="04674-188">Cette approche présente l’avantage supplémentaire de protéger les objets qui peuvent être initialisés avant l’utilisation de **xlAutoOpen,** ou de résister après l’appel de **xlAutoClose,** mais vous devez faire attention à la création de trop de sections critiques et à la surcharge du système d’exploitation que cela créerait.</span><span class="sxs-lookup"><span data-stu-id="04674-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="04674-189">Lorsque vous avez du code qui a besoin d’accéder à plusieurs blocs de mémoire protégée en même temps, vous devez considérer très attentivement l’ordre dans lequel les sections critiques sont entrées et sorties.</span><span class="sxs-lookup"><span data-stu-id="04674-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="04674-190">Par exemple, les deux fonctions suivantes peuvent créer un blocage.</span><span class="sxs-lookup"><span data-stu-id="04674-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="04674-191">Si la première fonction d’un thread entre **g_csSharedTableA** tandis que la seconde sur un autre thread entre g_csSharedTableB **,** les deux threads se bloquent.</span><span class="sxs-lookup"><span data-stu-id="04674-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="04674-192">L’approche correcte consiste à entrer dans un ordre cohérent et à quitter dans l’ordre inverse, comme suit.</span><span class="sxs-lookup"><span data-stu-id="04674-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="04674-193">Dans la mesure du possible, il est préférable d’un point de vue de la co-exploitation de thread d’isoler l’accès à des blocs distincts, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="04674-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="04674-194">En cas de conflit important pour une ressource partagée, telle que des demandes d’accès fréquentes de courte durée, vous devez envisager d’utiliser la capacité de rotation de la section critique.</span><span class="sxs-lookup"><span data-stu-id="04674-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="04674-195">Il s’agit d’une technique qui rend l’attente de la ressource moins intensive en processeur.</span><span class="sxs-lookup"><span data-stu-id="04674-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="04674-196">Pour ce faire, vous pouvez utiliser **InitializeCriticalSectionAndSpinCount** lors de l’initialisation de la section ou **SetCriticalSectionSpinCount** une fois initialisé, pour définir le nombre de boucles du thread avant d’attendre que des ressources deviennent disponibles.</span><span class="sxs-lookup"><span data-stu-id="04674-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="04674-197">L’opération d’attente est coûteuse, donc la rotation évite cela si la ressource est libérée entre-temps.</span><span class="sxs-lookup"><span data-stu-id="04674-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="04674-198">Sur un système de processeur unique, le nombre de rotations est effectivement ignoré, mais vous pouvez toujours le spécifier sans causer de dommages.</span><span class="sxs-lookup"><span data-stu-id="04674-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="04674-199">Le gestionnaire de tas de mémoire utilise un nombre de rotations de 4 000.</span><span class="sxs-lookup"><span data-stu-id="04674-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="04674-200">Pour plus d’informations sur l’utilisation des sections critiques, voir la documentation du SDK Windows.</span><span class="sxs-lookup"><span data-stu-id="04674-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04674-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04674-201">See also</span></span>



[<span data-ttu-id="04674-202">Gestion de la mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="04674-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="04674-203">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="04674-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="04674-204">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="04674-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

