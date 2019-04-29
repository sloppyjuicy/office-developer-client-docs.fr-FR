---
title: Appeler des fonctions XLL à partir de l'Assistant fonction ou des boîtes de dialogue remplacer
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions XLL [Excel 2007], appel de la boîte de dialogue remplacer, boîte de dialogue remplacer [Excel 2007], appel des fonctions XLL, Assistant fonction [Excel 2007], appel des fonctions XLL, fonctions XLL [Excel 2007], appel à partir de l'Assistant fonction
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 11189beed13e2ceb99ef04b7a2f966cb4171915c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410748"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="d11fa-104">Appeler des fonctions XLL à partir de l'Assistant fonction ou des boîtes de dialogue remplacer</span><span class="sxs-lookup"><span data-stu-id="d11fa-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="d11fa-105">**S’applique à** : Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d11fa-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d11fa-106">Microsoft Excel appelle généralement des fonctions XLL lors du recalcul normal du classeur ou d'une partie de celui-ci si le calcul est sous le contrôle d'une macro.</span><span class="sxs-lookup"><span data-stu-id="d11fa-106">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro.</span></span> <span data-ttu-id="d11fa-107">N'oubliez pas que la fonction ne se trouve pas dans une formule de cellule, mais peut faire partie d'une définition de plage nommée ou d'une expression conditionnelle de mise en forme.</span><span class="sxs-lookup"><span data-stu-id="d11fa-107">Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="d11fa-108">Il existe deux cas dans lesquels une fonction peut être appelée à partir d'une boîte de dialogue Excel.</span><span class="sxs-lookup"><span data-stu-id="d11fa-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="d11fa-109">La première est la boîte de dialogue de **collage des arguments** de la fonction, dans laquelle les utilisateurs peuvent construire une fonction appeler un argument à la fois.</span><span class="sxs-lookup"><span data-stu-id="d11fa-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="d11fa-110">L'autre est lorsque les formules sont modifiées et resaisies par Excel dans la boîte de dialogue **remplacer** .</span><span class="sxs-lookup"><span data-stu-id="d11fa-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="d11fa-111">Pour la boîte de dialogue **coller les arguments** de la fonction, il se peut que vous ne voulez pas que votre fonction s'exécute normalement.</span><span class="sxs-lookup"><span data-stu-id="d11fa-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="d11fa-112">Cela peut être dû à une longue durée d'exécution et vous ne voulez pas ralentir l'utilisation de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d11fa-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="d11fa-113">La boîte de dialogue **coller une fonction** et la boîte de dialogue **remplacer** portent le nom de classe Windows **bosa_sdm_XL**n, où n est un nombre.</span><span class="sxs-lookup"><span data-stu-id="d11fa-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="d11fa-114">Windows fournit une fonction d'API, **GetClassName**, qui obtient ce nom à partir d'un handle Windows, un type de variable HWND.</span><span class="sxs-lookup"><span data-stu-id="d11fa-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="d11fa-115">Elle fournit également une autre fonction, **EnumWindows**, qui appelle une fonction de rappel fournie (dans votre dll) une fois pour chaque fenêtre de niveau supérieur ouverte.</span><span class="sxs-lookup"><span data-stu-id="d11fa-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="d11fa-116">La fonction de rappel doit effectuer uniquement les étapes suivantes:</span><span class="sxs-lookup"><span data-stu-id="d11fa-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="d11fa-117">Vérifiez si le parent de cette fenêtre est l'instance actuelle d'Excel (si plusieurs instances sont en cours d'exécution).</span><span class="sxs-lookup"><span data-stu-id="d11fa-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="d11fa-118">Obtenez le nom de la classe à partir du handle transmis par Windows.</span><span class="sxs-lookup"><span data-stu-id="d11fa-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="d11fa-119">Vérifiez si le nom de la classe se présente sous la forme **bosa_sdm_XL**n.</span><span class="sxs-lookup"><span data-stu-id="d11fa-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="d11fa-120">Si vous devez faire la distinction entre les deux boîtes de dialogue, vérifiez si le titre de la boîte de dialogue contient du texte d'identification.</span><span class="sxs-lookup"><span data-stu-id="d11fa-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="d11fa-121">Le titre de la fenêtre est obtenu à l'aide \*\*\*\* de l'API Windows.</span><span class="sxs-lookup"><span data-stu-id="d11fa-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="d11fa-122">Le code C++ suivant montre une classe et un rappel à transmettre à Windows qui effectue ces étapes.</span><span class="sxs-lookup"><span data-stu-id="d11fa-122">The following C++ code shows a class and callback to be passed to Windows that performs these steps.</span></span> <span data-ttu-id="d11fa-123">Cela est appelé par les fonctions qui appellent un test spécifique pour l'une des boîtes de dialogue concernées.</span><span class="sxs-lookup"><span data-stu-id="d11fa-123">This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d11fa-124">Les titres des fenêtres des versions ultérieures d'Excel pourraient modifier et invalider ce code.</span><span class="sxs-lookup"><span data-stu-id="d11fa-124">Window titles of future Excel versions might change and invalidate this code.</span></span> <span data-ttu-id="d11fa-125">Notez également que le fait de définir **window_title_text** sur **null** a pour effet d'ignorer le titre de la fenêtre dans la recherche de rappel.</span><span class="sxs-lookup"><span data-stu-id="d11fa-125">Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

<span data-ttu-id="d11fa-126">La boîte de dialogue **coller une fonction** n'a pas de titre, de sorte que la fonction suivante transmet une chaîne de titre de recherche de «», c'est-à-dire une chaîne vide, au rappel pour indiquer que la condition de correspondance est que la fenêtre ne doit pas avoir de titre.</span><span class="sxs-lookup"><span data-stu-id="d11fa-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a><span data-ttu-id="d11fa-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d11fa-127">See also</span></span>



[<span data-ttu-id="d11fa-128">Accés au code XLL dans Excel</span><span class="sxs-lookup"><span data-stu-id="d11fa-128">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)
  
[<span data-ttu-id="d11fa-129">Appel dans Excel � partir du fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="d11fa-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="d11fa-130">Développement de XLL de Excel</span><span class="sxs-lookup"><span data-stu-id="d11fa-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

