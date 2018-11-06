---
title: MoveAndSizeWindow, action de macro
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8737de80c38626b72933eb15a59e08ab0452ce74
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998811"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="74482-102">MoveAndSizeWindow, action de macro</span><span class="sxs-lookup"><span data-stu-id="74482-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="74482-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="74482-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="74482-104">Si vous avez défini votre document options de la fenêtre à utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l’action **Déplaceretdimensionnerfenêtre** pour déplacer ou redimensionner la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="74482-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="74482-105">Pour plus d’informations sur la façon de définir les options de fenêtre de document, voir la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="74482-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="74482-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="74482-106">Setting</span></span>

<span data-ttu-id="74482-107">L’action **Déplaceretdimensionnerfenêtre** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="74482-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74482-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="74482-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="74482-109">Description</span><span class="sxs-lookup"><span data-stu-id="74482-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="74482-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="74482-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-111">Nouvelle position horizontale de l'angle supérieur gauche de la fenêtre mesurée depuis le bord gauche de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="74482-112">Dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro, entrez la position dans la zone de <strong>droite</strong> .</span><span class="sxs-lookup"><span data-stu-id="74482-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74482-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="74482-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-114">Nouvelle position verticale de l'angle supérieur gauche de la fenêtre mesurée depuis le haut de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="74482-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="74482-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-116">Nouvelle largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74482-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="74482-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-118">Nouvelle hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="74482-119">Si vous laissez un argument vierge, Microsoft Access utilise la valeur actuelle de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="74482-120">Vous devez entrer une valeur pour au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="74482-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="74482-121">Chaque mesure est exprimée en pouces ou en centimètres, selon les paramètres régionaux du Panneau de configuration Windows.</span><span class="sxs-lookup"><span data-stu-id="74482-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="74482-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="74482-122">Remarks</span></span>

<span data-ttu-id="74482-123">Pour configurer une application pour utiliser des fenêtres superposées au lieu des documents à onglets, utilisez la procédure suivante :</span><span class="sxs-lookup"><span data-stu-id="74482-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="74482-124">Cliquez sur **Options**</span><span class="sxs-lookup"><span data-stu-id="74482-124">Click **Options**</span></span>

2.  <span data-ttu-id="74482-125">Cliquez sur **base de données Active**.</span><span class="sxs-lookup"><span data-stu-id="74482-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="74482-126">Dans la section **Options de l'application**, sous **Options de la fenêtre Document**, cliquez sur **Fenêtres superposées**.</span><span class="sxs-lookup"><span data-stu-id="74482-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="74482-127">Cliquez sur **OK**, puis fermez et rouvrez la base de données.</span><span class="sxs-lookup"><span data-stu-id="74482-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="74482-128">Cette action équivaut à cliquer sur **déplacer** ou **taille** sur le **contrôle de** menu fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="74482-129">Avec les commandes de menu, vous utilisez les touches de direction pour déplacer ou pour redimensionner la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="74482-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="74482-130">Avec l’action **Déplaceretdimensionnerfenêtre** , vous entrez directement les mesures de position et de taille.</span><span class="sxs-lookup"><span data-stu-id="74482-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="74482-131">Vous pouvez également utiliser la souris pour déplacer et dimensionner des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="74482-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="74482-132">Vous pouvez utiliser cette action sur n’importe quelle fenêtre, dans n’importe quel mode.</span><span class="sxs-lookup"><span data-stu-id="74482-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="74482-133">Pour déplacer une fenêtre sans la dimensionner, entrez des valeurs pour la **droite** et **bas** arguments, mais laissez les arguments **largeur** et **hauteur** vide.</span><span class="sxs-lookup"><span data-stu-id="74482-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="74482-134">Pour redimensionner une fenêtre sans la déplacer, entrez des valeurs pour la **largeur** et la **hauteur** arguments, mais laissez les arguments **droite** et **bas** vide.</span><span class="sxs-lookup"><span data-stu-id="74482-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="74482-135">Pour exécuter l’action **Déplaceretdimensionnerfenêtre** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **MoveSize** de l’objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="74482-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="74482-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="74482-136">Example</span></span>

<span data-ttu-id="74482-137">**Synchroniser des formulaires à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="74482-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="74482-p104">La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="74482-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="74482-142">Condition</span><span class="sxs-lookup"><span data-stu-id="74482-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="74482-143">Action</span><span class="sxs-lookup"><span data-stu-id="74482-143">Action</span></span></p></th>
<th><p><span data-ttu-id="74482-144">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="74482-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="74482-145">Commentaire</span><span class="sxs-lookup"><span data-stu-id="74482-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="74482-146"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="74482-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-147"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="74482-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-148">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="74482-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74482-149">IsNull ([Réf fournisseur])</span><span class="sxs-lookup"><span data-stu-id="74482-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="74482-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="74482-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-151"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="74482-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="74482-152"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="74482-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="74482-153">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="74482-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="74482-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="74482-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-155"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="74482-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="74482-156">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="74482-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="74482-157">...</span><span class="sxs-lookup"><span data-stu-id="74482-157"></span></span></p></td>
<td><p><span data-ttu-id="74482-158"><strong>ArrêtMacro</strong></span><span class="sxs-lookup"><span data-stu-id="74482-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="74482-159">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="74482-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="74482-160"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="74482-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-161"><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [Réf fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="74482-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-162">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="74482-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="74482-163"><strong>DéplacerEtDimensionnerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="74482-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="74482-164"><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="74482-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="74482-165">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="74482-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

