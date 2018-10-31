---
title: Action de Macro écho (référence de base de données du bureau Access)
TOCTitle: Echo Macro Action
ms:assetid: 38dfb2cf-8db5-44b3-91fa-e490932b940b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192516(v=office.15)
ms:contentKeyID: 48544227
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39471ea4bab2ec1bbeb8cd22ecb00aa5df3bc411
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863968"
---
# <a name="echo-macro-action"></a><span data-ttu-id="72716-102">Action de Macro écho</span><span class="sxs-lookup"><span data-stu-id="72716-102">Echo Macro Action</span></span>


<span data-ttu-id="72716-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72716-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72716-104">Vous pouvez utiliser l’action **écho** pour spécifier si l’écho est activé.</span><span class="sxs-lookup"><span data-stu-id="72716-104">You can use the **Echo** action to specify whether echo is turned on.</span></span> <span data-ttu-id="72716-105">Par exemple, vous pouvez utiliser cette action pour masquer ou afficher les résultats d’une macro pendant son exécution.</span><span class="sxs-lookup"><span data-stu-id="72716-105">For example, you can use this action to hide or show the results of a macro while it runs.</span></span>

## <a name="setting"></a><span data-ttu-id="72716-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="72716-106">Setting</span></span>


> [!NOTE]
> <span data-ttu-id="72716-p102">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="72716-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span>



<span data-ttu-id="72716-109">L’action **écho** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="72716-109">The **Echo** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72716-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="72716-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="72716-111">Description</span><span class="sxs-lookup"><span data-stu-id="72716-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72716-112"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="72716-112"><strong>Echo On</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-113">Cliquez sur <strong>Oui</strong> (pour activer l’écho) ou <strong>non</strong> (pour désactiver l’écho) dans la zone <strong>Écho</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro.</span><span class="sxs-lookup"><span data-stu-id="72716-113">Click <strong>Yes</strong> (turn echo on) or <strong>No</strong> (turn echo off) in the <strong>Echo On</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="72716-114">La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="72716-114">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72716-115"><strong>Texte de la barre d’état</strong></span><span class="sxs-lookup"><span data-stu-id="72716-115"><strong>Status Bar Text</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-116">Le texte à afficher dans la barre lorsque l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="72716-116">The text to display in the status bar when echo is turned off.</span></span> <span data-ttu-id="72716-117">Par exemple, lorsque l’écho est désactivé, la barre d’état peut afficher &quot;la macro est en cours d’exécution.&quot;</span><span class="sxs-lookup"><span data-stu-id="72716-117">For example, when echo is turned off, the status bar can display &quot;The macro is running.&quot;</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72716-118">S’exécute une macro, la mise à jour souvent affiche des informations pas indispensable au fonctionnement de la macro.</span><span class="sxs-lookup"><span data-stu-id="72716-118">When runs a macro, screen updating often shows information not essential to the functioning of the macro.</span></span> <span data-ttu-id="72716-119">Lorsque vous définissez l’argument **Écho actif** sur **non**, la macro s’exécute sans mise à jour de l’écran.</span><span class="sxs-lookup"><span data-stu-id="72716-119">When you set the **Echo On** argument to **No**, the macro runs without updating the screen.</span></span> <span data-ttu-id="72716-120">Une fois la macro terminée, Access automatiquement activer l’écho et redessine la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="72716-120">When the macro finishes, Access automatically turns echo back on and repaints the window.</span></span> <span data-ttu-id="72716-121">Le paramètre **non** de l’argument **Écho actif** n’affecte pas la fonctionnalité de la macro ni ses résultats.</span><span class="sxs-lookup"><span data-stu-id="72716-121">The **No** setting for the **Echo On** argument doesn't affect the functionality of the macro or its results.</span></span>

<span data-ttu-id="72716-122">L’action **écho** ne supprime pas l’affichage des boîtes de dialogue modales, telles que des formulaires indépendants, tels que des feuilles de propriétés ou des messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="72716-122">The **Echo** action doesn't suppress the display of modal dialog boxes, such as error messages, or pop-up forms, such as property sheets.</span></span> <span data-ttu-id="72716-123">Vous pouvez utiliser les boîtes de dialogue et formulaires indépendants pour rassembler ou afficher plus d’informations, même si l’écho est désactivé.</span><span class="sxs-lookup"><span data-stu-id="72716-123">You can use dialog boxes and pop-up forms to gather or display information, even if echo is turned off.</span></span> <span data-ttu-id="72716-124">Pour supprimer toutes les boîtes de message ou, à l’exception des boîtes de dialogue qui exigent que l’utilisateur à entrer des informations et des boîtes de message d’erreur, utilisez l’action **avertissements** .</span><span class="sxs-lookup"><span data-stu-id="72716-124">To suppress all message or dialog boxes except error message boxes and dialog boxes that require the user to enter information, use the **SetWarnings** action.</span></span>

<span data-ttu-id="72716-125">Vous pouvez exécuter l’action **écho** plusieurs fois dans une macro.</span><span class="sxs-lookup"><span data-stu-id="72716-125">You can run the **Echo** action more than once in a macro.</span></span> <span data-ttu-id="72716-126">Cela vous permet de modifier le texte de barre d’état pendant l’exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="72716-126">This allows you to change the status bar text while the macro runs.</span></span>

<span data-ttu-id="72716-127">Si vous désactivez l’écho, vous pouvez utiliser l’action **Afficherpointeursablier** pour transformer le pointeur de souris en icône de sablier (ou celle que vous avez définie pour « Occupé ») pour fournir une indication visuelle de la macro est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="72716-127">If you turn echo off, you can use the **DisplayHourglassPointer** action to change the mouse pointer into an hourglass icon (or whatever mouse pointer icon you've set for "Busy") to provide a visual indication that the macro is running.</span></span>

<span data-ttu-id="72716-128">Pour exécuter l’action **écho** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **Echo** de l’objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="72716-128">To run the **Echo** action in a Visual Basic for Applications (VBA) module, use the **Echo** method of the **DoCmd** object.</span></span>

## <a name="examples"></a><span data-ttu-id="72716-129">Exemples</span><span class="sxs-lookup"><span data-stu-id="72716-129">Examples</span></span>

<span data-ttu-id="72716-130">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="72716-130">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="72716-p108">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="72716-p108">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72716-136">Action</span><span class="sxs-lookup"><span data-stu-id="72716-136">Action</span></span></p></th>
<th><p><span data-ttu-id="72716-137">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="72716-137">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="72716-138">Commentaire</span><span class="sxs-lookup"><span data-stu-id="72716-138">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="72716-139"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="72716-139"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-140"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="72716-140"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-141">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="72716-141">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72716-142"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="72716-142"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-143"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="72716-143"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-144">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="72716-144">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72716-145"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="72716-145"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-146"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="72716-146"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-147">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="72716-147">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72716-148"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="72716-148"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-149"><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</span><span class="sxs-lookup"><span data-stu-id="72716-149"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="72716-150">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="72716-150">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72716-151"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="72716-151"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-152"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="72716-152"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="72716-153">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="72716-153">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="72716-154">**Synchroniser des formulaires à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="72716-154">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="72716-155">La macro suivante ouvre le formulaire liste des produits dans le coin inférieur droit du formulaire fournisseurs, affichant les produits du fournisseur actif.</span><span class="sxs-lookup"><span data-stu-id="72716-155">The following macro opens the Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products.</span></span> <span data-ttu-id="72716-156">Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**.</span><span class="sxs-lookup"><span data-stu-id="72716-156">It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions.</span></span> <span data-ttu-id="72716-157">Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**.</span><span class="sxs-lookup"><span data-stu-id="72716-157">It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions.</span></span> <span data-ttu-id="72716-158">Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="72716-158">This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="72716-159">Condition</span><span class="sxs-lookup"><span data-stu-id="72716-159">Condition</span></span></p></th>
<th><p><span data-ttu-id="72716-160">Action</span><span class="sxs-lookup"><span data-stu-id="72716-160">Action</span></span></p></th>
<th><p><span data-ttu-id="72716-161">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="72716-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="72716-162">Commentaire</span><span class="sxs-lookup"><span data-stu-id="72716-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="72716-163"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="72716-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-164"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="72716-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-165">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="72716-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72716-166">IsNull ([Réf fournisseur])</span><span class="sxs-lookup"><span data-stu-id="72716-166">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="72716-167"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="72716-167"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-168"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="72716-168"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="72716-169"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="72716-169"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="72716-170">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="72716-170">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="72716-171">...</span><span class="sxs-lookup"><span data-stu-id="72716-171"></span></span></p></td>
<td><p><span data-ttu-id="72716-172"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="72716-172"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-173"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="72716-173"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="72716-174">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="72716-174">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="72716-175">...</span><span class="sxs-lookup"><span data-stu-id="72716-175"></span></span></p></td>
<td><p><span data-ttu-id="72716-176"><strong>ArrêtMacro</strong></span><span class="sxs-lookup"><span data-stu-id="72716-176"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="72716-177">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="72716-177">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="72716-178"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="72716-178"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-179"><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [Réf fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="72716-179"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-180">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="72716-180">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="72716-181"><strong>DéplacerEtDimensionnerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="72716-181"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="72716-182"><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="72716-182"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="72716-183">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="72716-183">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

