---
title: Action de macro écho (référence de base de données du bureau Access)
TOCTitle: Echo macro action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 03eeab3884e093b7c22f8fd23d5471d1dc620bc8
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997454"
---
# <a name="echo-macro-action"></a><span data-ttu-id="a3aab-102">Echo, action de macro</span><span class="sxs-lookup"><span data-stu-id="a3aab-102">Echo macro action</span></span>

<span data-ttu-id="a3aab-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3aab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3aab-104">Vous pouvez utiliser l’action **écho** pour spécifier si l’écho est activé.</span><span class="sxs-lookup"><span data-stu-id="a3aab-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="a3aab-105">Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d’une macro pendant son exécution.</span><span class="sxs-lookup"><span data-stu-id="a3aab-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="a3aab-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a3aab-106">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="a3aab-107">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="a3aab-107">This action will not be allowed if the database is not trusted.</span></span>

<span data-ttu-id="a3aab-108">L’action **écho** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="a3aab-108">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3aab-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="a3aab-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a3aab-110">Description</span><span class="sxs-lookup"><span data-stu-id="a3aab-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3aab-111"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-111"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-112">Cliquez sur <strong>Oui</strong> (pour activer l’écho) ou <strong>non</strong> (pour désactiver l’écho) dans la zone <strong>Écho</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-112">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a3aab-113">La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3aab-113">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3aab-114"><strong>Texte de la barre d’état</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-114"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-115">Le texte à afficher dans la barre lorsque l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3aab-115">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="a3aab-116">Par exemple, lorsque l’écho est désactivé, la barre d’état peut afficher &quot;la macro est en cours d’exécution.&quot;</span><span class="sxs-lookup"><span data-stu-id="a3aab-116">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3aab-117">Lors de l’exécution d’une macro, la mise à jour de l’écran affiche souvent des informations qui ne sont pas indispensables pour le fonctionnement de la macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-117">When a macro runs, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="a3aab-118">Lorsque vous définissez l’argument **Écho actif** sur **non**, la macro s’exécute sans mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="a3aab-118">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="a3aab-119">Une fois la macro terminée, Access automatiquement activer l’écho et redessine la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a3aab-119">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="a3aab-120">Le paramètre **non** de l’argument **Écho actif** n’affecte pas la fonctionnalité de la macro ni ses résultats.</span><span class="sxs-lookup"><span data-stu-id="a3aab-120">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="a3aab-121">L’action **écho** ne supprime pas l’affichage des boîtes de dialogue modales, telles que des formulaires indépendants, tels que des feuilles de propriétés ou des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a3aab-121">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="a3aab-122">Vous pouvez utiliser les boîtes de dialogue et formulaires indépendants pour rassembler ou afficher plus d’informations, même si l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a3aab-122">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="a3aab-123">Pour supprimer toutes les boîtes de message ou, à l’exception des boîtes de dialogue qui exigent que l’utilisateur à entrer des informations et des boîtes de message d’erreur, utilisez l’action **avertissements** .</span><span class="sxs-lookup"><span data-stu-id="a3aab-123">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="a3aab-124">Vous pouvez exécuter l’action **écho** plusieurs fois dans une macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-124">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="a3aab-125">Cela vous permet de modifier le texte de barre d’état pendant l’exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-125">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="a3aab-126">Si vous désactivez l’écho, vous pouvez utiliser l’action **Afficherpointeursablier** pour transformer le pointeur de souris en icône de sablier (ou celle que vous avez définie pour « Occupé ») pour fournir une indication visuelle de la macro est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="a3aab-126">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="a3aab-127">Pour exécuter l’action **écho** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Echo** de l’objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="a3aab-127">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="a3aab-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="a3aab-128">Examples</span></span>

### <a name="set-the-value-of-a-control-by-using-a-macro"></a><span data-ttu-id="a3aab-129">Définissez la valeur d'un contrôle en utilisant une macro</span><span class="sxs-lookup"><span data-stu-id="a3aab-129">Set the value of a control by using a macro</span></span>

<span data-ttu-id="a3aab-p107">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a3aab-p107">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3aab-135">Action</span><span class="sxs-lookup"><span data-stu-id="a3aab-135">Action</span></span></p></th>
<th><p><span data-ttu-id="a3aab-136">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="a3aab-136">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a3aab-137">Commentaire</span><span class="sxs-lookup"><span data-stu-id="a3aab-137">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3aab-138"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-138"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-139"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-139"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-140">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-140">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3aab-141"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-141"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-142"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-142"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-143">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="a3aab-143">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3aab-144"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-144"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-145"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-145"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-146">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="a3aab-146">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3aab-147"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-147"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-148"><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</span><span class="sxs-lookup"><span data-stu-id="a3aab-148"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="a3aab-149">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a3aab-149">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3aab-150"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-150"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-151"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="a3aab-151"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="a3aab-152">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="a3aab-152">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="synchronize-forms-by-using-a-macro"></a><span data-ttu-id="a3aab-153">Synchroniser des formulaires à l'aide d'une macro</span><span class="sxs-lookup"><span data-stu-id="a3aab-153">Synchronize forms by using a macro</span></span>

<span data-ttu-id="a3aab-154">La macro suivante ouvre le formulaire liste des produits dans le coin inférieur droit du formulaire fournisseurs, affichant les produits du fournisseur actif.</span><span class="sxs-lookup"><span data-stu-id="a3aab-154">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="a3aab-155">Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**.</span><span class="sxs-lookup"><span data-stu-id="a3aab-155">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="a3aab-156">Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**.</span><span class="sxs-lookup"><span data-stu-id="a3aab-156">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="a3aab-157">Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a3aab-157">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3aab-158">Condition</span><span class="sxs-lookup"><span data-stu-id="a3aab-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="a3aab-159">Action</span><span class="sxs-lookup"><span data-stu-id="a3aab-159">Action</span></span></p></th>
<th><p><span data-ttu-id="a3aab-160">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="a3aab-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a3aab-161">Commentaire</span><span class="sxs-lookup"><span data-stu-id="a3aab-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a3aab-162"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-163"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-164">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3aab-165">IsNull ([Réf fournisseur])</span><span class="sxs-lookup"><span data-stu-id="a3aab-165">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="a3aab-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-167"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="a3aab-167"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="a3aab-168"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="a3aab-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="a3aab-169">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="a3aab-169">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3aab-170">...</span><span class="sxs-lookup"><span data-stu-id="a3aab-170"></span></span></p></td>
<td><p><span data-ttu-id="a3aab-171"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-171"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-172"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="a3aab-172"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="a3aab-173">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="a3aab-173">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3aab-174">...</span><span class="sxs-lookup"><span data-stu-id="a3aab-174"></span></span></p></td>
<td><p><span data-ttu-id="a3aab-175"><strong>ArrêtMacro</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-175"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a3aab-176">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="a3aab-176">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a3aab-177"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-177"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-178"><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [Réf fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-178"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-179">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="a3aab-179">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="a3aab-180"><strong>DéplacerEtDimensionnerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="a3aab-180"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="a3aab-181"><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="a3aab-181"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="a3aab-182">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a3aab-182">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

