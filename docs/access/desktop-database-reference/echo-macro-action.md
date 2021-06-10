---
title: Écho, action de macro (référence de base de données de bureau Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d536ed47c780b7f9f1675a9879e86aeff80b67f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293622"
---
# <a name="echo-macro-action"></a><span data-ttu-id="cd209-102">Echo, action de macro</span><span class="sxs-lookup"><span data-stu-id="cd209-102">Echo macro action</span></span>

<span data-ttu-id="cd209-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd209-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cd209-104">Vous pouvez utiliser l’action **Écho** pour spécifier si l’écho est allumé.</span><span class="sxs-lookup"><span data-stu-id="cd209-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="cd209-105">Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d’une macro pendant qu’elle s’exécute.</span><span class="sxs-lookup"><span data-stu-id="cd209-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="cd209-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="cd209-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="cd209-107">Cette action ne sera pas autorisée si la base de données n’est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="cd209-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="cd209-108">**L’action Écho** a les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="cd209-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd209-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="cd209-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="cd209-110">Description</span><span class="sxs-lookup"><span data-stu-id="cd209-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd209-111"><strong>Écho sur</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-112">Cliquez <strong>sur Oui</strong> (activer l’écho) ou <strong></strong> Non <strong>(désactiver</strong> l’écho) dans la zone Écho sur dans la section Arguments de <strong>l’action</strong> du volet Générateur de macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="cd209-113">La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="cd209-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd209-114"><strong>Texte de la barre d’état</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-115">Texte à afficher dans la barre d’état lorsque l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cd209-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="cd209-116">Par exemple, lorsque l’écho est désactivé, la barre d’état peut afficher &quot; la macro en cours d’exécution.&quot;</span><span class="sxs-lookup"><span data-stu-id="cd209-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd209-117">Lorsqu’une macro s’exécute, la mise à jour de l’écran affiche souvent des informations non essentielles au fonctionnement de la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="cd209-118">Lorsque vous définissez **l’argument Écho sur** **non,** la macro s’exécute sans mettre à jour l’écran.</span><span class="sxs-lookup"><span data-stu-id="cd209-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="cd209-119">À la fin de la macro, Access réessaie automatiquement l’écho et réessaie la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cd209-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="cd209-120">Le **paramètre Non** de l’argument Écho **sur** n’affecte pas la fonctionnalité de la macro ou ses résultats.</span><span class="sxs-lookup"><span data-stu-id="cd209-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="cd209-121">**L’action Écho** ne supprime pas l’affichage des boîtes de dialogue modales, telles que les messages d’erreur, ou les formulaires de fenêtre publicitaire, tels que les feuilles de propriétés.</span><span class="sxs-lookup"><span data-stu-id="cd209-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="cd209-122">Vous pouvez utiliser des boîtes de dialogue et des formulaires pop-up pour collecter ou afficher des informations, même si l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="cd209-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="cd209-123">Pour supprimer tous les messages ou boîtes de dialogue à l’exception des boîtes de dialogue et des boîtes de dialogue d’erreur qui exigent que l’utilisateur entre des informations, utilisez l’action **DéfinirWarnings.**</span><span class="sxs-lookup"><span data-stu-id="cd209-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="cd209-124">Vous pouvez exécuter l’action **Écho** plusieurs fois dans une macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="cd209-125">Cela vous permet de modifier le texte de la barre d’état pendant l’exécutement de la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="cd209-126">Si vous éteinez l’écho, vous pouvez utiliser l’action **DisplayHourglassPointer** pour transformer le pointeur de la souris en icône de sablier (ou toute icône de pointeur de souris que vous avez définie pour « Occupé ») afin de fournir une indication visuelle de l’exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="cd209-127">Pour exécuter l’action **Écho** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Echo** de l’objet **DoCmd.**</span><span class="sxs-lookup"><span data-stu-id="cd209-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="cd209-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="cd209-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="cd209-129">Définissez la valeur d’un contrôle en utilisant une macro</span><span class="sxs-lookup"><span data-stu-id="cd209-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="cd209-p107">La macro suivante ouvre le formulaire Ajouter des produits à partir d’un bouton dans le formulaire Fournisseurs. Elle présente l’utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L’action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L’action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cd209-p107">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd209-135">Action</span><span class="sxs-lookup"><span data-stu-id="cd209-135">Action</span></span></p></th>
<th><p><span data-ttu-id="cd209-136">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="cd209-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="cd209-137">Commentaire</span><span class="sxs-lookup"><span data-stu-id="cd209-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd209-138"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-139"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-140">Arrêter l’actualisation de l’écran pendant l’exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd209-141"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-142"><strong>Type d’objet</strong> : <strong>FormulaireNom de l’objet</strong> : Liste des produits <strong>Enregistrer</strong> : <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-143">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="cd209-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd209-144"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-145"><strong>Nom du formulaire</strong> : Produits <strong>Affichage</strong> : <strong>FormulaireMode de données</strong> : <strong>AjouterMode Fenêtre</strong> :<strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-146">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="cd209-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd209-147"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-148"><strong>Élément</strong>: [Forms]![Produits]! [N° fournisseur] <strong>Expression</strong>: N° fournisseur    </span><span class="sxs-lookup"><span data-stu-id="cd209-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="cd209-149">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cd209-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd209-150"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-151"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="cd209-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="cd209-152">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="cd209-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="cd209-153">Synchroniser des formulaires à l’aide d’une macro</span><span class="sxs-lookup"><span data-stu-id="cd209-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="cd209-154">La macro suivante ouvre le formulaire Liste des produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="cd209-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="cd209-155">Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**.</span><span class="sxs-lookup"><span data-stu-id="cd209-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="cd209-156">Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**.</span><span class="sxs-lookup"><span data-stu-id="cd209-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="cd209-157">Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cd209-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd209-158">Condition</span><span class="sxs-lookup"><span data-stu-id="cd209-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="cd209-159">Action</span><span class="sxs-lookup"><span data-stu-id="cd209-159">Action</span></span></p></th>
<th><p><span data-ttu-id="cd209-160">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="cd209-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="cd209-161">Commentaire</span><span class="sxs-lookup"><span data-stu-id="cd209-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="cd209-162"><strong>Echo</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-163"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-164">Arrêter l’actualisation de l’écran pendant l’exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd209-165">IsNull([ID fournisseur])</span><span class="sxs-lookup"><span data-stu-id="cd209-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="cd209-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-167"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="cd209-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="cd209-168"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionner un fournisseur</span><span class="sxs-lookup"><span data-stu-id="cd209-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="cd209-169">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="cd209-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd209-170">...</span><span class="sxs-lookup"><span data-stu-id="cd209-170">...</span></span></p></td>
<td><p><span data-ttu-id="cd209-171"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-172"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="cd209-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="cd209-173">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="cd209-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd209-174">...</span><span class="sxs-lookup"><span data-stu-id="cd209-174">...</span></span></p></td>
<td><p><span data-ttu-id="cd209-175"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="cd209-176">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="cd209-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="cd209-177"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-178"><strong>Nom du formulaire</strong>: Affichage de la liste <strong>des</strong>produits : Nom <strong>de DatasheetFilter</strong>: <strong>Condition where</strong>: [ID fournisseur] = [Formulaires]! [Fournisseurs]! [SupplierID] <strong>Mode données</strong>: <strong>mode Lecture seule :</strong> <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-179">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="cd209-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="cd209-180"><strong>MoveAndSizeWindow</strong></span><span class="sxs-lookup"><span data-stu-id="cd209-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="cd209-181"><strong>Droite</strong>: 0,7799 &quot; <strong>Bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="cd209-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="cd209-182">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="cd209-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

