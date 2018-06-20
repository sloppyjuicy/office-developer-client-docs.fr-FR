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
# <a name="multithreading-and-memory-contention-in-excel"></a><span data-ttu-id="00c56-104">Multithreading et la Contention de mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="00c56-104">Multithreading and Memory Contention in Excel</span></span>

 <span data-ttu-id="00c56-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="00c56-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="00c56-106">Versions de Microsoft Excel antérieures à Excel 2007 utilisent un seul thread pour tous les calculs de feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="00c56-106">Versions of Microsoft Excel earlier than Excel 2007 use a single thread for all worksheet calculations.</span></span> <span data-ttu-id="00c56-107">Toutefois, à compter d’Excel 2007, Excel peut être configuré pour utiliser à partir de 1 à des threads simultanés 1024 pour le calcul de la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="00c56-107">However, starting in Excel 2007, Excel can be configured to use from 1 to 1024 concurrent threads for worksheet calculation.</span></span> <span data-ttu-id="00c56-108">Sur un ordinateur multiprocesseur ou multicœur, le nombre de threads par défaut est égal au nombre de processeurs ou cœurs.</span><span class="sxs-lookup"><span data-stu-id="00c56-108">On a multi-processor or multi-core computer, the default number of threads is equal to the number of processors or cores.</span></span> <span data-ttu-id="00c56-109">Par conséquent, thread-safe cellules ou les cellules qui contiennent uniquement des fonctions qui sont thread-safe, pouvant être attribuées à des threads simultanés, soumis à la logique de recalcul habituels de devoir être calculée après leurs antécédents.</span><span class="sxs-lookup"><span data-stu-id="00c56-109">Therefore, thread-safe cells, or cells that only contain functions that are thread safe, can be allotted to concurrent threads, subject to the usual recalculation logic of needing to be calculated after their precedents.</span></span>
  
## <a name="thread-safe-functions"></a><span data-ttu-id="00c56-110">Fonctions de thread-Safe</span><span class="sxs-lookup"><span data-stu-id="00c56-110">Thread-Safe Functions</span></span>

<span data-ttu-id="00c56-111">La plupart des fonctions de feuille de calcul intégré à compter d’Excel 2007 sont thread-safe.</span><span class="sxs-lookup"><span data-stu-id="00c56-111">Most of the built-in worksheet functions starting in Excel 2007 are thread safe.</span></span> <span data-ttu-id="00c56-112">Vous pouvez également écrire et enregistrer les fonctions XLL comme étant thread-safe.</span><span class="sxs-lookup"><span data-stu-id="00c56-112">You can also write and register XLL functions as being thread safe.</span></span> <span data-ttu-id="00c56-113">Excel utilise un seul thread (son thread principal) pour appeler tous les commandes, fonctions non sécurisées, des fonctions **xlAuto** (sauf [xlAutoFree](xlautofree-xlautofree12.md) et **xlAutoFree12**) et COM et Visual Basic pour les fonctions d’Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="00c56-113">Excel uses one thread (its main thread) to call all commands, thread-unsafe functions, **xlAuto** functions (except [xlAutoFree](xlautofree-xlautofree12.md) and **xlAutoFree12**), and COM and Visual Basic for Applications (VBA) functions.</span></span>
  
<span data-ttu-id="00c56-114">Où une fonction XLL retourne une **XLOPER** ou un **XLOPER12** **xlbitDLLFree** pourvue, Excel utilise le même thread sur lequel l’appel de fonction a été effectuée pour appeler **xlAutoFree** ou **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="00c56-114">Where an XLL function returns an **XLOPER** or **XLOPER12** with **xlbitDLLFree** set, Excel uses the same thread on which the function call was made to call **xlAutoFree** or **xlAutoFree12**.</span></span> <span data-ttu-id="00c56-115">L’appel à **xlAutoFree** ou **xlAutoFree12** est effectué avant le prochain appel de fonction sur ce thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-115">The call to **xlAutoFree** or **xlAutoFree12** is made before the next function call on that thread.</span></span> 
  
<span data-ttu-id="00c56-116">Pour les développeurs XLL, voici les avantages pour la création de fonctions de thread-safe :</span><span class="sxs-lookup"><span data-stu-id="00c56-116">For XLL developers, there are benefits for creating thread-safe functions:</span></span>
  
- <span data-ttu-id="00c56-117">Ils permettent à Microsoft Excel pour que le plus d’un ordinateur multiprocesseur ou multicœur.</span><span class="sxs-lookup"><span data-stu-id="00c56-117">They allow Excel to make the most of a multi-processor or multi-core computer.</span></span>
    
- <span data-ttu-id="00c56-118">Ils ouvriront la possibilité d’utiliser des serveurs distants beaucoup plus efficace peut être effectuée à l’aide d’un seul thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-118">They open up the possibility of using remote servers much more efficiently than can be done using a single thread.</span></span>
    
<span data-ttu-id="00c56-119">Supposons que vous disposez d’un ordinateur à processeur unique qui a été configuré pour utiliser, par exemple, les threads de *N* .</span><span class="sxs-lookup"><span data-stu-id="00c56-119">Suppose that you have a single-processor computer that has been configured to use, say,  *N*  threads.</span></span> <span data-ttu-id="00c56-120">Supposons qu’une feuille de calcul est en cours d’exécution que fait un grand nombre d’appels à une fonction XLL qui tour envoie une demande de données ou pour un calcul à réaliser à un serveur distant ou un cluster de serveurs.</span><span class="sxs-lookup"><span data-stu-id="00c56-120">Suppose that a spreadsheet is running that makes a large number of calls to an XLL function that in turn sends a request for data or for a calculation to be performed to a remote server or cluster of servers.</span></span> <span data-ttu-id="00c56-121">Soumis à la topologie de l’arborescence de dépendance, Excel peut appeler les heures de la fonction N presque simultanément.</span><span class="sxs-lookup"><span data-stu-id="00c56-121">Subject to the topology of the dependency tree, Excel could call the function N times almost simultaneously.</span></span> <span data-ttu-id="00c56-122">L’ou les serveurs sont suffisamment rapide ou en parallèle, à condition que la durée de recalcul de la feuille de calcul peut être réduite en autant qu’un facteur de 1/N.</span><span class="sxs-lookup"><span data-stu-id="00c56-122">Provided that the server or servers are sufficiently fast or parallel, the recalculation time of the spreadsheet could be reduced by as much as a factor of 1/N.</span></span> 
  
<span data-ttu-id="00c56-123">La question de l’écriture de fonctions de thread-safe gère correctement contention des ressources.</span><span class="sxs-lookup"><span data-stu-id="00c56-123">The key issue in writing thread-safe functions is handling contention for resources correctly.</span></span> <span data-ttu-id="00c56-124">Cela signifie généralement que la contention de mémoire, et il peut être divisé en deux problèmes :</span><span class="sxs-lookup"><span data-stu-id="00c56-124">This usually means memory contention, and it can be broken down into two issues:</span></span>
  
- <span data-ttu-id="00c56-125">Comment créer la mémoire que vous connaissez est utilisé uniquement par ce thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-125">How to create memory that you know will only be used by this thread.</span></span>
    
- <span data-ttu-id="00c56-126">Comment s’assurer que mémoire partagée est accessible par plusieurs threads en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="00c56-126">How to ensure that shared memory is accessed by multiple threads safely.</span></span>
    
<span data-ttu-id="00c56-127">La première chose à connaître est quelle mémoire dans une solution XLL est accessible par tous les threads, et ce qui est accessible uniquement par le thread en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="00c56-127">The first thing to be aware of is what memory in an XLL is accessible by all threads, and what is only accessible by the currently executing thread.</span></span>
  
 <span data-ttu-id="00c56-128">**Accessible par tous les threads**</span><span class="sxs-lookup"><span data-stu-id="00c56-128">**Accessible by all threads**</span></span>
  
- <span data-ttu-id="00c56-129">Instances de classe, les structures et les variables déclarées en dehors du corps d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="00c56-129">Variables, structures, and class instances declared outside the body of a function.</span></span>
    
- <span data-ttu-id="00c56-130">Variables statiques déclarées dans le corps d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="00c56-130">Static variables declared within the body of a function.</span></span>
    
<span data-ttu-id="00c56-131">Dans ces deux cas, la mémoire est attribuée dans un bloc de mémoire de la DLL créé pour cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="00c56-131">In these two cases, memory is set aside in the DLL's memory block created for this instance of the DLL.</span></span> <span data-ttu-id="00c56-132">Si une autre instance de l’application charge la DLL, il obtient sa propre copie de la mémoire afin qu’il n’existe pas de conflit avec ces ressources en dehors de cette instance de la DLL.</span><span class="sxs-lookup"><span data-stu-id="00c56-132">If another application instance loads the DLL, it gets its own copy of that memory so that there is no contention for these resources from outside this instance of the DLL.</span></span>
  
 <span data-ttu-id="00c56-133">**Accessible uniquement par le thread actuel**</span><span class="sxs-lookup"><span data-stu-id="00c56-133">**Accessible only by the current thread**</span></span>
  
- <span data-ttu-id="00c56-134">Variables automatiques dans le code de la fonction (y compris les arguments de la fonction).</span><span class="sxs-lookup"><span data-stu-id="00c56-134">Automatic variables within function code (including function arguments).</span></span>
    
<span data-ttu-id="00c56-135">Dans ce cas, mémoire définie à part sur la pile pour chaque instance de l’appel de fonction.</span><span class="sxs-lookup"><span data-stu-id="00c56-135">In this case, memory is set aside on the stack for each instance of the function call.</span></span>
  
> [!NOTE]
> <span data-ttu-id="00c56-136">L’étendue de mémoire allouée dynamiquement dépend de l’étendue du pointeur qui pointe vers lui : si le pointeur est accessible par tous les threads, la mémoire est également.</span><span class="sxs-lookup"><span data-stu-id="00c56-136">The scope of dynamically allocated memory depends on the scope of the pointer that points to it: if the pointer is accessible by all threads, the memory is also.</span></span> <span data-ttu-id="00c56-137">Si le pointeur est une variable automatique dans une fonction, la mémoire allouée est efficacement privée ce thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-137">If the pointer is an automatic variable in a function, the allocated memory is effectively private to that thread.</span></span> 
  
## <a name="memory-accessible-by-only-one-thread-thread-local-memory"></a><span data-ttu-id="00c56-138">Mémoire Accessible par un seul Thread : mémoire locale de Thread</span><span class="sxs-lookup"><span data-stu-id="00c56-138">Memory Accessible by Only One Thread: Thread-Local Memory</span></span>

<span data-ttu-id="00c56-139">Étant donné que les variables statiques dans le corps d’une fonction sont accessibles par tous les threads, les fonctions qui les utilisent sont clairement pas thread-safe.</span><span class="sxs-lookup"><span data-stu-id="00c56-139">Given that static variables within the body of a function are accessible by all threads, functions that use them are clearly not thread safe.</span></span> <span data-ttu-id="00c56-140">Une seule instance de la fonction sur un thread peut modifier la valeur pendant une autre instance sur un autre thread est en partant du principe qu’il est complètement différent.</span><span class="sxs-lookup"><span data-stu-id="00c56-140">One instance of the function on one thread could be changing the value while another instance on another thread is assuming it is something completely different.</span></span> 
  
<span data-ttu-id="00c56-141">Il existe deux raisons pour déclarer des variables statiques au sein d’une fonction :</span><span class="sxs-lookup"><span data-stu-id="00c56-141">There are two reasons for declaring static variables within a function:</span></span>
  
1. <span data-ttu-id="00c56-142">Conserver des données statiques à partir d’un appel à la suivante.</span><span class="sxs-lookup"><span data-stu-id="00c56-142">Static data persist from one call to the next.</span></span>
    
2. <span data-ttu-id="00c56-143">Un pointeur vers les données statiques en toute sécurité peut être renvoyé par la fonction.</span><span class="sxs-lookup"><span data-stu-id="00c56-143">A pointer to static data can safely be returned by the function.</span></span>
    
<span data-ttu-id="00c56-144">Dans le cas de première raison, vous voudrez peut-être des données qui est conservée et a de signification pour tous les appels à la fonction : par exemple un compteur simple qui est incrémenté à chaque fois que la fonction est appelée sur n’importe quel thread, ou une structure qui collecte les données d’utilisation et performances veille appel Ry.</span><span class="sxs-lookup"><span data-stu-id="00c56-144">In the case of first reason, you might want to have data that persists and has meaning for all calls to the function: perhaps a simple counter that is incremented every time the function is called on any thread, or a structure that collects usage and performance data on every call.</span></span> <span data-ttu-id="00c56-145">La question est comment protéger les données partagées ou la structure de données.</span><span class="sxs-lookup"><span data-stu-id="00c56-145">The question is how to protect the shared data or data structure.</span></span> <span data-ttu-id="00c56-146">Mieux, cela s’effectue à l’aide de section critique comme l’explique la section suivante.</span><span class="sxs-lookup"><span data-stu-id="00c56-146">This is best done by using critical section as the next section explains.</span></span>
  
<span data-ttu-id="00c56-147">Si les données sont destinées uniquement à ce thread, qui peut être le cas pour la raison 1 et est toujours le cas pour la raison 2, la question est la création de mémoire qui persiste, mais n’est pas accessible à partir de ce thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-147">If the data is intended only for use by this thread, which could be the case for reason 1 and is always the case for reason 2, the question is how to create memory that persists but is only accessible from this thread.</span></span> <span data-ttu-id="00c56-148">Une solution consiste à utiliser le stockage local des threads (TLS) API.</span><span class="sxs-lookup"><span data-stu-id="00c56-148">One solution is to use the thread-local storage (TLS) API.</span></span>
  
<span data-ttu-id="00c56-149">Par exemple, imaginons une fonction qui retourne un pointeur vers un **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="00c56-149">For example, consider a function that returns a pointer to an **XLOPER**.</span></span>
  
```cs
LPXLOPER12 WINAPI mtr_unsafe_example(LPXLOPER12 pxArg)
{
    static XLOPER12 xRetVal; // memory shared by all threads!!!
// code sets xRetVal to a function of pxArg ...
    return &xRetVal;
}
```

<span data-ttu-id="00c56-150">Cette fonction n’est pas thread-safe car un thread peut renvoyer l' statique **XLOPER12** tandis que l’autre est le remplacement.</span><span class="sxs-lookup"><span data-stu-id="00c56-150">This function is not thread safe because one thread can return the static **XLOPER12** while another is overwriting it.</span></span> <span data-ttu-id="00c56-151">La probabilité de ce problème est accrue si le **XLOPER12** doit être transmis à **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="00c56-151">The likelihood of this happening is greater still if the **XLOPER12** needs to be passed to **xlAutoFree12**.</span></span> <span data-ttu-id="00c56-152">Une solution consiste à allouer un **XLOPER12**, retourner un pointeur et implémenter **xlAutoFree12** afin que la mémoire **XLOPER12** elle-même est libérée.</span><span class="sxs-lookup"><span data-stu-id="00c56-152">One solution is to allocate an **XLOPER12**, return a pointer to it, and implement **xlAutoFree12** so that the **XLOPER12** memory itself is freed.</span></span> <span data-ttu-id="00c56-153">Cette approche est utilisée dans la plupart des fonctions exemple indiquées dans la [Gestion de la mémoire dans Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="00c56-153">This approach is used in many of the example functions shown in [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
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

<span data-ttu-id="00c56-154">Cette approche est plus simple à implémenter que celle décrite dans la section suivante, qui repose sur l’API TLS, mais elle présente des inconvénients.</span><span class="sxs-lookup"><span data-stu-id="00c56-154">This approach is simpler to implement than the approach outlined in the next section, which relies on the TLS API, but it has some disadvantages.</span></span> <span data-ttu-id="00c56-155">Tout d’abord, Excel doit appeler **xlAutoFree**/ **xlAutoFree12** quel que soit le type de l' renvoyée **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="00c56-155">First, Excel must call **xlAutoFree**/ **xlAutoFree12** whatever the type of the returned **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="00c56-156">Deuxièmement, un problème est survenu lors de la réponse **XLOPER**/ s**XLOPER12**qui correspondent à la valeur de retour d’un appel à une fonction de rappel API C.</span><span class="sxs-lookup"><span data-stu-id="00c56-156">Second, there is a problem when returning **XLOPER**/ **XLOPER12**s that are the return value of a call to a C API callback function.</span></span> <span data-ttu-id="00c56-157">Le **XLOPER**/ **XLOPER12** peuvent pointer vers la mémoire doit être libérée par Excel, mais le **XLOPER**/ **XLOPER12** lui-même doit être libérée de la même manière qu’il a été attribué.</span><span class="sxs-lookup"><span data-stu-id="00c56-157">The **XLOPER**/ **XLOPER12** may point to memory that needs to be freed by Excel, but the **XLOPER**/ **XLOPER12** itself must be freed in the same way it was allocated.</span></span> <span data-ttu-id="00c56-158">Si ces un **XLOPER**/ **XLOPER12** doit être utilisée comme valeur de retour d’une fonction de feuille de calcul XLL, il n’existe aucun moyen simple d’informer **xlAutoFree**/ **xlAutoFree12** de la nécessité de libérer les deux pointeurs de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="00c56-158">If such an **XLOPER**/ **XLOPER12** is to be used as the return value of an XLL worksheet function, there is no easy way to inform **xlAutoFree**/ **xlAutoFree12** of the need to free both pointers in the appropriate way.</span></span> <span data-ttu-id="00c56-159">(Définition **xlbitXLFree** et **xlbitDLLFree** ne résout pas le problème, comme le traitement de **XLOPER/XLOPER12s** dans Excel avec la valeur n’est pas défini et peut changer d’une version à l’autre.) Pour contourner ce problème, la ressource XLL permettre rendre des copies complètes de tous les allouée Excel **XLOPER/XLOPER12s** qu’elle renvoie à la feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="00c56-159">(Setting both the **xlbitXLFree** and **xlbitDLLFree** does not solve the problem, as the treatment of **XLOPER/XLOPER12s** in Excel with both set is undefined and might change from version to version.) To work around this problem, the XLL can make deep copies of all Excel-allocated **XLOPER/XLOPER12s** that it returns to the worksheet.</span></span> 
  
<span data-ttu-id="00c56-160">Pour éviter ces limitations consiste à remplir et renvoyer un thread **local/XLOPER12 XLOPER**, une approche qui nécessite que **xlAutoFree/xlAutoFree12** ne la libère pas le pointeur **XLOPER/XLOPER12** lui-même.</span><span class="sxs-lookup"><span data-stu-id="00c56-160">A solution that avoids these limitations is to populate and return a thread-local **XLOPER/XLOPER12**, an approach that necessitates that **xlAutoFree/xlAutoFree12** does not free the **XLOPER/XLOPER12** pointer itself.</span></span> 
  
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

<span data-ttu-id="00c56-161">La question suivante est comment configurer et récupérer la mémoire locale de thread, en d’autres termes, comment implémenter la fonction **get_thread_local_xloper12** dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="00c56-161">The next question is how to set up and retrieve the thread-local memory, in other words, how to implement the function **get_thread_local_xloper12** in the previous example.</span></span> <span data-ttu-id="00c56-162">Cette opération est effectuée à l’aide du stockage TLS (Thread Local) API.</span><span class="sxs-lookup"><span data-stu-id="00c56-162">This is done using the Thread Local Storage (TLS) API.</span></span> <span data-ttu-id="00c56-163">La première étape consiste à obtenir un index TLS à l’aide de **TlsAlloc**, qui doit être libéré à l’aide de **TlsFree**.</span><span class="sxs-lookup"><span data-stu-id="00c56-163">The first step is to obtain a TLS index by using **TlsAlloc**, which must ultimately be released using **TlsFree**.</span></span> <span data-ttu-id="00c56-164">Les deux sont effectuées depuis **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="00c56-164">Both are best accomplished from **DllMain**.</span></span>
  
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

<span data-ttu-id="00c56-165">Après avoir obtenu l’index, l’étape suivante consiste à allouer un bloc de mémoire pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-165">After you obtain the index, the next step is to allocate a block of memory for each thread.</span></span> <span data-ttu-id="00c56-166">La [Documentation de développement Windows](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) recommande cette opération chaque fois que la fonction de rappel **DllMain** est appelée avec un événement **DLL_THREAD_ATTACH** et libérer la mémoire sur chaque **DLL_THREAD_DETACH**.</span><span class="sxs-lookup"><span data-stu-id="00c56-166">The [Windows Development Documentation](http://msdn.microsoft.com/en-us/library/ms682583%28VS.85%29.aspx) recommends doing this every time the **DllMain** callback function is called with a **DLL_THREAD_ATTACH** event, and freeing the memory on every **DLL_THREAD_DETACH**.</span></span> <span data-ttu-id="00c56-167">Toutefois, ce Conseil serait entraîner votre DLL faire inutiles pour les threads non utilisé pour le recalcul.</span><span class="sxs-lookup"><span data-stu-id="00c56-167">However, following this advice would cause your DLL to do unnecessary work for threads not used for recalculation.</span></span> 
  
<span data-ttu-id="00c56-168">Au lieu de cela, il est préférable d’utiliser une stratégie d’affecter à la première utilisation.</span><span class="sxs-lookup"><span data-stu-id="00c56-168">Instead, it is better to use an allocate-on-first-use strategy.</span></span> <span data-ttu-id="00c56-169">Tout d’abord, vous devez définir une structure que vous souhaitez allouer pour chaque thread.</span><span class="sxs-lookup"><span data-stu-id="00c56-169">First, you need to define a structure that you want to allocate for each thread.</span></span> <span data-ttu-id="00c56-170">Pour les exemples précédents qui renvoient **XLOPER** ou **XLOPER12s**, suffit suivantes, mais vous pouvez créer une structure répondant à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="00c56-170">For the previous examples that return **XLOPERs** or **XLOPER12s**, the following suffices, but you can create any structure that satisfies your needs.</span></span>
  
```cs
struct TLS_data
{
    XLOPER xloper_shared_ret_val;
    XLOPER12 xloper12_shared_ret_val;
// Add other required thread-local data here...
};
```

<span data-ttu-id="00c56-171">La fonction suivante obtient un pointeur vers l’instance locale de thread ou en alloue un s’il s’agit du premier appel.</span><span class="sxs-lookup"><span data-stu-id="00c56-171">The following function gets a pointer to the thread-local instance, or allocates one if this is the first call.</span></span>
  
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

<span data-ttu-id="00c56-172">Vous pouvez maintenant voir comment la mémoire **XLOPER/XLOPER12** locale de thread est obtenue : tout d’abord, vous obtenez un pointeur vers l’instance du thread de **TLS_data**, puis vous renvoyez un pointeur vers le **XLOPER/XLOPER12** contenues dans celui-ci, comme suit.</span><span class="sxs-lookup"><span data-stu-id="00c56-172">Now you can see how the thread-local **XLOPER/XLOPER12** memory is obtained: first, you get a pointer to the thread's instance of **TLS_data**, and then you return a pointer to the **XLOPER/XLOPER12** contained within it, as follows.</span></span> 
  
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

<span data-ttu-id="00c56-173">Les fonctions **mtr_safe_example_1** et **mtr_safe_example_2** peuvent être enregistrées en tant que les fonctions de feuille de calcul thread-safe lorsque vous exécutez Excel.</span><span class="sxs-lookup"><span data-stu-id="00c56-173">The **mtr_safe_example_1** and **mtr_safe_example_2** functions can be registered as thread-safe worksheet functions when you are running Excel.</span></span> <span data-ttu-id="00c56-174">Toutefois, vous ne pouvez pas mélanger les deux approches dans un XLL.</span><span class="sxs-lookup"><span data-stu-id="00c56-174">However, you cannot mix the two approaches in one XLL.</span></span> <span data-ttu-id="00c56-175">Votre XLL permettre exporter uniquement une implémentation de **xlAutoFree** et **xlAutoFree12**, et chaque stratégie de mémoire requiert une approche différente.</span><span class="sxs-lookup"><span data-stu-id="00c56-175">Your XLL can only export one implementation of **xlAutoFree** and **xlAutoFree12**, and each memory strategy requires a different approach.</span></span> <span data-ttu-id="00c56-176">Avec **mtr_safe_example_1**, le pointeur passé à **xlAutoFree/xlAutoFree12** doit être libéré avec toutes les données qu’il pointe vers.</span><span class="sxs-lookup"><span data-stu-id="00c56-176">With **mtr_safe_example_1**, the pointer passed to **xlAutoFree/xlAutoFree12** must be freed along with any data it points to.</span></span> <span data-ttu-id="00c56-177">Avec **mtr_safe_example_2**, uniquement les données désigné doivent être libérées.</span><span class="sxs-lookup"><span data-stu-id="00c56-177">With **mtr_safe_example_2**, only the pointed-to data should be freed.</span></span>
  
<span data-ttu-id="00c56-178">Windows fournit également une fonction **GetCurrentThreadId**, qui retourne l’ID unique au niveau du système. du thread courant</span><span class="sxs-lookup"><span data-stu-id="00c56-178">Windows also provides a function **GetCurrentThreadId**, which returns the current thread's unique system-wide ID.</span></span> <span data-ttu-id="00c56-179">Ainsi, le développeur avec une autre façon de sécuriser le thread de code, ou de passer son thread de comportement spécifique.</span><span class="sxs-lookup"><span data-stu-id="00c56-179">This provides the developer with another way to make code thread safe, or to make its behavior thread specific.</span></span>
  
## <a name="memory-accessible-only-by-more-than-one-thread-critical-sections"></a><span data-ttu-id="00c56-180">Mémoire Accessible uniquement par plusieurs threads : Sections critiques</span><span class="sxs-lookup"><span data-stu-id="00c56-180">Memory Accessible Only by More than One Thread: Critical Sections</span></span>

<span data-ttu-id="00c56-181">Vous devez protéger la mémoire en lecture-écriture qui est accessible par plusieurs threads utilisant des sections critiques.</span><span class="sxs-lookup"><span data-stu-id="00c56-181">You should protect read/write memory that can be accessed by more than one thread using critical sections.</span></span> <span data-ttu-id="00c56-182">Vous avez besoin d’une section critique nommé pour chaque bloc de mémoire que vous souhaitez protéger.</span><span class="sxs-lookup"><span data-stu-id="00c56-182">You need a named critical section for each block of memory you want to protect.</span></span> <span data-ttu-id="00c56-183">Vous pouvez initialiser pendant l’appel à la fonction **xlAutoOpen** et les libérer et leur attribuer la valeur null pendant l’appel à la fonction **xlAutoClose** .</span><span class="sxs-lookup"><span data-stu-id="00c56-183">You can initialize these during the call to the **xlAutoOpen** function, and release them and set them to null during the call to the **xlAutoClose** function.</span></span> <span data-ttu-id="00c56-184">Vous devez ensuite contenir chaque accès au bloc protégé au sein d’une paire d’appels à **EnterCriticalSection** et **LeaveCriticalSection**.</span><span class="sxs-lookup"><span data-stu-id="00c56-184">You then need to contain each access to the protected block within a pair of calls to **EnterCriticalSection** and **LeaveCriticalSection**.</span></span> <span data-ttu-id="00c56-185">Un seul thread est autorisé dans la section critique à tout moment.</span><span class="sxs-lookup"><span data-stu-id="00c56-185">Only one thread is permitted into the critical section at any time.</span></span> <span data-ttu-id="00c56-186">Voici un exemple de l’initialisation, désinitialisation et l’utilisation d’une section appelée **g_csSharedTable**.</span><span class="sxs-lookup"><span data-stu-id="00c56-186">Here is an example of the initialization, uninitialization, and use of a section called **g_csSharedTable**.</span></span>
  
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

<span data-ttu-id="00c56-187">Une autre, peut-être plus sûr de protéger un bloc de mémoire consiste à créer une classe qui contient sa propre **CRITICAL_SECTION** et dont constructeur, destructeur et prendre en charge les méthodes d’accesseurs de son utilisation.</span><span class="sxs-lookup"><span data-stu-id="00c56-187">Another, perhaps safer way of protecting a block of memory is to create a class that contains its own **CRITICAL_SECTION** and whose constructor, destructor, and accessor methods take care of its use.</span></span> <span data-ttu-id="00c56-188">Cette approche présente l’avantage de protéger les objets qui peuvent être initialisées avant **xlAutoOpen** est exécutée ou survivre après avoir appelé **xlAutoClose** , mais vous devez être attentif à la création de sections critiques trop et le système d’exploitation surcharge à créer.</span><span class="sxs-lookup"><span data-stu-id="00c56-188">This approach has the added advantage of protecting objects that may be initialized before **xlAutoOpen** is run, or survive after **xlAutoClose** is called, but you should be careful about creating too many critical sections and the operating system overhead that this would create.</span></span> 
  
<span data-ttu-id="00c56-189">Lorsque vous avez du code qui doit accéder à plusieurs blocs de mémoire protégés en même temps, vous devez prendre en compte soigneusement l’ordre dans lequel les sections critiques sont entrées et s’est arrêtées.</span><span class="sxs-lookup"><span data-stu-id="00c56-189">When you have code that needs access to more than one block of protected memory at the same time, you need to consider very carefully the order in which the critical sections are entered and exited.</span></span> <span data-ttu-id="00c56-190">Par exemple, les deux fonctions suivantes peuvent créer un blocage.</span><span class="sxs-lookup"><span data-stu-id="00c56-190">For example, the following two functions could create a deadlock.</span></span>
  
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

<span data-ttu-id="00c56-191">Si la première fonction sur un thread entre **g_csSharedTableA** alors que la seconde sur un autre thread passe **g_csSharedTableB**, les deux threads se bloquent.</span><span class="sxs-lookup"><span data-stu-id="00c56-191">If the first function on one thread enters **g_csSharedTableA** while the second on another thread enters **g_csSharedTableB**, both threads hang.</span></span> <span data-ttu-id="00c56-192">L’approche correcte consiste à entrer dans un ordre cohérent et quitter dans l’ordre inverse, comme suit.</span><span class="sxs-lookup"><span data-stu-id="00c56-192">The correct approach is to enter in a consistent order and exit in the reverse order, as follows.</span></span>
  
```cs
    EnterCriticalSection(&g_csSharedTableA);
    EnterCriticalSection(&g_csSharedTableB);
    // code that accesses both blocks
    LeaveCriticalSection(&g_csSharedTableB);
    LeaveCriticalSection(&g_csSharedTableA);
```

<span data-ttu-id="00c56-193">Si possible, il est préférable d’un thread coopération point de vue pour isoler l’accès aux blocs distincts, comme indiqué ici.</span><span class="sxs-lookup"><span data-stu-id="00c56-193">Where possible, it is better from a thread co-operation point of view to isolate access to distinct blocks, as shown here.</span></span>
  
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

<span data-ttu-id="00c56-194">Où il y a beaucoup de contention pour une ressource partagée, telles que les demandes d’accès de courte durée fréquents, vous devez envisager à l’aide de la section critique pour faire pivoter.</span><span class="sxs-lookup"><span data-stu-id="00c56-194">Where there is a lot of contention for a shared resource, such as frequent short-duration access requests, you should consider using the critical section's ability to spin.</span></span> <span data-ttu-id="00c56-195">Il s’agit d’une technique qui rend en attente de la ressource moins utilisation intensive du processeur.</span><span class="sxs-lookup"><span data-stu-id="00c56-195">This is a technique that makes waiting for the resource less processor-intensive.</span></span> <span data-ttu-id="00c56-196">Pour ce faire, vous pouvez utiliser soit **InitializeCriticalSectionAndSpinCount** lors de l’initialisation de la section ou le **SetCriticalSectionSpinCount** une fois initialisée, pour définir le nombre de fois que le thread effectue une boucle avant d’attendre de ressources Il est disponible.</span><span class="sxs-lookup"><span data-stu-id="00c56-196">To do this, you can use either **InitializeCriticalSectionAndSpinCount** when initializing the section or **SetCriticalSectionSpinCount** once initialized, to set the number of times the thread loops before waiting for resources to become available.</span></span> <span data-ttu-id="00c56-197">L’opération d’attente étant onéreuse, rotation permet de l’éviter si la ressource est libérée entre-temps.</span><span class="sxs-lookup"><span data-stu-id="00c56-197">The wait operation is expensive, so spinning avoids this if the resource is freed in the meantime.</span></span> <span data-ttu-id="00c56-198">Sur un système à processeur unique, le nombre de rotations est ignoré, mais vous pouvez toujours le spécifier sans nuire à toute l’entreprise.</span><span class="sxs-lookup"><span data-stu-id="00c56-198">On a single processor system, the spin count is effectively ignored, but you can still specify it without doing any harm.</span></span> <span data-ttu-id="00c56-199">Le Gestionnaire de segments de mémoire utilise un compteur de rotations de 4000.</span><span class="sxs-lookup"><span data-stu-id="00c56-199">The memory heap manager uses a spin count of 4000.</span></span> <span data-ttu-id="00c56-200">Pour plus d’informations sur l’utilisation de sections critiques, voir la documentation du SDK de Windows.</span><span class="sxs-lookup"><span data-stu-id="00c56-200">For more information about the use of critical sections, see the Windows SDK documentation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00c56-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c56-201">See also</span></span>



[<span data-ttu-id="00c56-202">Gestion de la m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="00c56-202">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="00c56-203">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="00c56-203">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="00c56-204">Gestionnaire de compléments et les fonctions de l’Interface XLL</span><span class="sxs-lookup"><span data-stu-id="00c56-204">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

