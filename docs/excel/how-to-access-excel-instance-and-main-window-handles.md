---
title: Instance d’Excel Access et les poignées de la fenêtre principale
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accès aux poignées, poignées [Excel 2007], accédez à, Excel instances, accédez à, handles de fenêtre [Excel 2007], l’accès à d’excel
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782143"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Instance d’Excel Access et les poignées de la fenêtre principale

 **S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
Pour programmer dans l’environnement Windows, parfois vous devez connaître le descripteur d’instances Microsoft Excel ou de la fenêtre principale gérer. Par exemple, ces poignées sont utiles lorsque vous créez et affichage des boîtes de dialogue Windows personnalisés.
  
Il existe deux fonctions XLL uniquement API C qui permettent d’accéder à ces poignées : la fonction [xlGetInst](xlgetinst.md) et la [xlGetHwnd](xlgethwnd.md) fonctionnent respectivement. Dans Win32, toutes les poignées sont des entiers 32 bits. Toutefois, lorsque la **XLOPER** a été conçu, Windows était un système 16 bits. Par conséquent, la structure autorisée uniquement pour les poignées de 16 bits. Dans Win32, lorsqu’elle est appelée avec **Excel4** ou **Excel4v**, la fonction **xlGetInst** et la fonction **xlGetHwnd** retournent uniquement la partie basse de la poignée 32 bits complète. 
  
Dans Excel 2007 et versions ultérieures, lorsque ces fonctions sont appelées avec [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), le renvoyée **XLOPER12** contient un handle 32 bits. 
  
Obtenir le descripteur d’instances complète est simple dans n’importe quelle version d’Excel, tel qu’il est passé au rappel Windows **DllMain**, qui est appelée lorsque la DLL est chargée. Si vous enregistrez ce descripteur d’instances dans une variable globale, vous devez jamais appeler la fonction **xlGetInst** . 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Obtenir le Handle principale Excel dans Excel 2003 et versions antérieures

Pour obtenir le handle Excel principal dans Excel 2003 et versions antérieures de 32 bits, vous devez d’abord appeler la fonction **xlGetHwnd** pour obtenir le mot bas de la poignée de réel. Puis, vous devez itérer la liste des fenêtres de niveau supérieur pour rechercher une correspondance avec le mot de poids faible renvoyée. Le code suivant illustre la technique. 
  
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
  // which match the LoWord retuned by xlGetHwnd.
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



[Affichage des boîtes de dialogue à partir d’une DLL ou XLL](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[D�veloppement de XLL de Excel 2013](developing-excel-xlls.md)

