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
ms.openlocfilehash: dfd7877ff1db960afcbf864f1e72ff01b12e8f09
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998951"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="cfa89-102">RestoreWindow, action de macro</span><span class="sxs-lookup"><span data-stu-id="cfa89-102">RestoreWindow macro action</span></span>

<span data-ttu-id="cfa89-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cfa89-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cfa89-104">Vous pouvez utiliser l'action **RestaurerFenêtre** pour rétablir la taille initiale d'une fenêtre agrandie ou réduite.</span><span class="sxs-lookup"><span data-stu-id="cfa89-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>

> [!NOTE]
> <span data-ttu-id="cfa89-p101">[!REMARQUE] Cette action ne peut pas être appliquée à des fenêtres Code de Visual Basic Editor. Pour plus d'informations sur la modification des fenêtres Code, consultez la rubrique de la propriété **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="cfa89-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="cfa89-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cfa89-107">Setting</span></span>

<span data-ttu-id="cfa89-108">L'action **RestaurerFenêtre** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="cfa89-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfa89-109">Notes</span><span class="sxs-lookup"><span data-stu-id="cfa89-109">Remarks</span></span>

<span data-ttu-id="cfa89-p102">Cette action s'applique à l'objet sélectionné. Si un objet a été réduit, vous pouvez d'abord le sélectionner avec l'action **SélectionnerObjet** et rétablir sa taille initiale avec l'action **RestaurerFenêtre**.</span><span class="sxs-lookup"><span data-stu-id="cfa89-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="cfa89-112">Vous pouvez utiliser l'action **DéplacerEtDimensionnerFenêtre** pour déplacer ou dimensionner une fenêtre que vous avez restaurée.</span><span class="sxs-lookup"><span data-stu-id="cfa89-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="cfa89-113">L'action **RestaurerFenêtre** équivaut à cliquer sur le bouton **Restaurer** dans le coin supérieur droit de la fenêtre ou à cliquer sur la commande Restaurer dans le menu **Restaurer** du menu **Contrôle** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cfa89-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="cfa89-114">Pour exécuter l'action **RestaurerFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Restore** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="cfa89-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

