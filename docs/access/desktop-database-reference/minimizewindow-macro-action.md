---
title: MinimizeWindow, action de macro
TOCTitle: MinimizeWindow macro action
ms:assetid: 3a92b654-15ce-1ed1-63e0-eed927dbe26c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192648(v=office.15)
ms:contentKeyID: 48544265
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm174420
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c1c8cb8d0f1166b63031925a02186ebc8a1bdac2
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996712"
---
# <a name="minimizewindow-macro-action"></a><span data-ttu-id="34a88-102">MinimizeWindow, action de macro</span><span class="sxs-lookup"><span data-stu-id="34a88-102">MinimizeWindow macro action</span></span>

<span data-ttu-id="34a88-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="34a88-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34a88-104">Si Access est configuré pour utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Réduirefenêtre** pour réduire la fenêtre active à une barre de titre en bas de la fenêtre Access.</span><span class="sxs-lookup"><span data-stu-id="34a88-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MinimizeWindow** action to reduce the active window to a small title bar at the bottom of the Access window.</span></span>

> [!NOTE]
> <span data-ttu-id="34a88-p101">[!REMARQUE] Cette action ne peut être appliquée aux fenêtres de code dans Visual Basic Editor. Pour plus d'informations sur la façon d'affecter des fenêtres de code, reportez-vous à la rubrique relative à la propriété **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="34a88-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="34a88-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="34a88-107">Setting</span></span>

<span data-ttu-id="34a88-108">L'action **RéduireFenêtre** ne possède aucun argument.</span><span class="sxs-lookup"><span data-stu-id="34a88-108">The **MinimizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="34a88-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="34a88-109">Remarks</span></span>

<span data-ttu-id="34a88-p102">Vous pouvez utiliser cette action pour supprimer une fenêtre de l'écran tout en laissant l'objet ouvert ou pour ouvrir un objet sans afficher sa fenêtre. Pour afficher l'objet, utilisez l'action **SélectionnerObjet** avec l'action **AgrandirFenêtre** ou **RestaurerFenêtre**. L'action **RestaurerFenêtre** rétablit la taille initiale d'une fenêtre réduite.</span><span class="sxs-lookup"><span data-stu-id="34a88-p102">You can use this action to remove a window from the screen while leaving the object open. You can also use this action to open an object without displaying its window. To display the object, use the **SelectObject** action with either the **MaximizeWindow** or **RestoreWindow** action. The **RestoreWindow** action restores a minimized window to its previous size.</span></span>

<span data-ttu-id="34a88-114">L'action **RéduireFenêtre** équivaut à cliquer sur le bouton **Réduire** dans le coin supérieur droit de la fenêtre ou à cliquer sur **Réduire** dans le menu **Contrôle** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="34a88-114">The **MinimizeWindow** action has the same effect as clicking the **Minimize** button in the window's upper-right corner or clicking **Minimize** on the window's **Control** menu.</span></span>

<span data-ttu-id="34a88-115">**Conseils**</span><span class="sxs-lookup"><span data-stu-id="34a88-115">**Tips**</span></span>

- <span data-ttu-id="34a88-116">Vous devrez peut-être commencer par utiliser la méthode **SélectionnerObjet** si la fenêtre que vous voulez réduire n'est pas la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="34a88-116">You may first need to use the **SelectObject** action if the window you want to minimize isn't the active window.</span></span>

- <span data-ttu-id="34a88-p103">Pour masquer le volet de navigation, utilisez l'action **SélectionnerObjet** avec l'argument DansVoletDeNavigation défini sur **Oui**, puis utilisez l'action **RéduireFenêtre**. L'objet sélectionné dans l'action **SélectionnerObjet** peut être tout objet de la base de données.</span><span class="sxs-lookup"><span data-stu-id="34a88-p103">To hide the Navigation Pane, use the **SelectObject** action with the In Navigation Pane argument set to **Yes** and then use the **MinimizeWindow** action. The object you select in the **SelectObject** action can be any object in the database.</span></span>

- <span data-ttu-id="34a88-p104">Vous pouvez masquer la fenêtre active en cliquant sur **Gérer cette fenêtre** dans le menu **Affichage**, puis en cliquant sur **Masquer**. Au lieu d'être réduite en icône, la fenêtre devient invisible. Utilisez la commande **Afficher** du même menu pour faire réapparaître la fenêtre. Vous pouvez utiliser l'action **ExécuterCommandeMenu** pour exécuter l'une ou l'autre de ces commandes depuis une macro.</span><span class="sxs-lookup"><span data-stu-id="34a88-p104">You can hide the active window by clicking **Manage This Window** on the **View** menu, and then clicking **Hide**. Instead of being reduced to an icon, the window becomes invisible. Use the **Unhide** command on the same menu to make the window reappear. You can use the **RunMenuCommand** action to carry out either of these commands from a macro.</span></span>

- <span data-ttu-id="34a88-123">Vous pouvez également utiliser l'action **DéfinirValeur** pour définir la propriété **Visible** d'un formulaire de manière à masquer ou afficher la fenêtre du formulaire.</span><span class="sxs-lookup"><span data-stu-id="34a88-123">You can also use the **SetValue** action to set a form's **Visible** property to hide or show the form's window.</span></span>

<span data-ttu-id="34a88-124">Pour exécuter l'action **RéduireFenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Minimize** de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="34a88-124">To run the **MinimizeWindow** action in a Visual Basic for Applications (VBA) module, use the **Minimize** method of the **DoCmd** object.</span></span>

