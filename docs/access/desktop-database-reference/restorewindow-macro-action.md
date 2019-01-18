---
title: RestoreWindow, action de macro
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718832"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="d7e33-102">RestoreWindow, action de macro</span><span class="sxs-lookup"><span data-stu-id="d7e33-102">RestoreWindow macro action</span></span>

<span data-ttu-id="d7e33-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7e33-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d7e33-104">Vous pouvez utiliser l'action **RestaurerFenêtre** pour rétablir la taille initiale d'une fenêtre agrandie ou réduite.</span><span class="sxs-lookup"><span data-stu-id="d7e33-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="d7e33-p101">[!REMARQUE] Cette action ne peut pas être appliquée à des fenêtres Code de Visual Basic Editor. Pour plus d'informations sur la modification des fenêtres Code, consultez la rubrique de la propriété **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="d7e33-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="d7e33-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="d7e33-107">Setting</span></span>

<span data-ttu-id="d7e33-108">L'action **RestaurerFenêtre** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="d7e33-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7e33-109">Notes</span><span class="sxs-lookup"><span data-stu-id="d7e33-109">Remarks</span></span>

<span data-ttu-id="d7e33-p102">Cette action s'applique à l'objet sélectionné. Si un objet a été réduit, vous pouvez d'abord le sélectionner avec l'action **SélectionnerObjet** et rétablir sa taille initiale avec l'action **RestaurerFenêtre**.</span><span class="sxs-lookup"><span data-stu-id="d7e33-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="d7e33-112">Vous pouvez utiliser l'action **DéplacerEtDimensionnerFenêtre** pour déplacer ou dimensionner une fenêtre que vous avez restaurée.</span><span class="sxs-lookup"><span data-stu-id="d7e33-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="d7e33-113">L'action **RestaurerFenêtre** équivaut à cliquer sur le bouton **Restaurer** dans le coin supérieur droit de la fenêtre ou à cliquer sur la commande Restaurer dans le menu **Restaurer** du menu **Contrôle** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="d7e33-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="d7e33-114">Pour exécuter l'action **RestaurerFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Restore** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="d7e33-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

