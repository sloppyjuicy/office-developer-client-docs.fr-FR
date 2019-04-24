---
title: Affichage des boîtes de dialogue dans un fichier DLL ou XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- XLL [Excel 2007], affichage des boîtes de dialogue à partir de, boîtes de dialogue [Excel 2007], affichage à partir d'un fichier DLL ou XLL, dll [Excel 2007], affichage des boîtes de dialogue à partir de
localization_priority: Normal
ms.assetid: e77ac555-331d-41c8-a000-7b178959754d
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 7b00430b047fe792afef701d210ccde06dd16216
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310934"
---
# <a name="displaying-dialog-boxes-from-within-a-dll-or-xll"></a><span data-ttu-id="66145-104">Affichage des boîtes de dialogue dans un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="66145-104">Displaying Dialog Boxes from Within a DLL or XLL</span></span>

 <span data-ttu-id="66145-105">**S’applique à**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="66145-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="66145-106">Pour afficher une boîte de dialogue Win32 en utilisant, par exemple, la fonction **DialogBox**du kit de développement logiciel (SDK) Windows, vous devez d'abord obtenir l'instance complète de 32 bits et les principaux handles de fenêtre pour Excel.</span><span class="sxs-lookup"><span data-stu-id="66145-106">To display a Win32 dialog box using, for example, the Windows SDK function **DialogBox**, you must first obtain the full 32-bit instance and main window handles for Excel.</span></span> <span data-ttu-id="66145-107">Pour plus d'informations, consultez la rubrique [Access Excel instance and principal Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span><span class="sxs-lookup"><span data-stu-id="66145-107">For more information, see [Access Excel Instance and Main Window Handles](how-to-access-excel-instance-and-main-window-handles.md).</span></span> 
  
<span data-ttu-id="66145-108">En supposant que votre projet contient la ressource de la boîte de dialogue, vous devez effectuer plusieurs étapes pour définir la routine de gestion des messages sur celle de la boîte de dialogue nouvellement affichée et pour restaurer la routine de gestion des messages Excel lors de la fermeture de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="66145-108">Assuming your project contains the dialog box resource, you must take several steps to set the message-handling routine to that of the newly displayed dialog box and to restore the Excel message handling routine when the dialog box is closed.</span></span> <span data-ttu-id="66145-109">L'exemple de commande [fShowDialog](fshowdialog.md) dans le projet générique illustre l'utilisation des fonctions Windows pour effectuer correctement cette opération.</span><span class="sxs-lookup"><span data-stu-id="66145-109">The example command [fShowDialog](fshowdialog.md) in the Generic project demonstrates the use of the Windows functions to do this correctly.</span></span> 
  
<span data-ttu-id="66145-110">Vous pouvez également afficher des boîtes de dialogue à l'aide de l'API C sans avoir à utiliser les fonctions du kit de développement logiciel Windows.</span><span class="sxs-lookup"><span data-stu-id="66145-110">You can also display dialog boxes using the C API without having to use Windows SDK functions.</span></span> <span data-ttu-id="66145-111">Toutefois, les fonctionnalités de boîte de dialogue de l'API C sont très limitées par rapport à celles de Windows, de Visual Basic pour applications (VBA) ou de Microsoft Foundation classes (MFC).</span><span class="sxs-lookup"><span data-stu-id="66145-111">However, the dialog box capabilities of the C API are very limited compared with those of Windows, Visual Basic for Applications (VBA), or the Microsoft Foundation Classes (MFC).</span></span> <span data-ttu-id="66145-112">(Par exemple, les boîtes de dialogue de l'API C sont toujours modales).</span><span class="sxs-lookup"><span data-stu-id="66145-112">(For example, C API dialog boxes are always modal).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66145-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="66145-113">See also</span></span>



[<span data-ttu-id="66145-114">Création de XLL</span><span class="sxs-lookup"><span data-stu-id="66145-114">Creating XLLs</span></span>](creating-xlls.md)
  
[<span data-ttu-id="66145-115">D�veloppement de DLL</span><span class="sxs-lookup"><span data-stu-id="66145-115">Developing DLLs</span></span>](developing-dlls.md)
  
[<span data-ttu-id="66145-116">Accès à l’instance Excel et aux handles de fenêtre principaux</span><span class="sxs-lookup"><span data-stu-id="66145-116">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
[<span data-ttu-id="66145-117">Fonctions de l’API C à appeler à partir d’un fichier DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="66145-117">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

