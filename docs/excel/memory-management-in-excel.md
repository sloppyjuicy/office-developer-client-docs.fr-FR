---
title: Gestion de la m�moire dans Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419540"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="3f03e-104">Gestion de la mémoire dans Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-104">Memory Management in Excel</span></span>

 <span data-ttu-id="3f03e-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f03e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f03e-p101">La gestion de la mémoire est l’élément le plus important à prendre en compte pour créer des XLL efficaces et stables. Un échec de la gestion de la mémoire peut entraîner différents problèmes dans Microsoft Excel, des problèmes mineurs tels qu’une initialisation et une allocation de mémoire inefficaces, ainsi que de petites pertes de mémoire ou des problèmes plus importants tels que la déstabilisation d’Excel.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="3f03e-p102">Une mauvaise gestion de la m�moire repr�sente la source la plus courante des probl�mes graves li�s aux compl�ments. Par cons�quent, vous devez g�n�rer votre projet avec une strat�gie de gestion de la m�moire coh�rente et bien �tudi�e.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="3f03e-p103">La gestion de la m�moire est devenue plus complexe dans Microsoft Office Excel�2007 avec l�introduction du recalcul de la feuille de calcul multithread. Si vous voulez cr�er et exporter des fonctions de feuille de calcul thread-safe, vous devez g�rer les conflits qui risquent de se produire lorsque plusieurs threads se disputent l�acc�s.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="3f03e-112">Certains �l�ments doivent �tre pris en compte au sujet de la m�moire pour les trois�types de structure de donn�es suivants�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="3f03e-113">**XLOPER** et **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="3f03e-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="3f03e-114">Les cha�nes qui ne sont pas dans une structure **XLOPER** ni dans une structure **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="3f03e-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="3f03e-115">Les tableaux **FP** et **FP12**</span><span class="sxs-lookup"><span data-stu-id="3f03e-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="3f03e-116">Mémoire XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="3f03e-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="3f03e-117">La structure de données **XLOPER**/ **XLOPER12** a plusieurs sous-types qui contiennent des pointeurs vers les blocs de mémoire, à savoir des chaînes (**xltypeStr**), des tableaux (**xltypeMulti**) et des références externes (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="3f03e-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="3f03e-118">En outre, les tableaux **xltypeMulti** peuvent contenir des éléments **XLOPER**/ **XLOPER12** de chaîne qui pointent ensuite vers d’autres blocs de mémoire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="3f03e-119">Une structure **XLOPER**/ **XLOPER12** peut �tre cr��e de diff�rentes mani�res�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="3f03e-120">Via Excel lors de la pr�paration des arguments � transmettre � une fonction XLL</span><span class="sxs-lookup"><span data-stu-id="3f03e-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="3f03e-121">Via Excel lors du renvoi d�une structure **XLOPER** ou **XLOPER12** dans un appel d�API C</span><span class="sxs-lookup"><span data-stu-id="3f03e-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="3f03e-122">Via votre DLL lors de la cr�ation des arguments � transmettre � un appel d�API C</span><span class="sxs-lookup"><span data-stu-id="3f03e-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="3f03e-123">Via votre DLL lors de la cr�ation d�une valeur de retour de la fonction XLL</span><span class="sxs-lookup"><span data-stu-id="3f03e-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="3f03e-124">Un bloc de m�moire dans l�un des types de pointage de m�moire peut �tre allou� de plusieurs fa�ons�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="3f03e-125">Il peut s�agir d�un bloc statique dans votre DLL, en dehors de tout code de fonction, auquel cas il est inutile d�allouer ou de lib�rer de la m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="3f03e-126">Il peut s�agir d�un bloc statique dans votre DLL, dans du code de fonction, auquel cas il est inutile d�allouer ou de lib�rer de la m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="3f03e-127">Il peut �tre allou� dynamiquement et lib�r� par votre DLL de plusieurs diff�rentes mani�res�: **malloc** et **free** **new** et **delete**, etc.</span><span class="sxs-lookup"><span data-stu-id="3f03e-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="3f03e-128">Il peut �tre allou� dynamiquement par Excel.</span><span class="sxs-lookup"><span data-stu-id="3f03e-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="3f03e-p105">�tant donn� le nombre d�origines possibles pour la m�moire **XLOPER**/ **XLOPER12** et le nombre de situations dans lesquelles cette m�moire peut avoir �t� affect�e � la structure **XLOPER**/ **XLOPER12**, il n�est pas surprenant que cet objet puisse sembler difficile. Toutefois, cette complexit� peut �tre consid�rablement r�duite si vous suivez plusieurs r�gles et recommandations.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p105">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="3f03e-131">Règles d’utilisation de XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="3f03e-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="3f03e-p106">Ne tentez pas de lib�rer de la m�moire ni de remplacer les structures **XLOPERs**/ **XLOPER12** transmises comme arguments vers votre fonction XLL. Vous devez consid�rer ces arguments comme �tant en lecture seule. Pour plus d�informations, consultez la rubrique � Renvoi de **XLOPER** ou **XLOPER12** par la modification des arguments actifs�� dans [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="3f03e-p106">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="3f03e-135">Si Excel a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** renvoy�e vers votre DLL dans un appel vers l�API C�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="3f03e-p107">Vous devez lib�rer de la m�moire lorsque vous n�avez plus besoin de la structure **XLOPER**/ **XLOPER12** � l�aide d�un appel vers [xlFree](xlfree.md). N�utilisez aucune autre m�thode, de lib�ration ou de suppression par exemple, pour lib�rer de la m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p107">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="3f03e-138">Si le type renvoy� est **xltypeMulti**, ne remplacez aucune structure **XLOPER**/ **XLOPER12** dans le tableau, surtout si elles contiennent des cha�nes, et surtout � l�emplacement o� vous essayez de remplacer une cha�ne.</span><span class="sxs-lookup"><span data-stu-id="3f03e-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="3f03e-139">Si vous voulez renvoyer la structure **XLOPER**/ **XLOPER12** vers Excel en tant que valeur de retour de votre fonction DLL, vous devez indiquer � Excel qu�il doit lib�rer de la m�moire lorsque vous avez termin�.</span><span class="sxs-lookup"><span data-stu-id="3f03e-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="3f03e-140">Vous devez uniquement appeler **xlFree** sur une structure **XLOPER**/ **XLOPER12** qui a �t� cr��e en tant que valeur de retour vers un appel d�API C.</span><span class="sxs-lookup"><span data-stu-id="3f03e-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="3f03e-141">Si votre DLL a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** que vous souhaitez renvoyer vers Excel en tant que valeur de retour de votre fonction DLL, vous devez indiquer � Excel que la DLL doit lib�rer de la m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="3f03e-142">Instructions pour la gestion de la mémoire</span><span class="sxs-lookup"><span data-stu-id="3f03e-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="3f03e-p108">Soyez cohérent au sein de la DLL quant à la méthode que vous utilisez pour allouer et libérer de la mémoire. Évitez de mélanger différentes méthodes. Une bonne approche consiste à placer la méthode que vous utilisez dans une classe de mémoire ou une structure, dans laquelle vous pouvez modifier la méthode utilisée sans modifier votre code à de nombreux endroits.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="3f03e-p109">Lorsque vous cr�ez des tableaux **xltypeMulti** dans votre DLL, soyez coh�rent dans la m�thode utilis�e pour allouer de la m�moire pour les cha�nes�: allouez toujours la m�moire dynamiquement ou utilisez toujours la m�moire statique. Ainsi, lorsque vous lib�rez de la m�moire, vous savez si vous devez toujours, ou jamais, lib�rer les cha�nes.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="3f03e-148">Effectuez des copies compl�tes de la m�moire allou�e par Excel lorsque vous copiez une structure **XLOPER**/ **XLOPER12** cr��e dans Excel.</span><span class="sxs-lookup"><span data-stu-id="3f03e-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="3f03e-p110">Ne placez pas des structures **XLOPER**/ **XLOPER12** de chaîne allou�e par Excel dans des tableaux **xltypeMulti**. Effectuez une copie compl�te des chaînes et stockez des pointeurs vers les copies dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p110">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="3f03e-151">Libérer de la mémoire XLOPER/XLOPER12 allouée par Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="3f03e-152">Utilisez la commande XLL, qui se sert de **xlGetName** pour obtenir une cha�ne contenant le chemin d�acc�s et le nom de fichier de la DLL, et qui affiche ces informations dans une bo�te de dialogue d�alerte � l�aide de **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="3f03e-153">Lorsque la fonction n�a plus besoin de la m�moire vers laquelle pointe **xDllName**, elle peut la lib�rer � l�aide d�un appel vers la [fonction xlFree](xlfree.md), l�une des fonctions d�API C pour DLL uniquement.</span><span class="sxs-lookup"><span data-stu-id="3f03e-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="3f03e-154">La fonction **xlFree** est d�crite en d�tail dans la section des r�f�rences de fonction (voir [Fonctions de l�API�C qui peuvent �tre appel�es uniquement � partir d�une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mais tenez compte des �l�ments suivants�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="3f03e-155">Vous pouvez transmettre les pointeurs vers plusieurs **XLOPER**/ **XLOPER12** dans un appel unique vers **xlFree**, la seule limite �tant le nombre d�arguments de fonction pris en charge dans la version d�Excel en cours d�ex�cution (30 dans Excel 2003, 255 � partir de Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="3f03e-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="3f03e-p111">**xlFree** d�finit le pointeur contenu vers **NULL** pour s�assurer qu�une tentative de lib�ration d�une structure **XLOPER**/ **XLOPER12** qui a d�j� �t� lib�r�e est s�curis�e. **xlFree** est la seule fonction d�API C qui modifie ses arguments.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p111">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="3f03e-158">Vous pouvez appeler en toute s�curit� **xlFree** sur n�importe quelle structure **XLOPER**/ **XLOPER12** utilis�e pour la valeur de retour d�un appel de l�API C, ind�pendamment du fait qu�elle contienne ou non un pointeur vers la m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="3f03e-159">Renvoi des XLOPER/XLOPER12 à libérer via Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="3f03e-p112">Supposons que vous vouliez modifier l�exemple de commande dans la section pr�c�dente et la remplacer par une fonction de feuille de calcul qui renvoie le chemin d�acc�s et le nom de fichier de DLL lorsqu�un argument **Boolean** **true** est transmis, et **#N/A** dans le cas contraire. Vous ne pouvez clairement pas appeler **xlFree** pour lib�rer la m�moire de cha�ne avant son renvoi vers Excel. Toutefois, si elle n�est pas lib�r�e � un moment donn�, le compl�ment perd de la m�moire chaque fois que la fonction est appel�e. Pour contourner ce probl�me, vous pouvez d�finir un bit dans le champ **xltype** de la structure **XLOPER**/ **XLOPER12**, d�fini comme **xlbitXLFree** dans xlcall.h. Cela indique � Excel qu�il doit lib�rer la m�moire renvoy�e lorsqu�il a termin� la copie de la valeur.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="3f03e-165">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f03e-165">Example</span></span>

<span data-ttu-id="3f03e-166">L’exemple de code suivant illustre la commande XLL de la section précédente convertie en une fonction de feuille de calcul XLL.</span><span class="sxs-lookup"><span data-stu-id="3f03e-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="3f03e-p113">Les fonctions XLL qui utilisent **XLOPER**/ **XLOPER12** doivent �tre d�clar�es comme prenant et renvoyant des pointeurs vers **XLOPER**/ **XLOPER12**. L�utilisation dans cet exemple d�une structure **XLOPER12** statique au sein de la fonction n�est pas thread-safe. Vous pouvez inscrire incorrectement cette fonction en tant que thread-safe, mais vous risqueriez de remplacer **xRtnValue** par un thread avant qu�un autre thread ne soit termin� pour cette fonction.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p113">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="3f03e-p114">Vous devez d�finir **xlbitXLFree** apr�s l�appel vers le rappel Excel qui l�alloue. Si vous le d�finissez avant, il est remplac� et n�a pas l�effet voulu. Si vous avez l�intention d�utiliser cette valeur comme un argument dans un appel vers une autre fonction d�API C avant de la renvoyer vers la feuille de calcul, vous devez d�finir ce bit apr�s un appel de ce type. Dans le cas contraire, vous confondrez les fonctions qui ne masquent pas ce bit avant de v�rifier le type de **XLOPER**/ **XLLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p114">You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="3f03e-174">Renvoi des XLOPER/XLOPER12 à libérer via la DLL</span><span class="sxs-lookup"><span data-stu-id="3f03e-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="3f03e-p115">Un probl�me semblable � celui-ci se produit lorsque votre XLL a allou� de la m�moire pour une structure **XLOPER**/ **XLOPER12** et souhaite la renvoyer vers Excel. Excel reconna�t un autre bit qui peut �tre d�fini dans le champ **xltype** de la structure **XLOPER**/ **XLOPER12**, d�fini comme **xlbitDLLFree** dans xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p115">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="3f03e-p116">Lorsqu�Excel re�oit **an XLOPER**/ **XLOPER12** avec ce bit d�fini, il essaie d�appeler une fonction qui doit �tre export�e par la XLL appel�e [xlAutoFree ](xlautofree-xlautofree12.md) (pour les **XLOPER**) ou **xlAutoFree12** (pour les **XLOPER12**). Cette fonction est d�crite plus en d�tail dans la r�f�rence de la fonction (voir [Gestionnaire de compl�ments et les fonctions de l'Interface XLL](add-in-manager-and-xll-interface-functions.md)), mais un exemple d�impl�mentation minimale est indiqu� ici. Son but est de lib�rer la m�moire **XLOPER**/ **XLOPER12** de fa�on coh�rente avec la mani�re dont elle a �t� allou�e � l�origine.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p116">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="3f03e-180">Exemples</span><span class="sxs-lookup"><span data-stu-id="3f03e-180">Examples</span></span>

<span data-ttu-id="3f03e-181">L�exemple de fonction suivant a le m�me r�sultat que la fonction pr�c�dente, sauf qu�elle inclut le texte ��Le chemin d�acc�s complet de cette DLL est�� avant le nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="3f03e-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="3f03e-182">Une impl�mentation minimale suffisante de **xlAutoFree12** dans la XLL qui a export� la fonction pr�c�dente se pr�sente comme suit.</span><span class="sxs-lookup"><span data-stu-id="3f03e-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="3f03e-p117">Cette impl�mentation est uniquement suffisante si la XLL renvoie uniquement des cha�nes **XLOPER12**, et que ces cha�nes sont uniquement allou�es � l�aide de **malloc**. Notez que le test</span><span class="sxs-lookup"><span data-stu-id="3f03e-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="3f03e-185">�chouerait dans ce cas car **xlbitDLLFree** est d�fini.</span><span class="sxs-lookup"><span data-stu-id="3f03e-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="3f03e-186">En g�n�ral, **xlAutoFree** et **xlAutoFree12** doivent �tre impl�ment�s afin qu�ils lib�rent de la m�moire associ�e aux tableaux **xltypeMulti** cr��s via XLL et aux r�f�rences externes **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="3f03e-p118">Vous pouvez d�cider d�impl�menter vos fonctions XLL afin qu�elles renvoient toutes les structures **XLOPER** et **XLOPER12** allou�es dynamiquement. Dans ce cas, vous devez d�finir **xlbitDLLFree** sur toutes ces **XLOPER** et **XLOPER12**, ind�pendamment du sous-type. Vous devez �galement impl�menter **xlAutoFree** et **xlAutoFree12** afin que cette m�moire soit lib�r�e, ainsi que la m�moire qui est vis�e par le pointeur dans la structure **XLOPER**/ **XLOPER12**. Cette approche est une fa�on de garantir que la valeur de retour est thread-safe. Par exemple, la fonction pr�c�dente peut �tre r��crite comme suit.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p118">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="3f03e-192">Pour plus d�informations sur **xlAutoFree** et **xlAutoFree12**, consultez [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="3f03e-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="3f03e-193">Renvoyer des arguments actifs à modifier</span><span class="sxs-lookup"><span data-stu-id="3f03e-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="3f03e-p119">Excel permet à une fonction XLL de renvoyer une valeur en modifiant un argument actif. Ceci est possible uniquement avec un argument transmis en tant que pointeur. Pour cela, la fonction doit être inscrite dans une méthode qui indique à Excel l’argument qui sera modifié.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="3f03e-197">Cette m�thode de renvoi d�une valeur est prise en charge pour tous les types de donn�es pouvant �tre transmis par le pointeur mais est particuli�rement utile pour les types suivants�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="3f03e-198">Cha�nes d�octets ASCII de longueur compt�e et se terminant par null</span><span class="sxs-lookup"><span data-stu-id="3f03e-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="3f03e-199">Cha�nes de caract�res larges Unicode de longueur compt�e et se terminant par null (d�marrage dans Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="3f03e-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="3f03e-200">Tableaux **FP** � virgule flottante</span><span class="sxs-lookup"><span data-stu-id="3f03e-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="3f03e-201">Tableaux **FP12** � virgule flottante (d�marrage dans Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="3f03e-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3f03e-p120">[!REMARQUE] Vous ne devriez pas essayer de renvoyer des **XLOPER** ou des **XLOPER12** de telle mani�re. Pour plus d�informations, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="3f03e-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="3f03e-p121">L�avantage de cette technique, plut�t que d�utiliser simplement l�instruction de renvoi, est qu�Excel alloue la m�moire pour les valeurs de retour. Une fois qu�Excel a fini de lire les donn�es renvoy�es, il lib�re la m�moire. Cela place les t�ches de gestion de la m�moire en dehors de la fonction XLL. Cette technique est thread-safe�: si elle est appel�e simultan�ment par Excel sur diff�rents threads, chaque appel de fonction sur chaque thread poss�de sa propre m�moire tampon.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="3f03e-p122">Cette technique est utile en particulier pour les types de donn�es r�pertori�es, car le m�canisme de rappel dans la DLL pour lib�rer de la m�moire apr�s le renvoi qui existe pour **XLOPER**/ **XLOPER12** n�existe pas pour les cha�nes simples ni pour les tableaux **FP**/ **FP12**. Par cons�quent, lors du renvoi d�une cha�ne cr��e par la DLL ou un tableau � virgule flottante, les choix suivants s�offrent � vous�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-p122">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="3f03e-p123">D�finissez un pointeur permanent vers une m�moire tampon allou�e dynamiquement, renvoyez le pointeur. Lors du prochain appel vers la fonction, (1) v�rifiez que le pointeur n�est pas null, (2) lib�rez les ressources allou�es � l�appel pr�c�dent et r�tablissez le pointeur sur null, et (3) r�utilisez le pointeur pour un bloc de m�moire nouvellement allou�.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="3f03e-212">Cr�ez des cha�nes et des tableaux dans une m�moire tampon statique ne n�cessitant pas d��tre lib�r�e et renvoyez un pointeur vers celle-ci.</span><span class="sxs-lookup"><span data-stu-id="3f03e-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="3f03e-213">Modifiez un argument actif, �crivez votre cha�ne ou votre tableau directement dans l�espace utilis� par Excel.</span><span class="sxs-lookup"><span data-stu-id="3f03e-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="3f03e-214">Dans le cas contraire, vous devez cr�er une structure **XLOPER**/ **XLOPER12** et utiliser **xlbitDLLFree** et **xlAutoFree**/ **xlAutoFree12** pour lib�rer les ressources.</span><span class="sxs-lookup"><span data-stu-id="3f03e-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="3f03e-p124">La derni�re option est peut-�tre la plus simple lorsque vous transmettez un argument du m�me type que la valeur de retour. Le point essentiel � retenir est le suivant : les tailles de m�moire tampon sont limit�es et vous devez veiller � ne pas les saturer. Le non-respect de cette consigne peut entra�ner une panne d�Excel. Les tailles de la m�moire tampon pour les chaînes et les tableaux **FP**/ **FP12** sont trait�es plus loin.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p124">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="3f03e-219">Strings</span><span class="sxs-lookup"><span data-stu-id="3f03e-219">Strings</span></span>

<span data-ttu-id="3f03e-220">Les problèmes liés à la gestion de la mémoire de chaîne sont sans doute la cause la plus courante d’instabilité dans les applications et les compléments. Cela peut être compréhensible, étant donné les diverses manières selon lesquelles les chaînes sont traitées : terminées par null ou de longueur comptée (ou les deux) ; mémoires tampons statiques ou dynamiques ; longueur fixe ou longueur presque illimitée ; mémoire gérée par le système d’exploitation (par exemple, OLE Bstr) ou chaînes non gérées ; etc.</span><span class="sxs-lookup"><span data-stu-id="3f03e-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="3f03e-p125">Les programmeurs C/C++ rencontrent souvent des cha�nes termin�es par null. La biblioth�que C standard est con�ue pour fonctionner avec ce type de cha�ne. Les litt�raux de cha�ne statique dans le code sont compil�s dans des cha�nes termin�es par null. Sinon, Excel fonctionne avec des cha�nes de longueur compt�e qui en g�n�ral ne sont pas termin�es par null. La combinaison de ces aspects requiert une approche claire et coh�rente dans votre DLL/XLL concernant la mani�re dont vous g�rez les cha�nes et la m�moire de cha�ne.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="3f03e-226">Les probl�mes les plus courants sont les suivants�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="3f03e-227">La transmission d�un pointeur null ou non valide vers une fonction qui attend un pointeur valide et qui ne v�rifie pas ou ne peut pas v�rifier la validit� du pointeur elle-m�me.</span><span class="sxs-lookup"><span data-stu-id="3f03e-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="3f03e-228">Le d�passement des limites d�une m�moire tampon de cha�ne par une fonction qui ne v�rifie pas ou ne peut pas v�rifier la longueur de la m�moire tampon par rapport � la longueur de la cha�ne en cours d��criture.</span><span class="sxs-lookup"><span data-stu-id="3f03e-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="3f03e-229">Une tentative de lib�ration de la m�moire tampon de cha�ne qui est statique, qui a d�j� �t� lib�r�e ou qui n��tait pas allou�e de fa�on coh�rente avec la mani�re dont elle est lib�r�e.</span><span class="sxs-lookup"><span data-stu-id="3f03e-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="3f03e-230">Des pertes de mémoire résultant de chaînes allouées et non libérées, généralement dans une fonction fréquemment appelée.</span><span class="sxs-lookup"><span data-stu-id="3f03e-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="3f03e-231">Règles pour les chaînes</span><span class="sxs-lookup"><span data-stu-id="3f03e-231">Rules for Strings</span></span>

<span data-ttu-id="3f03e-p126">Comme pour les structures **XLOPER**/ **XLOPER**, il existe des r�gles et des instructions � suivre. Les instructions sont les m�mes que celles �num�r�es dans la section pr�c�dente. Les r�gles d�crites ici sont une extension des r�gles propres aux chaînes.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p126">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="3f03e-235">**R�gles�:**</span><span class="sxs-lookup"><span data-stu-id="3f03e-235">**Rules:**</span></span>
  
- <span data-ttu-id="3f03e-p127">Ne tentez pas de lib�rer de la m�moire ou de remplacer une cha�ne **XLOPER**/ **XLOPER12** ou des cha�nes de longueur compt�e ou termin�es par null transmises comme arguments � la fonction de votre XLL. Vous devez consid�rer ces arguments comme �tant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p127">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="3f03e-238">Lorsque Excel alloue de la m�moire � une cha�ne **XLOPER**/ **XLOPER12** pour la valeur de retour d�une fonction de rappel API C, utilisez **xlFree** pour la lib�rer ou d�finissez **xlbitXLFree** si vous la renvoyez vers Excel � partir d�une fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="3f03e-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="3f03e-239">Lorsque votre DLL alloue dynamiquement une m�moire tampon de cha�ne pour une structure **XLOPER**/ **XLOPER12**, lib�rez-la de fa�on coh�rente avec la mani�re dont vous l�allouez une fois que vous avez termin� ou d�finissez **xlbitDLLFree** si vous la renvoyez vers Excel � partir d�une fonction XLL, puis lib�rez-la dans **xlAutoFree**/ **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="3f03e-p128">Si Excel a allou� la m�moire pour un tableau **xltypeMulti** renvoy� � votre DLL dans un appel d�API C, ne remplacez aucune cha�ne **XLOPER**/ **XLOPER12** dans le tableau. Ces tableaux doivent uniquement �tre lib�r�s � l�aide de **xlFree**, ou en cas de renvoi par une fonction XLL, par la d�finition de **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p128">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="3f03e-242">Types de chaîne pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f03e-242">String Types Supported</span></span>

<span data-ttu-id="3f03e-243">**API C xltypeStr XLOPER/XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="3f03e-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="3f03e-244">\*\*Cha�nes d�octets�: \*\*XLOPER\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3f03e-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="3f03e-245">\*\*Cha�nes de caract�res larges�: \*\*XLOPER12\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="3f03e-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f03e-246">Toutes les versions d�Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="3f03e-247">D�marrage dans Excel 2007</span><span class="sxs-lookup"><span data-stu-id="3f03e-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="3f03e-248">Longueur maximale�: 255�octets ASCII �tendus</span><span class="sxs-lookup"><span data-stu-id="3f03e-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="3f03e-249">Longueur maximale�: 32�767 caract�res Unicode</span><span class="sxs-lookup"><span data-stu-id="3f03e-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="3f03e-250">Le premier octet (non sign�) = longueur</span><span class="sxs-lookup"><span data-stu-id="3f03e-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="3f03e-251">Le premier caract�re Unicode = longueur</span><span class="sxs-lookup"><span data-stu-id="3f03e-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="3f03e-252">[!IMPORTANTE] Ne supposez pas que les cha�nes **XLOPER** ou **XLOPER12** se terminent par null.</span><span class="sxs-lookup"><span data-stu-id="3f03e-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="3f03e-253">**Cha�nes C/C++**</span><span class="sxs-lookup"><span data-stu-id="3f03e-253">**C/C++ strings**</span></span>

|<span data-ttu-id="3f03e-254">**Cha�nes d�octets**</span><span class="sxs-lookup"><span data-stu-id="3f03e-254">**Byte strings**</span></span>|<span data-ttu-id="3f03e-255">**Chaînes de caractères larges**</span><span class="sxs-lookup"><span data-stu-id="3f03e-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3f03e-256">Longueur maximale de l’élément « C » terminé par null (**char** \*) : 255 octets ASCII étendus</span><span class="sxs-lookup"><span data-stu-id="3f03e-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="3f03e-257">Longueur maximale de l’élément « C% » terminé par null (**wchar_t** \*) : 32 767 caractères Unicode</span><span class="sxs-lookup"><span data-stu-id="3f03e-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="3f03e-258">Longueur comptée (**char non signé** \*) : « D »</span><span class="sxs-lookup"><span data-stu-id="3f03e-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="3f03e-259">Longueur comptée ((**wchar_t** \*) \*) : « D % »</span><span class="sxs-lookup"><span data-stu-id="3f03e-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="3f03e-260">Chaînes dans les tableaux xltypeMulti XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="3f03e-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="3f03e-p129">Dans certains cas, Excel cr�e un tableau **xltypeMulti** � utiliser dans votre DLL/XLL. Plusieurs fonctions d�informations XLM renvoient ces tableaux. Par exemple, la fonction de l�API C **xlfGetWorkspace**, lorsque l�argument  *44*  est transmis, renvoie un tableau contenant des chaînes qui d�crivent toutes les proc�dures DLL actuellement inscrites. La fonction de l�API C **xlfDialogBox** renvoie une copie modifi�e de l�argument de tableau, contenant des copies compl�tes des chaînes. Une XLL rencontre peut-�tre le plus couramment un tableau **xltypeMulti** � l�endroit o� il a �t� transmis en tant qu�argument vers une fonction XLL, ou l� o� il a �t� converti en ce type � partir d�une r�f�rence de plage. Dans ce dernier cas, Excel cr�e des copies compl�tes des chaînes dans les cellules sources et pointe vers celles-ci dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="3f03e-p130">� l�endroit o� vous souhaitez modifier ces cha�nes dans votre DLL, vous devez effectuer vos propres copies compl�tes. Lorsque vous cr�ez vos propres tableaux **xltypeMulti**, vous ne devez pas placer la cha�ne allou�e par Excel **XLOPER**/ **XLOPER12**. Vous risquez ainsi de ne pas les lib�rer correctement ult�rieurement, ou de ne pas les lib�rer du tout. L� encore, vous devez effectuer des copies compl�tes des cha�nes et stocker des pointeurs vers les copies dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p130">Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="3f03e-271">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="3f03e-271">**Examples**</span></span>
  
<span data-ttu-id="3f03e-p131">La fonction de l�exemple suivant cr�e une copie d�une cha�ne Unicode de longueur compt�e allou�e dynamiquement. Notez que l�appelant doit finalement lib�rer la m�moire allou�e dans cet exemple � l�aide de **delete**[], et que la cha�ne source n�est pas suppos�e se terminer par null. La cha�ne de copie est tronqu�e si n�cessaire pour des raisons de s�curit� et ne se termine pas par null.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="3f03e-p132">Cette fonction peut ensuite �tre utilis�e en toute s�curit� pour copier une structure **XLOPER12**, comme indiqu� dans la fonction XLL exportable suivante qui renvoie une copie de l�argument s�il s�agit d�une chaîne. Tous les autres types sont renvoy�s comme une chaîne de longueur nulle. Notez que si les plages ne sont pas g�r�es, la fonction renvoie **#VALUE!**. La fonction doit �tre inscrite comme prenant un argument de type U afin que les r�f�rences soient transmises en tant que valeurs. Cela �quivaut � la fonction de feuille de calcul int�gr�e **T()**, sauf que **AsText** convertit �galement les erreurs en chaînes de longueur nulle. Cet exemple de code suppose que **xlAutoFree12** lib�re le pointeur transmis, ainsi que son contenu, � l�aide de **delete**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p132">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="3f03e-281">Renvoi d’arguments de chaîne actifs à modifier</span><span class="sxs-lookup"><span data-stu-id="3f03e-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="3f03e-p133">Les arguments inscrits en tant que types **F**, **G**, **F%** et **G%** peuvent �tre modifi�s en actifs. Quand Excel pr�pare les arguments de cha�ne pour ces types, il cr�e une m�moire tampon de longueur maximale. Il copie ensuite la cha�ne d�argument dans celle-ci, m�me si cette cha�ne est beaucoup plus courte. Ainsi, la fonction XLL peut �crire sa valeur de retour directement dans la m�me m�moire.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="3f03e-286">Les diff�rentes tailles de m�moire tampon pour ces types sont les suivantes�:</span><span class="sxs-lookup"><span data-stu-id="3f03e-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="3f03e-287">**Cha�nes d�octets�:** 256�octets, y compris de longueur compt�e (type G) ou termin�es par null (type F).</span><span class="sxs-lookup"><span data-stu-id="3f03e-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="3f03e-288">**Cha�nes Unicode�:** 32�768 caract�res larges (65�536 octets), y compris de longueur compt�e (type G�%) ou termin�es par null (type F�%).</span><span class="sxs-lookup"><span data-stu-id="3f03e-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="3f03e-p134">[!REMARQUE] Vous ne pouvez pas appeler une telle fonction directement � partir de Visual Basic pour Applications (VBA), car vous ne pouvez pas garantir qu�une m�moire tampon suffisamment large a �t� affect�e. Vous pouvez uniquement appeler une telle fonction � partir d�une autre DLL en toute s�curit� si vous avez explicitement transmis une m�moire tampon suffisamment large.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="3f03e-p135">Voici un exemple d�une fonction XLL qui annule une cha�ne de caract�res larges termin�e par null transmise � l�aide de la fonction de biblioth�que standard **wcsrev**. Dans ce cas, l�argument peut �tre inscrit en tant que type **F%**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="3f03e-293">Stockage permanent (noms binaires)</span><span class="sxs-lookup"><span data-stu-id="3f03e-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="3f03e-p136">Les noms binaires sont d�finis et associ�s � des blocs de donn�es binaires, autrement dit, non structur�es, qui sont stock�es avec la feuille de calcul. Ils sont cr��s � l�aide de la fonction [xlDefineBinaryName ](xldefinebinaryname.md) et les donn�es sont r�cup�r�es � l�aide de la fonction [xlGetBinaryName ](xlgetbinaryname.md). Les deux fonctions sont d�crites plus en d�tail dans la r�f�rence de la fonction (voir [Fonctions de l�API C qui peuvent �tre appel�es uniquement � partir d�une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)) et utilisent **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p136">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook. They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md). Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="3f03e-297">Pour plus d�informations sur les probl�mes connus qui limitent les applications pratiques des noms binaires, consultez [Probl�mes connus concernant le d�veloppement de XLL Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="3f03e-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="3f03e-298">Pile d’Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-298">Excel Stack</span></span>

<span data-ttu-id="3f03e-p137">Excel partage son espace de pile avec toutes les DLL chargées. L’espace de pile est généralement plus adapté à une utilisation ordinaire, et il est inutile de vous préoccuper tant que vous respectez les instructions suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f03e-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="3f03e-p138">Ne transmettez pas de tr�s grandes structures comme des arguments vers des fonctions par valeur sur la pile. Transmettez plut�t des pointeurs ou des r�f�rences.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="3f03e-p139">Ne renvoyez pas de grandes structures sur la pile. Renvoyez des pointeurs vers la m�moire allou�e de mani�re dynamique ou statique, ou utilisez les arguments transmis par r�f�rence.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="3f03e-p140">Ne d�clarez pas de tr�s grandes structures variables automatiques dans le code de la fonction. Si vous en avez besoin, d�clarez-les comme �tant statiques.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="3f03e-p141">N�appelez pas les fonctions de mani�re r�cursive, sauf si vous �tes s�r que la profondeur de r�cursivit� sera toujours faible. Essayez plut�t d�utiliser une boucle.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="3f03e-p142">Lorsqu�une DLL rappelle dans Excel � l�aide d�une API C, Excel v�rifie d�abord s�il y a suffisamment d�espace sur la pile pour l�appel d�utilisation le plus d�favorable pouvant �tre effectu�. S�il pense que l�espace est insuffisant, il fait �chouer l�appel pour des raisons de s�curit�, bien que l�espace puisse �tre suffisant pour cet appel en particulier. Dans ce cas, les rappels renvoient le code **xlretFailed**. Pour une utilisation ordinaire de l�API C et de la pile, il s�agit d�une cause d��chec d�un appel d�API C peu probable.</span><span class="sxs-lookup"><span data-stu-id="3f03e-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="3f03e-313">Si cela vous pr�occupe, si vous �tes simplement curieux ou si vous souhaitez �liminer le manque d�espace de pile comme raison d�un �chec inexpliqu�, vous pouvez conna�tre la quantit� d�espace de pile disponible par un appel de la fonction [xlStack](xlstack.md).</span><span class="sxs-lookup"><span data-stu-id="3f03e-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f03e-314">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f03e-314">See also</span></span>



[<span data-ttu-id="3f03e-315">Recalcul multithread dans Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="3f03e-316">Le multithreading et la Contention de m�moire dans Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="3f03e-317">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="3f03e-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

