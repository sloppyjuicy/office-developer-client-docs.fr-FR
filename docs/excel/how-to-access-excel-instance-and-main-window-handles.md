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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="fa166-104">Instance d’Excel Access et les poignées de la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="fa166-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="fa166-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fa166-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fa166-106">Pour programmer dans l’environnement Windows, parfois vous devez connaître le descripteur d’instances Microsoft Excel ou de la fenêtre principale gérer.</span><span class="sxs-lookup"><span data-stu-id="fa166-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="fa166-107">Par exemple, ces poignées sont utiles lorsque vous créez et affichage des boîtes de dialogue Windows personnalisés.</span><span class="sxs-lookup"><span data-stu-id="fa166-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="fa166-108">Il existe deux fonctions XLL uniquement API C qui permettent d’accéder à ces poignées : la fonction [xlGetInst](xlgetinst.md) et la [xlGetHwnd](xlgethwnd.md) fonctionnent respectivement.</span><span class="sxs-lookup"><span data-stu-id="fa166-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="fa166-109">Dans Win32, toutes les poignées sont des entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fa166-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="fa166-110">Toutefois, lorsque la **XLOPER** a été conçu, Windows était un système 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fa166-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="fa166-111">Par conséquent, la structure autorisée uniquement pour les poignées de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="fa166-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="fa166-112">Dans Win32, lorsqu’elle est appelée avec **Excel4** ou **Excel4v**, la fonction **xlGetInst** et la fonction **xlGetHwnd** retournent uniquement la partie basse de la poignée 32 bits complète.</span><span class="sxs-lookup"><span data-stu-id="fa166-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="fa166-113">Dans Excel 2007 et versions ultérieures, lorsque ces fonctions sont appelées avec [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), le renvoyée **XLOPER12** contient un handle 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fa166-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="fa166-114">Obtenir le descripteur d’instances complète est simple dans n’importe quelle version d’Excel, tel qu’il est passé au rappel Windows **DllMain**, qui est appelée lorsque la DLL est chargée.</span><span class="sxs-lookup"><span data-stu-id="fa166-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="fa166-115">Si vous enregistrez ce descripteur d’instances dans une variable globale, vous devez jamais appeler la fonction **xlGetInst** .</span><span class="sxs-lookup"><span data-stu-id="fa166-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="fa166-116">Obtenir le Handle principale Excel dans Excel 2003 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="fa166-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="fa166-117">Pour obtenir le handle Excel principal dans Excel 2003 et versions antérieures de 32 bits, vous devez d’abord appeler la fonction **xlGetHwnd** pour obtenir le mot bas de la poignée de réel.</span><span class="sxs-lookup"><span data-stu-id="fa166-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="fa166-118">Puis, vous devez itérer la liste des fenêtres de niveau supérieur pour rechercher une correspondance avec le mot de poids faible renvoyée.</span><span class="sxs-lookup"><span data-stu-id="fa166-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="fa166-119">Le code suivant illustre la technique.</span><span class="sxs-lookup"><span data-stu-id="fa166-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="fa166-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa166-120">See also</span></span>



[<span data-ttu-id="fa166-121">Affichage des boîtes de dialogue à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="fa166-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="fa166-122">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="fa166-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="fa166-123">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="fa166-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

