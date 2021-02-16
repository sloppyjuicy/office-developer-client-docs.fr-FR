---
title: Appeler des fonctions XLL à partir de l’Assistant Fonction ou remplacer des boîtes de dialogue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
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
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Appeler des fonctions XLL à partir de l’Assistant Fonction ou remplacer des boîtes de dialogue

 **S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel appelle généralement des fonctions XLL pendant le recalcul normal du manuel, ou une partie de celui-ci si le calcul est sous le contrôle d’une macro. N’oubliez pas que la fonction peut ne pas résider dans une formule de cellule, mais peut faire partie d’une définition de plage nommée ou d’une expression de mise en forme conditionnelle.
  
Il existe deux cas où une fonction peut être appelée à partir d’une boîte de dialogue Excel. La première est la **boîte de dialogue Arguments de** la fonction coller, dans laquelle les utilisateurs peuvent construire un appel de fonction un argument à la fois. L’autre est lorsque les formules sont modifiées et réentées par Excel dans la **boîte** de dialogue Remplacer. Pour la **boîte de dialogue Arguments de** la fonction coller, vous ne souhaitez peut-être pas que votre fonction s’exécute normalement. Cela peut être dû au fait que l’exécution prend beaucoup de temps et que vous ne souhaitez pas ralentir l’utilisation de la boîte de dialogue. 
  
La boîte de dialogue  **Coller la** fonction et la boîte de dialogue Remplacer ont le nom de classe Windows **bosa_sdm_XL** n, où n est un nombre. Windows fournit une fonction API, **GetClassName**, qui obtient ce nom à partir d’un handle Windows, un type de variable HWND. Il fournit également une autre fonction, **EnumWindows,** qui appelle une fonction de rappel fournie (dans votre DLL) une fois pour chaque fenêtre de niveau supérieur actuellement ouverte.
  
La fonction de rappel doit effectuer uniquement les étapes suivantes :
  
1. Vérifiez si le parent de cette fenêtre est l’instance actuelle d’Excel (si plusieurs instances sont en cours d’exécution).
    
2. Obtenez le nom de classe à partir du handle transmis par Windows.
    
3. Vérifiez si le nom de la classe est au **bosa_sdm_XL** n.
    
4. Si vous devez faire la distinction entre les deux boîtes de dialogue, vérifiez si le titre de la boîte de dialogue contient du texte d’identification. Le titre de la fenêtre est obtenu à l’aide de l’appel de l’API Windows **GetWindowText**.
    
Le code C++ suivant montre une classe et un rappel à passer à Windows qui effectue ces étapes. Cette fonction est appelée par les fonctions qui appellent le test spécifiquement pour l’une des boîtes de dialogue concernées. 
  
> [!NOTE]
> Les titres de fenêtre des versions ultérieures d’Excel peuvent modifier et invalider ce code. Notez également que la **définition window_title_text** **sur NULL** a pour effet d’ignorer le titre de la fenêtre dans la recherche de rappel. 
  
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

La  boîte de dialogue Coller une fonction n’a pas de titre, donc la fonction suivante transmet une chaîne de titre de recherche de « », c’est-à-dire une chaîne vide, au rappel pour indiquer que la condition de correspondance est que la fenêtre ne doit pas avoir de titre. 
  
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

## <a name="see-also"></a>Voir aussi



[Accés au code XLL dans Excel](accessing-xll-code-in-excel.md)
  
[Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[Développement de XLL de Excel](developing-excel-xlls.md)

