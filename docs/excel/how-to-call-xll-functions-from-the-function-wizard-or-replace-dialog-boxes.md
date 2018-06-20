---
title: Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions de XLL [excel 2007], appel à partir de la boîte de dialogue Remplacer, boîte de dialogue Remplacer zone fonctions XLL [Excel 2007], appel, Assistant fonction [Excel 2007], appeler des fonctions XLL, fonctions XLL [Excel 2007], appel à partir de l’Assistant fonction
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782140"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a>Appel des fonctions XLL à partir de l’Assistant fonction ou remplacer des boîtes de dialogue

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Si le calcul est sous le contrôle d’une macro, Microsoft Excel appelle généralement fonctions XLL pendant le recalcul normal du classeur, ou une partie de celle-ci. N’oubliez pas que la fonction ne peut pas résider dans une formule de cellule, mais peut-être faire partie d’une définition de la plage nommée ou une expression de mise en forme conditionnelle.
  
Il existe deux cas où une fonction peut être appelée à partir d’une boîte de dialogue Excel. Une est la boîte de dialogue **Arguments de la fonction Coller** , où les utilisateurs sont en mesure de construire un un argument appel de fonction à la fois. L’autre est lorsque les formules sont modifiées et réentrées par Excel dans la boîte de dialogue **Remplacer** . Pour la boîte de dialogue **Arguments de la fonction Coller** , vous pouvez ne pas vouloir votre fonction s’exécuter normalement. Cela peut être, car elle prend beaucoup de temps d’exécution et vous ne souhaitez pas l’utilisation de la boîte de dialogue de ralentir. 
  
La boîte de dialogue **Coller une fonction** et de la boîte de dialogue **Remplacer** ont Windows classe nom **bosa_sdm_XL**n, où n est un nombre. Windows propose une fonction d’API, **GetClassName**, qui obtient ce nom à partir d’une poignée de Windows, un type de variable HWND. Il fournit également une autre fonction, **EnumWindows**, qui appelle une fonction de rappel fourni (au sein de votre DLL) qu’une seule fois pour chaque fenêtre de niveau supérieur qui est actuellement ouvert.
  
La fonction de rappel doit effectuer les étapes suivantes uniquement :
  
1. Vérifiez si le parent de la fenêtre est l’instance actuelle de Microsoft Excel (au cas où il existe plusieurs instances en cours d’exécution).
    
2. Obtenir le nom de classe à partir du handle passé par Windows.
    
3. Vérifiez si le nom de classe de formulaire **bosa_sdm_XL**n.
    
4. Si vous devez faire la distinction entre les deux boîtes de dialogue, vérifiez si le titre de la boîte de dialogue contient du texte d’identification. Titre de la fenêtre est obtenu à l’aide de l’appel d’API Windows **GetWindowText**.
    
Le code C++ suivant illustre une classe et un rappel à transmettre à Windows qui effectue ces étapes. Il s’agit par les fonctions de ce test d’appel spécifiquement pour une des boîtes de dialogue concernés. 
  
> [!NOTE]
> Titres des fenêtres de futures versions d’Excel peuvent modifier et invalider ce code. Notez également que la définition de **window_title_text** sur **NULL** a pour effet d’ignorer le titre de la fenêtre de la recherche de rappel. 
  
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

La boîte de dialogue **Coller une fonction** ne dispose pas d’un titre, afin que la fonction suivante transmet une chaîne de titre de recherche de « », c'est-à-dire, une chaîne vide au rappel pour indiquer que la condition de correspondance est que la fenêtre ne doit pas comporter un titre. 
  
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



[Acc�s au code XLL dans Excel (en anglais)](accessing-xll-code-in-excel.md)
  
[Appel dans Excel � partir du fichier DLL ou XLL](calling-into-excel-from-the-dll-or-xll.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

