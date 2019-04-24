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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="cfb2b-104">Accéder à l'instance Excel et aux handles de fenêtre principaux</span><span class="sxs-lookup"><span data-stu-id="cfb2b-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="cfb2b-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="cfb2b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="cfb2b-106">Pour programmer dans l'environnement Windows, vous devez parfois posséder le handle de l'instance Microsoft Excel ou le handle de la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-106">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle.</span></span> <span data-ttu-id="cfb2b-107">Par exemple, ces handles sont utiles lorsque vous créez et affichez des boîtes de dialogue Windows personnalisées.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-107">For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="cfb2b-108">Il existe deux fonctions d'API C XLL uniquement qui fournissent l'accès à ces handles: la fonction [xlGetInst](xlgetinst.md) et la fonction [xlGetHwnd](xlgethwnd.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb2b-108">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively.</span></span> <span data-ttu-id="cfb2b-109">Dans Win32, tous les handles sont des entiers 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-109">In Win32, all handles are 32-bit integers.</span></span> <span data-ttu-id="cfb2b-110">Toutefois, lorsque la conception **XLOPER** a été conçue, Windows était un système 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-110">However, when the **XLOPER** was designed, Windows was a 16-bit system.</span></span> <span data-ttu-id="cfb2b-111">Par conséquent, la structure n'est autorisée que pour les handles 16 bits.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-111">Therefore, the structure only allowed for 16-bit handles.</span></span> <span data-ttu-id="cfb2b-112">Dans Win32, lorsqu'elle est appelée avec **Excel4** ou **Excel4v**, la fonction **xlGetInst** et la fonction **xlGetHwnd** renvoient uniquement la partie basse de la poignée complète 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-112">In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="cfb2b-113">Dans Excel 2007 et versions ultérieures, lorsque ces fonctions sont appelées avec [Excel12](excel4-excel12.md) ou [Excel12v](excel4v-excel12v.md), le **XLOPER12** renvoyé contient la poignée complète 32 bits.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="cfb2b-114">L'obtention du handle d'instance complet est simple dans n'importe quelle version d'Excel, car il est transmis au service **DllMain**de rappel Windows, qui est appelé lors du chargement de la dll.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-114">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded.</span></span> <span data-ttu-id="cfb2b-115">Si vous enregistrez ce handle d'instance dans une variable globale, vous n'avez jamais besoin d'appeler la fonction **xlGetInst** .</span><span class="sxs-lookup"><span data-stu-id="cfb2b-115">If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="cfb2b-116">Obtention du handle Excel principal dans Excel 2003 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="cfb2b-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="cfb2b-117">Pour obtenir le descripteur Excel principal dans Excel 2003 et les versions antérieures de 32 bits, vous devez d'abord appeler la fonction **xlGetHwnd** afin d'obtenir le mot bas du handle réel.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-117">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle.</span></span> <span data-ttu-id="cfb2b-118">Ensuite, vous devez parcourir la liste des fenêtres de niveau supérieur pour rechercher une correspondance avec le mot bas renvoyé.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-118">Then, you must iterate the list of top-level windows to search for a match with the returned low word.</span></span> <span data-ttu-id="cfb2b-119">Le code suivant illustre la technique.</span><span class="sxs-lookup"><span data-stu-id="cfb2b-119">The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="cfb2b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb2b-120">See also</span></span>



[<span data-ttu-id="cfb2b-121">Affichage des boîtes de dialogue dans un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="cfb2b-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="cfb2b-122">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="cfb2b-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="cfb2b-123">D�veloppement de XLL de Excel 2013</span><span class="sxs-lookup"><span data-stu-id="cfb2b-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

