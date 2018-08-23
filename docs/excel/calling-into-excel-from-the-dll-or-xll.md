---
title: Appel dans Excel à partir du fichier DLL ou XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- dialog boxes [excel 2007], invoking excel commands,DLLs [Excel 2007], calling into Excel,passing arguments to C API functions [Excel 2007],commands [Excel 2007], invoking with dialog boxes,commands [Excel 2007], accessible from DLL/XLL,Excel4 function [Excel 2007],Excel12 function [Excel 2007],XLCallVer function [Excel 2007],operRes argument [Excel 2007],functions [Excel 2007], accessible from DLL/XLL,Excel12v function [Excel 2007],DLL-only functions [Excel 2007],C API [Excel 2007], passing arguments,count argument [Excel 2007],commands [Excel 2007], calling in international versions,DLL-only commands [Excel 2007],international versions [Excel 2007], calling functions and commands,XLLs [Excel 2007], calling into Excel,Excel 4v function [Excel 2007],xlfn argument [Excel 2007],functions [Excel 2007], calling in international versions
localization_priority: Normal
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 996226aa8e01d58edbe9b9a8d6e6996b2453d581
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567705"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="19f0c-104">Appel dans Excel à partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="19f0c-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="19f0c-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="19f0c-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="19f0c-p101">Microsoft Excel permet � votre DLL d�acc�der aux commandes Excel int�gr�es, aux fonctions de feuille de calcul et aux fonctions de feuille de macro. Ces derni�res sont disponibles � partir des commandes et fonctions DLL appel�es � partir de Visual Basic pour Applications (VBA) ou des commandes et fonctions XLL appel�es directement par Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p101">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions. These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="19f0c-108">Fonctions Excel4, Excel4v, Excel12 et Excel12v</span><span class="sxs-lookup"><span data-stu-id="19f0c-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="19f0c-109">Excel permet � vos DLL d�acc�der aux commandes et fonctions au moyen des fonctions de rappel [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel 12](excel4-excel12.md) et [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="19f0c-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="19f0c-p102">Les fonctions **Excel4** et **Excel4v** ont �t� introduites dans Excel�4. Elles travaillent avec la structure de donn�es **XLOPER**. Excel 2007 a introduit deux nouvelles fonctions de rappel, **Excel12** et **Excel12v**, travaillant avec la structure de donn�es **XLOPER12**. Les fonctions **Excel4** et **Excel4v** sont export�es par la biblioth�que Xlcall32.lib, qui doit �tre incluse dans votre projet DLL ou XLL. **Excel12** et **Excel12v** sont inclus dans le fichier source C++ du SDK, Xlcall.cpp, devant �tre ins�r� dans votre projet si vous souhaitez acc�der aux fonctionnalit�s Excel � l�aide de structures **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p102">The **Excel4** and **Excel4v** functions were introduced in Excel version 4. They work with the **XLOPER** data structure. Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure. The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project. **Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="19f0c-p103">Le code suivant repr�sente les prototypes pour ces quatre fonctions. Les trois premiers arguments sont identiques, sauf que le deuxi�me argument est un pointeur vers une **XLOPER** dans la premi�re paire et un pointeur vers une **XLOPER12** dans la seconde paire. La convention d�appel est **_cdecl** dans **Excel4** et **Excel12** pour autoriser les listes d�arguments de variable. Les points de suspension repr�sentent les valeurs **XLOPER** pour **Excel4** et les valeurs **XLOPER12** pour **Excel12**. Le nombre de pointeurs est �gal � la valeur du param�tre  _count_.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p103">The following code shows the function prototypes for these four functions. The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair. The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists. The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**. The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="19f0c-120">**Toutes les versions d�Excel**</span><span class="sxs-lookup"><span data-stu-id="19f0c-120">**All versions of Excel**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="19f0c-121">**Introduit dans Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="19f0c-121">**Starting in Excel 2007**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="19f0c-p104">Pour que la DLL puisse appeler **Excel4**, **Excel4v**, **Excel12** ou **Excel12v**, Excel doit passer le contr�le � la DLL. Cela signifie que ces rappels d�API C peuvent �tre r�alis�s uniquement dans les sc�narios suivants :</span><span class="sxs-lookup"><span data-stu-id="19f0c-p104">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL. This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="19f0c-124">Depuis une commande XLL qu’Excel a appelée directement ou via VBA.</span><span class="sxs-lookup"><span data-stu-id="19f0c-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="19f0c-125">Depuis une feuille de calcul XLL ou une fonction de feuille de macro qu’Excel a appelée directement ou via VBA.</span><span class="sxs-lookup"><span data-stu-id="19f0c-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="19f0c-126">Vous ne pouvez pas appeler l’API C Excel dans les scénarios suivants :</span><span class="sxs-lookup"><span data-stu-id="19f0c-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="19f0c-127">� partir d�un �v�nement de systéme d�exploitation (par exemple, depuis la fonction [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)).</span><span class="sxs-lookup"><span data-stu-id="19f0c-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="19f0c-128">À partir d’un thread en arrière-plan créé par votre DLL.</span><span class="sxs-lookup"><span data-stu-id="19f0c-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="19f0c-129">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="19f0c-129">Return values</span></span>

<span data-ttu-id="19f0c-p105">Ces quatre fonctions renvoient un nombre entier qui indique � l�appelant si la fonction ou la commande a �t� correctement appel�e. Les valeurs renvoy�es peuvent faire partie des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="19f0c-p105">All four of these functions return an integer value that informs the caller whether the function or command was called successfully. The values returned can be any of the following:</span></span>
  
|<span data-ttu-id="19f0c-132">**Valeur renvoy�e**</span><span class="sxs-lookup"><span data-stu-id="19f0c-132">**Return value**</span></span>|<span data-ttu-id="19f0c-133">**D�finie dans Xlcall.h comme**</span><span class="sxs-lookup"><span data-stu-id="19f0c-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="19f0c-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="19f0c-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19f0c-135">0</span><span class="sxs-lookup"><span data-stu-id="19f0c-135">0</span></span>  <br/> |<span data-ttu-id="19f0c-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="19f0c-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="19f0c-p106">La fonction ou la commande a �t� ex�cut�e comme il se doit. Cela ne signifie pas que l�ex�cution �tait sans erreur. Par exemple, **Excel4** peut renvoyer **xlretSuccess** lors de l�appel de la fonction **FIND**, m�me si elle est �valu�e � **#VALUE!**, car le texte recherch� est introuvable. Vous devez examiner le type et la valeur de **XLOPER/XLOPER12** renvoy�e lorsque cela est possible.  </span><span class="sxs-lookup"><span data-stu-id="19f0c-p106">The function or command executed successfully. This does not mean that the execution was error free. For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!** because the search text could not be found. You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.  </span></span><br/> |
|<span data-ttu-id="19f0c-142">1</span><span class="sxs-lookup"><span data-stu-id="19f0c-142">1</span></span>  <br/> |<span data-ttu-id="19f0c-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="19f0c-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="19f0c-144">Une macro de commande a �t� arr�t�e par l�utilisateur en cliquant sur le bouton **ANNULER** ou en appuyant sur la touche �CHAP.</span><span class="sxs-lookup"><span data-stu-id="19f0c-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="19f0c-145">2</span><span class="sxs-lookup"><span data-stu-id="19f0c-145">2</span></span>  <br/> |<span data-ttu-id="19f0c-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="19f0c-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="19f0c-p107">La fonction ou le code de commande fourni n�est pas valide. Cette erreur peut se produire lorsque la fonction d�appel n�est pas autoris�e � appeler la fonction ou la commande. Par exemple, une fonction de feuille de calcul ne peut pas appeler une fonction d�information feuille macro ou une fonction de commande.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p107">The supplied function or command code is not valid. This error can occur when the calling function does not have permission to call the function or command. For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="19f0c-150">4</span><span class="sxs-lookup"><span data-stu-id="19f0c-150">4</span></span>  <br/> |<span data-ttu-id="19f0c-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="19f0c-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="19f0c-152">Le nombre d’arguments fourni n’est pas correct dans l’appel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="19f0c-153">8</span><span class="sxs-lookup"><span data-stu-id="19f0c-153">8</span></span>  <br/> |<span data-ttu-id="19f0c-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="19f0c-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="19f0c-155">Une ou plusieurs valeurs d�argument **XLOPER** ou **XLOPER12** ne sont pas correctement mises en forme ou remplies.</span><span class="sxs-lookup"><span data-stu-id="19f0c-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="19f0c-156">16</span><span class="sxs-lookup"><span data-stu-id="19f0c-156">16</span></span>  <br/> |<span data-ttu-id="19f0c-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="19f0c-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="19f0c-158">Excel a détecté un risque que l’opération dépasse sa pile d’appels et, par conséquent, ne puisse pas appeler la fonction.</span><span class="sxs-lookup"><span data-stu-id="19f0c-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="19f0c-159">32</span><span class="sxs-lookup"><span data-stu-id="19f0c-159">32</span></span>  <br/> |<span data-ttu-id="19f0c-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="19f0c-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="19f0c-p108">La commande ou la fonction a �chou� pour une raison qui n�est pas d�crite par une des autres valeurs de retour. Une op�ration qui n�cessite trop de m�moire, par exemple, �choue avec l�erreur suivante. Cela peut se produire pendant la tentative de conversion d�une référence tr�s volumineuse � un tableau **xltypeMulti** � l�aide de la fonction [xlCoerce](xlcoerce.md).  </span><span class="sxs-lookup"><span data-stu-id="19f0c-p108">The command or function failed for a reason not described by one of the other return values. An operation that would require too much memory, for example, would fail with this error. This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.  </span></span><br/> |
|<span data-ttu-id="19f0c-164">64</span><span class="sxs-lookup"><span data-stu-id="19f0c-164">64</span></span>  <br/> |<span data-ttu-id="19f0c-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="19f0c-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="19f0c-p109">L�op�ration a tent� de r�cup�rer la valeur d�une cellule non calcul�e. Pour pr�server l�int�grit� de recalcul dans Excel, les fonctions de feuille de calcul ne sont pas autoris�es � effectuer cette action. Toutefois, les fonctions et commandes XLL enregistr�es en tant que fonctions macro sont autoris�es � acc�der aux valeurs des cellules non calcul�es.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p109">The operation attempted to retrieve the value of an uncalculated cell. To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this. However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="19f0c-169">128</span><span class="sxs-lookup"><span data-stu-id="19f0c-169">128</span></span>  <br/> |<span data-ttu-id="19f0c-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="19f0c-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="19f0c-p110">(Introduit dans Excel 2007) Une fonction de feuille de calcul XLL enregistr�e en tant que fonction thread-safe essayait d�appeler une fonction d�API C non thread-safe. Par exemple, une fonction thread-safe ne peut pas appeler la fonction XLM **xlfGetCell**.  </span><span class="sxs-lookup"><span data-stu-id="19f0c-p110">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe. For example, a thread-safe function cannot call the XLM function **xlfGetCell**.  </span></span><br/> |
|<span data-ttu-id="19f0c-173">256</span><span class="sxs-lookup"><span data-stu-id="19f0c-173">256</span></span>  <br/> |<span data-ttu-id="19f0c-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="19f0c-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="19f0c-175">(Introduit dans Excel 2010) Le pointeur de fonction asynchrone n�est pas valide.</span><span class="sxs-lookup"><span data-stu-id="19f0c-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="19f0c-176">512</span><span class="sxs-lookup"><span data-stu-id="19f0c-176">512</span></span>  <br/> |<span data-ttu-id="19f0c-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="19f0c-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="19f0c-178">(Introduit dans Excel 2010) L�appel n�est pas pris en charge sur les clusters.</span><span class="sxs-lookup"><span data-stu-id="19f0c-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="19f0c-p111">Si la fonction renvoie une des valeurs d��chec de la table (autrement dit, elle ne renvoie pas **xlretSuccess**), la valeur de retour **XLOPER** ou **XLOPER12** est �galement d�finie sur **#VALUE!**. Dans certains cas, il peut s�agir d�un test de r�ussite suffisant, mais vous remarquerez qu�un appel peut renvoyer � la fois **xlretSuccess** et **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p111">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**. In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="19f0c-181">Si un appel de l�API C entra�ne **xlretUncalced** ou **xlretAbort**, votre code DLL ou XLL doit rendre la main � Excel avant d�effectuer les autres appels d�API C (autres que les appels vers la fonction [xlfree](xlfree.md) pour lib�rer des ressources m�moire Excel allou�es dans les valeurs **XLOPER** et **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="19f0c-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="19f0c-182">Argument d’énumération de commande ou de fonction : xlfn</span><span class="sxs-lookup"><span data-stu-id="19f0c-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="19f0c-p112">L�argument  _xlfn_ est le premier argument des fonctions de rappel et est un entier sign� 32�bits. Sa valeur doit �tre une des �num�rations de fonction ou de commande d�finies dans le fichier d�en-t�te SDK Xlcall.h, comme indiqu� dans l�exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p112">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer. Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="19f0c-185">Toutes les fonctions de feuille de calcul et de feuille de macro figurent dans la plage hexadécimale entre 0 (**xlfCount**) et 0x0fff bien que la valeur la plus élevée affectée dans Excel 2013 soit 547 (en base décimale) ou 0x0223 (en base hexadécimale). (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="19f0c-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="19f0c-186">Toutes les fonctions de commande figurent dans la plage de nombres décimaux entre 0x8000 (**xlcBeep**) et 0x8fff, bien que la valeur la plus élevée affectée dans Excel 2013 soit 0x8328 (**xlcHideallInkannots**).</span><span class="sxs-lookup"><span data-stu-id="19f0c-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="19f0c-187">Elles sont définies dans le fichier d’en-tête `(n | xlCommand)`, où `n` est un nombre décimal supérieur ou égal à 0 et **xlCommand** est défini en tant que nombre hexadécimal 0x8000.</span><span class="sxs-lookup"><span data-stu-id="19f0c-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="19f0c-188">Appel de commandes Excel qui utilisent des boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="19f0c-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="19f0c-p114">Certains codes de commande correspondent aux actions Excel qui utilisent des boîtes de dialogue. Par exemple, **xlcFileDelete** prend un seul argument : un nom de fichier ou un masque. Cet appel peut s’effectuer avec la boîte de dialogue afin que l’utilisateur puisse annuler ou modifier l’opération de suppression. Il peut s’effectuer également sans la boîte de dialogue, auquel cas le ou les fichiers sont supprimés sans autre intervention, en supposant qu’ils existent et que l’appelant dispose des autorisations nécessaires. Pour appeler de telles commandes dans leur formulaire de boîte de dialogue, l’énumération de commande doit être combinée à l’aide de l’opération OR avec 0x1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="19f0c-p114">Some of the command codes correspond to actions in Excel that use dialog boxes. For example, **xlcFileDelete** takes a single argument: a file name or mask. This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation. It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission. To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="19f0c-194">L�exemple suivant supprime les fichiers dans le r�pertoire actif correspondant au masque my_data\*.bak. Une bo�te de dialogue s�affiche uniquement si l�argument est vrai.</span><span class="sxs-lookup"><span data-stu-id="19f0c-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="19f0c-195">Appel de fonctions et de commandes dans les versions internationales</span><span class="sxs-lookup"><span data-stu-id="19f0c-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="19f0c-p115">Vous pouvez configurer Excel de façon à afficher les fonctions et les noms des commandes XML dans plusieurs langues. Certaines fonctions et commandes de l’API C opèrent sur des chaînes qui sont considérées comme des noms de fonction ou de commande. Par exemple, **xlcFormula** prend un argument de chaîne qui est destiné à être placé dans une cellule spécifiée. Pour que votre complément fonctionne avec tous les paramètres de langue, vous pouvez fournir les noms de chaîne en anglais et définir le bit 0x2000 (**xlIntl**) dans l’énumération de fonction ou de commande.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p115">You can configure Excel to display functions and XLM command names in a variety of languages. Some C API commands and functions operate on strings that are interpreted as function or command names. For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell. For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="19f0c-p116">L�exemple suivant ins�re l��quivalent de  `=SUM(X1:X100)` dans la cellule A2 de la feuille active. Notez qu�il utilise la fonction Framework **TempActiveRef** pour cr�er une référence externe temporaire **XLOPER**. La formule appara�t dans la cellule A2 dans la langue correcte d�termin�e par les param�tres r�gionaux (par exemple,  `=SOMME(X1:X100)` si la langue est le fran�ais).</span><span class="sxs-lookup"><span data-stu-id="19f0c-p116">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet. Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**. The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="19f0c-p117">�tant donn� que le r�sultat de l�appel de **Excel12** n�est pas requis, z�ro (NULL) peut �tre pass� comme deuxi�me argument � la place de l�adresse de **xResult**. Ce point est abord� en d�tail dans la section suivante.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p117">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**. This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="19f0c-205">Fonctions et commandes DLL uniquement</span><span class="sxs-lookup"><span data-stu-id="19f0c-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="19f0c-p118">Excel prend en charge un petit nombre de fonctions accessibles uniquement � partir d�une DLL ou d�une XLL. Elles sont d�finies dans le fichier d�en-t�te  `(n | xlSpecial)`, o�  `n` est un nombre d�cimal sup�rieur ou �gal � 0 et  `xlSpecial` est d�fini en tant que nombre d�cimal 0x4000. Ces fonctions sont r�pertori�es dans le tableau suivant et pr�sent�es dans la [Référence des fonctions d�API](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="19f0c-p118">Excel supports a small number of functions that are only accessible from a DLL or XLL. These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal. These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="19f0c-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="19f0c-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="19f0c-210">0</span><span class="sxs-lookup"><span data-stu-id="19f0c-210">0</span></span> | <span data-ttu-id="19f0c-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-212">Libère les ressources de mémoire allouées par Excel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="19f0c-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="19f0c-214">1</span><span class="sxs-lookup"><span data-stu-id="19f0c-214">1</span></span> | <span data-ttu-id="19f0c-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-216">Renvoie l’espace libre dans la pile Excel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="19f0c-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="19f0c-218">2</span><span class="sxs-lookup"><span data-stu-id="19f0c-218">2</span></span> | <span data-ttu-id="19f0c-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-220">Convertit les types **XLOPER** et **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="19f0c-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="19f0c-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="19f0c-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="19f0c-222">3</span><span class="sxs-lookup"><span data-stu-id="19f0c-222">3</span></span> | <span data-ttu-id="19f0c-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-224">Fournit une méthode rapide de définition des valeurs de cellule.</span><span class="sxs-lookup"><span data-stu-id="19f0c-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="19f0c-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="19f0c-226">4</span><span class="sxs-lookup"><span data-stu-id="19f0c-226">4</span></span> | <span data-ttu-id="19f0c-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-228">Obtient un nom de feuille de calcul à l’aide de son ID interne.</span><span class="sxs-lookup"><span data-stu-id="19f0c-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="19f0c-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="19f0c-230">5</span><span class="sxs-lookup"><span data-stu-id="19f0c-230">5</span></span> | <span data-ttu-id="19f0c-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-232">Obtient un ID interne de feuille de calcul à l’aide de son nom.</span><span class="sxs-lookup"><span data-stu-id="19f0c-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="19f0c-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="19f0c-234">6</span><span class="sxs-lookup"><span data-stu-id="19f0c-234">6</span></span> | <span data-ttu-id="19f0c-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-236">V�rifie si l�utilisateur a cliqu� sur le bouton **ANNULER** ou a appuy� sur la touche �CHAP.</span><span class="sxs-lookup"><span data-stu-id="19f0c-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="19f0c-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="19f0c-238">7</span><span class="sxs-lookup"><span data-stu-id="19f0c-238">7</span></span> | <span data-ttu-id="19f0c-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-240">Obtient le pointeur d’instance Excel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="19f0c-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="19f0c-242">8</span><span class="sxs-lookup"><span data-stu-id="19f0c-242">8</span></span> | <span data-ttu-id="19f0c-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-244">Obtient le pointeur de fenêtre principale Excel.</span><span class="sxs-lookup"><span data-stu-id="19f0c-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="19f0c-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="19f0c-246">9</span><span class="sxs-lookup"><span data-stu-id="19f0c-246">9</span></span> | <span data-ttu-id="19f0c-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-248">Obtient le chemin d’accès et le nom de la DLL.</span><span class="sxs-lookup"><span data-stu-id="19f0c-248">Gets the path and file name of the DLL.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="19f0c-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="19f0c-250">10</span><span class="sxs-lookup"><span data-stu-id="19f0c-250">10</span></span> | <span data-ttu-id="19f0c-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-252">Cette fonction est déconseillée et ne doit plus être appelée.</span><span class="sxs-lookup"><span data-stu-id="19f0c-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="19f0c-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="19f0c-254">11</span><span class="sxs-lookup"><span data-stu-id="19f0c-254">11</span></span> | <span data-ttu-id="19f0c-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-256">Cette fonction est déconseillée et ne doit plus être appelée.</span><span class="sxs-lookup"><span data-stu-id="19f0c-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="19f0c-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="19f0c-258">12</span><span class="sxs-lookup"><span data-stu-id="19f0c-258">12</span></span> | <span data-ttu-id="19f0c-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-260">Définit un nom de stockage binaire permanent.</span><span class="sxs-lookup"><span data-stu-id="19f0c-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="19f0c-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="19f0c-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="19f0c-262">13</span><span class="sxs-lookup"><span data-stu-id="19f0c-262">13</span></span> | <span data-ttu-id="19f0c-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="19f0c-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="19f0c-264">Obtient les données d’un nom de stockage permanent binaire.</span><span class="sxs-lookup"><span data-stu-id="19f0c-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="19f0c-265">Renvoyer la valeur XLOPER/XLOPER12 : operRes</span><span class="sxs-lookup"><span data-stu-id="19f0c-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="19f0c-266">L’argument _operRes_ est le deuxième argument pour les rappels et il s’agit d’un pointeur vers un élément **XLOPER** (**Excel4** et **Excel4v**) ou **XLOPER12** (**Excel12** et **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="19f0c-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="19f0c-267">Après un appel réussi, il contient la valeur renvoyée de la fonction ou de la commande.</span><span class="sxs-lookup"><span data-stu-id="19f0c-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="19f0c-268">**operRes** peut �tre configur� sur z�ro (pointeur NULL) si aucune valeur de retour n�est requise.</span><span class="sxs-lookup"><span data-stu-id="19f0c-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="19f0c-269">Le contenu pr�c�dent de **operRes** est remplac� afin que toute m�moire pr�c�demment point�e soit lib�r�e avant l�appel pour �viter les pertes de m�moire.</span><span class="sxs-lookup"><span data-stu-id="19f0c-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="19f0c-p120">Si la fonction ou la commande ne peut pas �tre appel�e (par exemple, si les arguments sont incorrects), **operRes** est d�finie sur l�erreur **#VALUE!**. Une commande retourne toujours **Boolean** **TRUE** si elle r�ussit, ou **FALSE** si elle a �chou� ou a �t� annul�e par l�utilisateur.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p120">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**. A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="19f0c-272">Nombre d’arguments suivants</span><span class="sxs-lookup"><span data-stu-id="19f0c-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="19f0c-p121">L�argument  _count_ est le troisi�me argument des rappels et est un entier sign� 32�bits. Il doit �tre configur� pour le nombre d�arguments suivants, en partant de 1. Si une fonction ou une commande ne prend aucun argument, elle doit �tre d�finie sur z�ro. Dans Microsoft Office Excel 2003, le nombre maximal d�arguments qu�une fonction accepte est �gal � 30 bien que la plupart des fonctions g�rent g�n�ralement moins d�arguments. � partir de Excel 2007, le nombre maximal d�arguments pouvant �tre pris en charge par une fonction est pass� � 255.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p121">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer. It should be set to the number of subsequent arguments, counting from 1. If a function or command takes no arguments, it should be set to zero. In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this. Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="19f0c-p122">Avec **Excel4** et **Excel12**,  _count_ correspond au nombre de pointeurs vers les valeurs **XLOPER** ou **XLOPER12** transmises. Vous devez veiller � ne pas transmettre moins d�arguments que la valeur que  _count_ a d�finie. En effet, Excel risque d�effectuer des lectures anticip�es dans la pile et de tenter de lire des valeurs **XLOPER** ou **XLOPER12** non valides, ce qui pourrait bloquer l�application.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p122">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed. You should be very careful not to pass fewer arguments than the value that  _count_ is set to. This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="19f0c-p123">Avec **Excel4v** et **Excel12v**,  _count_ est la taille de la matrice des pointeurs vers les valeurs **XLOPER** ou **XLOPER12** transmises en tant qu�argument final. L� encore, vous devez veiller � ne pas passer un tableau inf�rieur �  _count_ �l�ments, car cela entra�nerait la saturation des limites de la matrice.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p123">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument. Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="19f0c-283">Passage d’arguments aux fonctions d’API C</span><span class="sxs-lookup"><span data-stu-id="19f0c-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="19f0c-p124">**Excel4** et **Excel12** g�rent des listes d�arguments de longueur variable,  _count_, qui sont interpr�t�es comme des pointeurs vers les valeurs **XLOPER** et **XLOPER12**, respectivement. **Excel4v** et **Excel12v** g�rent un seul argument, apr�s  _count_, qui est un pointeur vers un tableau de pointeurs vers des valeurs **XLOPER** dans le cas de **Excel4v**, et vers des valeurs **XLOPER12** dans le cas de **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p124">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively. **Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="19f0c-p125">Les formulaires de matrice **Excel4v** et **Excel12v** vous permettent de coder un appel � l�API C proprement lorsque le nombre d�arguments est variable. L�exemple suivant montre une fonction qui g�re un tableau de taille variable de nombres et qui utilise les fonctions de feuille de calcul Excel, via l�API C, pour calculer la somme, la moyenne, le minimum et le maximum.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p125">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable. The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="19f0c-p126">Le remplacement des références des valeurs **XLOPER12** par **XLOPER**, et **Excel12v** par **Excel4v**, dans le code pr�c�dent permettait d�avoir une fonction compatible avec toutes les versions d�Excel. L�ex�cution de ces fonctions Excel **SUM**, **AVERAGE**, **MIN** et **MAX** est assez simple et il serait plus efficace de les coder en langage�C afin de ne pas avoir � pr�parer les arguments et l�appel dans Excel. Toutefois, la plupart des fonctions Excel sont plus complexes, ce qui rend cette approche utile dans certains cas.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p126">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel. This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel. However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="19f0c-p127">La rubrique [xlfRegister](xlfregister-form-1.md) offre un autre exemple d�utilisation de **Excel4v** et **Excel12v**. Lorsque vous enregistrez une fonction de feuille de calcul XLL, vous pouvez fournir une cha�ne descriptive pour chaque argument utilis� dans la bo�te de dialogue **Coller une fonction**. Par cons�quent, le nombre total d�arguments fourni � **xlfRegister** d�pend du nombre d�arguments que votre fonction XLL accepte et varie d�une fonction � l�autre.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p127">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**. When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box. Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="19f0c-p128">Lorsque vous appelez toujours une fonction API C ou une commande avec le m�me nombre d�arguments, vous voulez �viter d�avoir � cr�er un tableau de pointeurs pour ces arguments. Dans ce cas, il est plus simple et plus rationnel d�utiliser **Excel4** et **Excel12**. Par exemple, lorsque vous enregistrez des commandes et fonctions XLL, vous devez fournir le chemin et le nom de fichier complets de la DLL ou de la XLL. Vous pouvez obtenir le nom du fichier dans un appel � **xlfGetName**, puis le lib�rer avec un appel � **xlFree**, comme montr� dans l�exemple suivant pour **Excel4** et **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p128">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments. In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**. For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL. You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="19f0c-298">Dans la pratique, la fonction **Excel12v_example** peut �tre cod�e plus efficacement en cr�ant un seul argument **xltypeMulti** **XLOPER12** et en appelant l�API C � l�aide de **Excel12**, comme montr� dans l�exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="19f0c-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="19f0c-p129">Dans ce cas, la valeur de retour de **Excel12** est ignor�e. Au lieu de cela, le code v�rifie que le texte renvoy� **XLOPER12** est **xltypeNum** pour d�terminer si l�appel a r�ussi.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p129">In this case, the return value of **Excel12** is ignored. The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="19f0c-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="19f0c-301">XLCallVer</span></span>

<span data-ttu-id="19f0c-302">Outre les rappels **Excel4**, **Excel4v**, **Excel12** et **Excel12v**, Excel exporte une fonction **XLCallVer**, qui retourne la version de l�API C en cours d�ex�cution.</span><span class="sxs-lookup"><span data-stu-id="19f0c-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="19f0c-303">La syntaxe du prototype de la fonction est la suivante :</span><span class="sxs-lookup"><span data-stu-id="19f0c-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="19f0c-304">Vous pouvez appeler cette fonction thread-safe à partir de n’importe quelle commande ou fonction XLL.</span><span class="sxs-lookup"><span data-stu-id="19f0c-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="19f0c-p130">D�Excel 97 � Excel 2003, **XLCallVer** renvoie 1280 = 0x0500 hex = 5 x 256, qui indique Excel�5. Depuis Excel 2007, elle renvoie 3072 = 0x0c00 hex = 12 x 256, qui indique de la m�me fa�on la version�12.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p130">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5. Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="19f0c-p131">Bien que vous puissiez utiliser ce m�canisme pour d�terminer si la nouvelle API C est disponible au moment de l�ex�cution, vous pouvez d�tecter l�ex�cution de la version d�Excel � l�aide de  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, o�  `arg` est une valeur num�rique **XLOPER** d�finie sur 2. La fonction retourne une cha�ne **XLOPER**, version, qui peut ensuite �tre convertie en entier. Selon le cas, vous pouvez vous appuyer sur la version Excel plut�t que sur la version API C, car il existe des diff�rences entre Excel 2000, Excel 2002 et Excel 2003 que votre compl�ment peut �galement avoir � d�tecter. Par exemple, des modifications ont �t� apport�es � la pr�cision de certaines fonctions statistiques.</span><span class="sxs-lookup"><span data-stu-id="19f0c-p131">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2. The function returns a string **XLOPER**, version, which can then be coerced to an integer. The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect. For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="19f0c-311">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="19f0c-311">See also</span></span>

- [<span data-ttu-id="19f0c-312">Création de XLL</span><span class="sxs-lookup"><span data-stu-id="19f0c-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="19f0c-313">Accés au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="19f0c-313">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="19f0c-314">Référence des fonctions XLL SDK API Excel 2013</span><span class="sxs-lookup"><span data-stu-id="19f0c-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="19f0c-315">Les fonctions de rappel de l'API C Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="19f0c-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="19f0c-316">Développement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="19f0c-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

