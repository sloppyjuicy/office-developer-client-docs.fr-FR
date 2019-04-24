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
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="74a55-104">Multithreading et contention de la mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="74a55-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="74a55-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="74a55-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="74a55-106">Les versions de Microsoft Excel antérieures à Excel 2007 utilisent un seul thread pour tous les calculs de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="74a55-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="74a55-107">Toutefois, en commençant dans Excel 2007, Excel peut être configuré pour utiliser de 1 à 1024 threads simultanés pour le calcul de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="74a55-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="74a55-108">Sur un ordinateur multiprocesseur ou multicœur, le nombre de threads par défaut est égal au nombre de processeurs ou cœurs.</span><span class="sxs-lookup"><span data-stu-id="74a55-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="74a55-109">Par conséquent, les cellules thread-safe, ou les cellules qui contiennent uniquement des fonctions thread-safe, peuvent être attribuées à des threads simultanés, sous réserve de la logique de Recalculation habituelle de la nécessité de les calculer après leurs antécédents.</span><span class="sxs-lookup"><span data-stu-id="74a55-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="74a55-110">Fonctions thread-safe</span><span class="sxs-lookup"><span data-stu-id="74a55-110">Thread-Safe Functions</span></span>

<span data-ttu-id="74a55-111">La plupart des fonctions de feuille de calcul intégrées commençant dans Excel 2007 sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="74a55-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="74a55-112">Vous pouvez également écrire et enregistrer des fonctions XLL comme thread-safe.</span><span class="sxs-lookup"><span data-stu-id="74a55-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="74a55-113">Excel utilise un thread (son thread principal) pour appeler toutes les commandes, les fonctions non sécurisées de thread, les fonctions **xlAuto** (à l'exception de [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**), ainsi que les fonctions com et Visual Basic pour applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="74a55-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="74a55-114">Lorsqu'une fonction XLL renvoie un élément **XLOPER** ou **XLOPER12** avec **xlbitDLLFree** , Excel utilise le même thread que celui sur lequel l'appel de la fonction a été effectué pour appeler **xlAutoFree** ou **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="74a55-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="74a55-115">L'appel à **xlAutoFree** ou **xlAutoFree12** est effectué avant l'appel de fonction suivant sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="74a55-116">Pour les développeurs XLL, il existe des avantages pour la création de fonctions thread-safe:</span><span class="sxs-lookup"><span data-stu-id="74a55-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="74a55-117">Elles permettent à Excel de tirer le meilleur parti d'un ordinateur multiprocesseur ou multicœur.</span><span class="sxs-lookup"><span data-stu-id="74a55-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="74a55-118">Ils ouvrent la possibilité d'utiliser des serveurs distants de manière bien plus efficace qu'ils ne peuvent le faire à l'aide d'un seul thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="74a55-119">Supposons que vous disposez d'un ordinateur à un seul processeur configuré pour utiliser, disons, *N* threads.</span><span class="sxs-lookup"><span data-stu-id="74a55-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="74a55-120">Supposons qu'une feuille de calcul est en cours d'exécution et qu'elle effectue un grand nombre d'appels à une fonction XLL qui envoie à son tour une demande de données ou un calcul à effectuer sur un serveur ou un cluster de serveurs distant.</span><span class="sxs-lookup"><span data-stu-id="74a55-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="74a55-121">Sous réserve de la topologie de l'arborescence des dépendances, Excel peut appeler la fonction N fois presque simultanément.</span><span class="sxs-lookup"><span data-stu-id="74a55-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="74a55-122">Étant donné que le ou les serveurs sont suffisamment rapides ou parallèles, le temps de recalcul de la feuille de calcul peut être réduit de 1/N.</span><span class="sxs-lookup"><span data-stu-id="74a55-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="74a55-123">Le problème clé lors de l'écriture de fonctions thread-safe consiste à gérer correctement la contention des ressources.</span><span class="sxs-lookup"><span data-stu-id="74a55-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="74a55-124">Cela signifie généralement une contention de mémoire et peut être divisée en deux problèmes:</span><span class="sxs-lookup"><span data-stu-id="74a55-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="74a55-125">La façon de créer de la mémoire qui sera utilisée uniquement par ce thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="74a55-126">Comment s'assurer que plusieurs threads accèdent à la mémoire partagée en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="74a55-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="74a55-127">La première chose à savoir est que la mémoire d'une XLL est accessible par tous les threads et ce qui est uniquement accessible par le thread en cours d'exécution.</span><span class="sxs-lookup"><span data-stu-id="74a55-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="74a55-128">**Accessible par tous les threads**</span><span class="sxs-lookup"><span data-stu-id="74a55-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="74a55-129">Variables, structures et instances de classe déclarées à l'extérieur du corps d'une fonction.</span><span class="sxs-lookup"><span data-stu-id="74a55-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="74a55-130">Variables statiques déclarées dans le corps d'une fonction.</span><span class="sxs-lookup"><span data-stu-id="74a55-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="74a55-131">Dans ces deux cas, la mémoire est réservée dans le bloc de mémoire de la DLL créé pour cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="74a55-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="74a55-132">Si une autre instance d'application charge la DLL, elle obtient sa propre copie de cette mémoire de sorte qu'il n'existe aucun conflit pour ces ressources provenant de l'extérieur de cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="74a55-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="74a55-133">**Accessible uniquement par le thread actuel**</span><span class="sxs-lookup"><span data-stu-id="74a55-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="74a55-134">Variables automatiques dans le code de fonction (y compris les arguments de fonction).</span><span class="sxs-lookup"><span data-stu-id="74a55-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="74a55-135">Dans ce cas, la mémoire est réservée sur la pile pour chaque instance de l'appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="74a55-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="74a55-136">L'étendue de la mémoire allouée dynamiquement dépend de la portée du pointeur qui pointe vers elle: si le pointeur est accessible par tous les threads, la mémoire est également.</span><span class="sxs-lookup"><span data-stu-id="74a55-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="74a55-137">Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est réellement propre à ce thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="74a55-138">Mémoire accessible par un seul thread: mémoire locale de thread</span><span class="sxs-lookup"><span data-stu-id="74a55-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="74a55-139">Étant donné que les variables statiques dans le corps d'une fonction sont accessibles par tous les threads, les fonctions qui les utilisent ne sont manifestement pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="74a55-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="74a55-140">Une instance de la fonction sur un thread peut modifier la valeur tandis qu'une autre instance sur un autre thread suppose qu'elle est complètement différente.</span><span class="sxs-lookup"><span data-stu-id="74a55-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="74a55-141">Il existe deux raisons pour déclarer des variables statiques au sein d'une fonction:</span><span class="sxs-lookup"><span data-stu-id="74a55-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="74a55-142">Les données statiques sont conservées d'un appel à l'autre.</span><span class="sxs-lookup"><span data-stu-id="74a55-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="74a55-143">Un pointeur vers des données statiques peut être retourné en toute sécurité par la fonction.</span><span class="sxs-lookup"><span data-stu-id="74a55-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="74a55-144">Dans le cas d'une première raison, vous pouvez souhaiter avoir des données qui persistent et ont une signification pour tous les appels à la fonction: un simple compteur qui est peut-être incrémenté chaque fois que la fonction est appelée sur un thread ou une structure qui collecte les données d'utilisation et de performances en veille. appel Ry.</span><span class="sxs-lookup"><span data-stu-id="74a55-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="74a55-145">La question est de savoir comment protéger les données partagées ou la structure des données.</span><span class="sxs-lookup"><span data-stu-id="74a55-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="74a55-146">Pour ce faire, vous devez utiliser la section critique, comme décrit dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="74a55-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="74a55-147">Si les données sont destinées uniquement à être utilisées par ce thread, ce qui peut être le cas pour la raison 1 et est toujours le cas pour la raison 2, la question est la façon de créer de la mémoire qui persiste, mais qui n'est accessible qu'à partir de ce thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="74a55-148">Une solution consiste à utiliser l'API de stockage local de thread (TLS).</span><span class="sxs-lookup"><span data-stu-id="74a55-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="74a55-149">Prenons l'exemple d'une fonction qui renvoie un pointeur vers un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="74a55-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="74a55-150">Cette fonction n'est pas thread-safe, car un thread peut renvoyer le **XLOPER12** statique, tandis qu'un autre peut le remplacer.</span><span class="sxs-lookup"><span data-stu-id="74a55-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="74a55-151">La probabilité que cela se produise est encore plus importante si la version de **XLOPER12** doit être passée à **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="74a55-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="74a55-152">Une solution consiste à allouer un **XLOPER12**, renvoyer un pointeur vers celui-ci et implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même soit libérée.</span><span class="sxs-lookup"><span data-stu-id="74a55-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="74a55-153">Cette approche est utilisée dans de nombreux exemples de fonctions illustrés dans la [gestion de la mémoire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="74a55-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="74a55-154">Cette approche est plus simple à mettre en œuvre que l'approche décrite dans la section suivante, qui repose sur l'API TLS, mais présente quelques inconvénients.</span><span class="sxs-lookup"><span data-stu-id="74a55-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="74a55-155">Tout d'abord, Excel doit appeler **xlAutoFree**/ **xlAutoFree12** quel que soit le type de l' **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="74a55-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="74a55-156">Deuxièmement, il y a un problème lors du renvoi des savesets **XLOPER**/ \*\*\*\* de la valeur de retour d'un appel à une fonction de rappel de l'API C.</span><span class="sxs-lookup"><span data-stu-id="74a55-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="74a55-157">La demande **XLOPER**/ \*\*\*\* peut pointer vers la mémoire qui doit être libérée par Excel, mais la méthode **XLOPER**/ \*\*\*\* propre elle-même doit être libérée de la même façon qu'elle.</span><span class="sxs-lookup"><span data-stu-id="74a55-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="74a55-158">Si une telle **expression XLOPER**/ \*\*\*\* doit être utilisée comme valeur de retour d'une fonction de feuille de calcul XLL, il n'existe pas de moyen simple d'informer **xlAutoFree**/ **xlAutoFree12** de la nécessité de libérer les deux pointeurs de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="74a55-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="74a55-159">(Le fait de définir à la fois **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, car le traitement de **XLOPER/XLOPER12** dans Excel avec les deux ensembles n'est pas défini et peut passer de la version à la version.) Pour contourner ce problème, le XLL peut effectuer des copies complètes de tous les **XLOPER/XLOPER12** alloués par Excel qu'il renvoie à la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="74a55-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="74a55-160">Une solution qui évite ces limitations est de remplir et de renvoyer une structure **XLOPER/XLOPER12**locale de thread, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne libère pas le pointeur **XLOPER/XLOPER12** lui-même.</span><span class="sxs-lookup"><span data-stu-id="74a55-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="74a55-161">La question suivante concerne la configuration et la récupération de la mémoire locale de thread, en d'autres termes, comment implémenter la fonction **get_thread_local_xloper12** dans l'exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="74a55-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="74a55-162">Cette opération est réalisée à l'aide de l'API de stockage local des threads (TLS).</span><span class="sxs-lookup"><span data-stu-id="74a55-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="74a55-163">La première étape consiste à obtenir un index TLS à l'aide de **TlsAlloc**, qui doit finalement être publié à l'aide de **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="74a55-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="74a55-164">Les deux sont les mieux effectués à partir de **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="74a55-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="74a55-165">Une fois l'index obtenu, l'étape suivante consiste à allouer un bloc de mémoire pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="74a55-166">La [documentation de développement Windows](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommande d'effectuer cette opération chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et de libérer de la mémoire sur chaque **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="74a55-166">The [Windows Development Documentation](https://msdn.microsoft.com/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="74a55-167">Toutefois, à la suite de ce Conseil, votre DLL n'effectuera pas de travail inutile pour les threads qui n'ont pas été utilisés pour le recalcul.</span><span class="sxs-lookup"><span data-stu-id="74a55-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="74a55-168">Au lieu de cela, il est préférable d'utiliser une stratégie d'allocation à la première utilisation.</span><span class="sxs-lookup"><span data-stu-id="74a55-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="74a55-169">Tout d'abord, vous devez définir une structure que vous souhaitez allouer à chaque thread.</span><span class="sxs-lookup"><span data-stu-id="74a55-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="74a55-170">Pour les exemples précédents qui renvoient **XLOPER** ou **XLOPER12**, les éléments suivants suffisent, mais vous pouvez créer une structure qui répond à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="74a55-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="74a55-171">La fonction suivante obtient un pointeur vers l'instance locale de thread ou alloue une s'il s'agit du premier appel.</span><span class="sxs-lookup"><span data-stu-id="74a55-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="74a55-172">À présent, vous pouvez voir comment la mémoire locale **XLOPER/XLOPER12** est obtenue: tout d'abord, vous obtenez un pointeur vers l'instance de la thread de **TLS_data**, puis vous renvoyez un pointeur vers l'élément **XLOPER/XLOPER12** qu'elle contient, comme suit.</span><span class="sxs-lookup"><span data-stu-id="74a55-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="74a55-173">Les fonctions **mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel.</span><span class="sxs-lookup"><span data-stu-id="74a55-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="74a55-174">Toutefois, vous ne pouvez pas mélanger les deux approches dans une XLL.</span><span class="sxs-lookup"><span data-stu-id="74a55-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="74a55-175">Votre XLL ne peut exporter qu'une seule implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire requiert une approche différente.</span><span class="sxs-lookup"><span data-stu-id="74a55-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="74a55-176">Avec **mtr_safe_example_1**, le pointeur transmis à **xlAutoFree/xlAutoFree12** doit être libéré en même temps que les données vers lesquelles il pointe.</span><span class="sxs-lookup"><span data-stu-id="74a55-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="74a55-177">Avec **mtr_safe_example_2**, seules les données ciblées doivent être libérées.</span><span class="sxs-lookup"><span data-stu-id="74a55-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="74a55-178">Windows fournit également une fonction **GetCurrentThreadID**, qui renvoie l'ID système unique du thread actuel.</span><span class="sxs-lookup"><span data-stu-id="74a55-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="74a55-179">Cela permet au développeur d'utiliser une autre méthode pour mettre en danger les threads de code ou de définir son comportement de thread propre.</span><span class="sxs-lookup"><span data-stu-id="74a55-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="74a55-180">Mémoire accessible uniquement par plus d'un thread: sections critiques</span><span class="sxs-lookup"><span data-stu-id="74a55-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="74a55-181">Vous devez protéger la mémoire en lecture/écriture accessible par plusieurs threads à l'aide de sections critiques.</span><span class="sxs-lookup"><span data-stu-id="74a55-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="74a55-182">Vous avez besoin d'une section critique nommée pour chaque bloc de mémoire que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="74a55-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="74a55-183">Vous pouvez les initialiser pendant l'appel à la fonction **xlAutoOpen** , puis les publier et les définir sur null pendant l'appel de la fonction **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="74a55-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="74a55-184">Vous devez ensuite contenir chaque accès au bloc protégé dans une paire d'appels vers **EnterCriticalSection** et **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="74a55-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="74a55-185">Un seul thread est autorisé à la section critique à tout moment.</span><span class="sxs-lookup"><span data-stu-id="74a55-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="74a55-186">Voici un exemple de l'initialisation, de l'échec d'initialisation et de l'utilisation d'une section appelée **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="74a55-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="74a55-187">Un autre moyen plus sûr de protéger un bloc de mémoire consiste à créer une classe qui contient son propre **critical_section** et dont les méthodes de constructeur, de destructeur et d'accesseur prennent en charge leur utilisation.</span><span class="sxs-lookup"><span data-stu-id="74a55-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="74a55-188">Cette approche présente l'avantage supplémentaire de protéger les objets qui peuvent être initialisés avant l'exécution d' **xlAutoOpen** ou survivent après l'appel de **xlAutoClose** , mais vous devez être attentif à la création d'un trop grand nombre de sections critiques et du système d'exploitation charge de travail créée.</span><span class="sxs-lookup"><span data-stu-id="74a55-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="74a55-189">Lorsque vous avez du code qui a besoin d'accéder à plusieurs blocs de mémoire protégée en même temps, vous devez tenir compte de l'ordre dans lequel les sections critiques sont entrées et sorties.</span><span class="sxs-lookup"><span data-stu-id="74a55-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="74a55-190">Par exemple, les deux fonctions suivantes peuvent créer un blocage.</span><span class="sxs-lookup"><span data-stu-id="74a55-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="74a55-191">Si la première fonction sur un thread entre **g_csSharedTableA** tandis que la seconde sur un autre, entre **g_csSharedTableB**, les deux threads se bloquent.</span><span class="sxs-lookup"><span data-stu-id="74a55-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="74a55-192">L'approche correcte consiste à entrer un ordre cohérent et à quitter l'ordre inverse, comme suit.</span><span class="sxs-lookup"><span data-stu-id="74a55-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="74a55-193">Dans la mesure du possible, il est préférable d'avoir un point de vue de la co-opération de thread pour isoler l'accès à des blocs distincts, comme illustré ici.</span><span class="sxs-lookup"><span data-stu-id="74a55-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="74a55-194">Lorsqu'il existe beaucoup de contention pour une ressource partagée, telle que des demandes d'accès de courte durée fréquentes, vous devez envisager d'utiliser la fonctionnalité de la section critique pour faire tourner.</span><span class="sxs-lookup"><span data-stu-id="74a55-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="74a55-195">Il s'agit d'une technique qui rend l'attente de ressources moins gourmandes en processeur.</span><span class="sxs-lookup"><span data-stu-id="74a55-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="74a55-196">Pour ce faire, vous pouvez utiliser l'un ou l'autre **InitializeCriticalSectionAndSpinCount** lors de l'initialisation de la section ou de **SetCriticalSectionSpinCount** une fois initialisé, afin de définir le nombre de boucles du thread avant d'attendre que les ressources deviennent possibles.</span><span class="sxs-lookup"><span data-stu-id="74a55-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="74a55-197">L'opération d'attente est coûteuse, ce qui évite cela si la ressource est libérée entre temps.</span><span class="sxs-lookup"><span data-stu-id="74a55-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="74a55-198">Sur un système à processeur unique, le nombre de spins est effectivement ignoré, mais vous pouvez toujours le spécifier sans nuire.</span><span class="sxs-lookup"><span data-stu-id="74a55-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="74a55-199">Le gestionnaire de tas de mémoire utilise un nombre de spins de 4000.</span><span class="sxs-lookup"><span data-stu-id="74a55-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="74a55-200">Pour plus d'informations sur l'utilisation des sections critiques, reportez-vous à la documentation du kit de développement logiciel Windows.</span><span class="sxs-lookup"><span data-stu-id="74a55-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="74a55-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74a55-201">See also</span></span>



[<span data-ttu-id="74a55-202">Gestion de la m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="74a55-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="74a55-203">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="74a55-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="74a55-204">Fonctions du Gestionnaire de compléments et de l’interface XLL</span><span class="sxs-lookup"><span data-stu-id="74a55-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

