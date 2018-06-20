---
title: Affichage des boîtes de dialogue à partir d’une DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [excel 2007], affichage des boîtes de dialogue, boîtes de dialogue [Excel 2007], affichage à partir d’une DLL ou XLL, affichage des boîtes de dialogue à partir de DLL [Excel 2007],
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: afb21125bc54a2607a997c7b2f7c73ef2f528f28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782028"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="440f1-104">Affichage des boîtes de dialogue à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="440f1-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="440f1-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="440f1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="440f1-106">Pour afficher une boîte de dialogue Win32 à l’aide, par exemple, la fonction Windows SDK **DialogBox**, vous devez d’abord obtenir l’instance 32 bits complète et les poignées de la fenêtre principale pour Excel.</span><span class="sxs-lookup"><span data-stu-id="440f1-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="440f1-107">Pour plus d’informations, voir [accès Instance d’Excel et gère les fenêtre principale](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="440f1-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="440f1-108">En supposant que votre projet contienne la ressource de boîte de dialogue, vous devez effectuer plusieurs étapes de la routine de gestion des messages à celle de la boîte de dialogue affiché et pour restaurer le message Excel routine de gestion des lors de la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="440f1-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="440f1-109">La commande d’exemple [fShowDialog](fshowdialog.md) dans le projet générique illustre l’utilisation des fonctions Windows pour ce faire correctement.</span><span class="sxs-lookup"><span data-stu-id="440f1-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="440f1-110">Vous pouvez également afficher les boîtes de dialogue sans avoir à utiliser les fonctions du Kit de développement Windows à l’aide de l’API C.</span><span class="sxs-lookup"><span data-stu-id="440f1-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="440f1-111">Toutefois, les fonctionnalités de boîte de dialogue de l’API C sont limitées par rapport à ceux de Windows, Visual Basic pour Applications (VBA) ou les Classes MFC (Microsoft Foundation).</span><span class="sxs-lookup"><span data-stu-id="440f1-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="440f1-112">(Par exemple, les boîtes de dialogue API C sont toujours modales).</span><span class="sxs-lookup"><span data-stu-id="440f1-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="440f1-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="440f1-113">See also</span></span>



[<span data-ttu-id="440f1-114">Cr�ation de XLL</span><span class="sxs-lookup"><span data-stu-id="440f1-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="440f1-115">D�veloppement de DLL</span><span class="sxs-lookup"><span data-stu-id="440f1-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="440f1-116">Instance d’Excel Access et les poignées de la fenêtre principale</span><span class="sxs-lookup"><span data-stu-id="440f1-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="440f1-117">Fonctions de l’API C qui peuvent être appelées uniquement à partir d’une DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="440f1-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

