---
title: Accéder à l'instance Excel et aux handles de fenêtre principaux
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accès aux handles Excel, Handles [Excel 2007], accès, instances Excel, accès, handles de fenêtre [Excel 2007], accès
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4b71ccd428e60c9ba2e59fea0e56eb2fc61390db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310758"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Accéder à l'instance Excel et aux handles de fenêtre principaux

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour programmer dans l'environnement Windows, vous devez parfois posséder le handle de l'instance Microsoft Excel ou le handle de la fenêtre principale. Par exemple, ces handles sont utiles lorsque vous créez et affichez des boîtes de dialogue Windows personnalisées.
  
Il existe deux fonctions d'API C XLL uniquement qui fournissent l'accès à ces handles: la fonction [xlGetInst](xlgetinst.md) et la fonction [xlGetHwnd](xlgethwnd.md) . Dans Win32, tous les handles sont des entiers 32 bits. Toutefois, lorsque la conception **XLOPER** a été conçue, Windows était un système 16 bits. Par conséquent, la structure n'est autorisée que pour les handles 16 bits. Dans Win32, lorsqu'elle est appelée avec **Excel4** ou **Excel4v**, la fonction **xlGetInst** et la fonction **xlGetHwnd** renvoient uniquement la partie basse de la poignée complète 32 bits. 
  
Dans Excel 2007 et versions ultérieures, lorsque ces fonctions sont appelées avec [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), le **XLOPER12** renvoyé contient la poignée complète 32 bits. 
  
L'obtention du handle d'instance complet est simple dans n'importe quelle version d'Excel, car il est transmis au service **DllMain**de rappel Windows, qui est appelé lors du chargement de la dll. Si vous enregistrez ce handle d'instance dans une variable globale, vous n'avez jamais besoin d'appeler la fonction **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtention du handle Excel principal dans Excel 2003 et versions antérieures

Pour obtenir le descripteur Excel principal dans Excel 2003 et les versions antérieures de 32 bits, vous devez d'abord appeler la fonction **xlGetHwnd** afin d'obtenir le mot bas du handle réel. Ensuite, vous devez parcourir la liste des fenêtres de niveau supérieur pour rechercher une correspondance avec le mot bas renvoyé. Le code suivant illustre la technique. 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord returned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>Voir aussi



[Affichage des boîtes de dialogue dans un fichier DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

