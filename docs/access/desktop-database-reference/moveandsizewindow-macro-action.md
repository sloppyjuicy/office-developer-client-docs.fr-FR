---
title: MoveAndSizeWindow, action de macro
TOCTitle: MoveAndSizeWindow macro action
ms:assetid: 86bcf45f-90ce-4ca2-a7fb-efbe5347d137
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197001(v=office.15)
ms:contentKeyID: 48546090
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c1b127995a2f9a0af7da80e9df862259b570870e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288805"
---
# <a name="moveandsizewindow-macro-action"></a><span data-ttu-id="86b07-102">MoveAndSizeWindow, action de macro</span><span class="sxs-lookup"><span data-stu-id="86b07-102">MoveAndSizeWindow macro action</span></span>

<span data-ttu-id="86b07-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86b07-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86b07-104">Si vous avez défini les options de la fenêtre de document de manière à utiliser des fenêtres superposées au lieu des documents à onglets, vous pouvez utiliser l'action **déplaceretdimensionnerfenêtre** pour déplacer ou redimensionner la fenêtre active.</span><span class="sxs-lookup"><span data-stu-id="86b07-104">If you have set your document window options to use overlapping windows instead of tabbed documents, you can use the **MoveAndSizeWindow** action to move or resize the active window.</span></span> <span data-ttu-id="86b07-105">Pour plus d'informations sur la définition des options de la fenêtre de document, voir la section Notes.</span><span class="sxs-lookup"><span data-stu-id="86b07-105">For information on how to set document window options, see the Remarks section.</span></span>

## <a name="setting"></a><span data-ttu-id="86b07-106">Setting</span><span class="sxs-lookup"><span data-stu-id="86b07-106">Setting</span></span>

<span data-ttu-id="86b07-107">L'action **déplaceretdimensionnerfenêtre** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="86b07-107">The **MoveAndSizeWindow** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86b07-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="86b07-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="86b07-109">Description</span><span class="sxs-lookup"><span data-stu-id="86b07-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86b07-110"><strong>Right</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-110"><strong>Right</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-111">Nouvelle position horizontale de l'angle supérieur gauche de la fenêtre mesurée depuis le bord gauche de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-111">The new horizontal position of the window's upper-left corner, measured from the left edge of its containing window.</span></span> <span data-ttu-id="86b07-112">Entrez la position dans la zone de <strong>droite</strong> dans la section arguments de l' <strong>action</strong> du volet générateur de macro.</span><span class="sxs-lookup"><span data-stu-id="86b07-112">Enter the position in the <strong>Right</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b07-113"><strong>Down</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-113"><strong>Down</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-114">Nouvelle position verticale de l'angle supérieur gauche de la fenêtre mesurée depuis le haut de cette fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-114">The new vertical position of the window's upper-left corner, measured from the top edge of its containing window.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86b07-115"><strong>Width</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-115"><strong>Width</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-116">Nouvelle largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-116">The window's new width.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b07-117"><strong>Height</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-117"><strong>Height</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-118">Nouvelle hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-118">The window's new height.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86b07-119">Si vous laissez un argument vide, Microsoft Access utilise le paramètre actuel de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-119">If you leave an argument blank, Microsoft Access uses the window's current setting.</span></span>

<span data-ttu-id="86b07-120">Vous devez entrer une valeur pour au moins un argument.</span><span class="sxs-lookup"><span data-stu-id="86b07-120">You must enter a value for at least one argument.</span></span>

> [!NOTE]
> <span data-ttu-id="86b07-121">Chaque mesure est exprimée en pouces ou en centimètres, selon les paramètres régionaux définis dans le panneau de configuration de Windows.</span><span class="sxs-lookup"><span data-stu-id="86b07-121">Each measurement is in inches or centimeters, depending on the regional settings in Windows Control Panel.</span></span>

## <a name="remarks"></a><span data-ttu-id="86b07-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="86b07-122">Remarks</span></span>

<span data-ttu-id="86b07-123">Pour configurer une application de sorte qu'elle utilise des fenêtres superposées au lieu des documents à onglets, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="86b07-123">To set up an application to use overlapping windows instead of tabbed documents, use the following procedure:</span></span>

1.  <span data-ttu-id="86b07-124">Cliquez sur **options**</span><span class="sxs-lookup"><span data-stu-id="86b07-124">Click **Options**</span></span>

2.  <span data-ttu-id="86b07-125">Cliquez sur **base de données active**.</span><span class="sxs-lookup"><span data-stu-id="86b07-125">Click **Current Database**.</span></span>

3.  <span data-ttu-id="86b07-126">Dans la section **Options de l'application**, sous **Options de la fenêtre Document**, cliquez sur **Fenêtres superposées**.</span><span class="sxs-lookup"><span data-stu-id="86b07-126">In the **Application Options** section, under **Document Window Options**, click **Overlapping Windows**.</span></span>

4.  <span data-ttu-id="86b07-127">Cliquez sur **OK**, puis fermez et rouvrez la base de données.</span><span class="sxs-lookup"><span data-stu-id="86b07-127">Click **OK**, and then close and reopen the database.</span></span>

<span data-ttu-id="86b07-128">Cette action équivaut à cliquer sur **déplacer** ou sur **taille** dans le menu **contrôle** de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="86b07-128">This action is similar to clicking **Move** or **Size** on the window's **Control** menu.</span></span> <span data-ttu-id="86b07-129">Les commandes de menu permettent de déplacer ou de redimensionner la fenêtre à l'aide des touches fléchées du clavier.</span><span class="sxs-lookup"><span data-stu-id="86b07-129">With the menu commands, you use the keyboard's arrow keys to move or resize the window.</span></span> <span data-ttu-id="86b07-130">À l'aide de l'action **déplaceretdimensionnerfenêtre** , vous entrez directement les mesures de position et de taille.</span><span class="sxs-lookup"><span data-stu-id="86b07-130">With the **MoveAndSizeWindow** action, you enter the position and size measurements directly.</span></span> <span data-ttu-id="86b07-131">Vous pouvez également utiliser la souris pour déplacer et dimensionner des fenêtres.</span><span class="sxs-lookup"><span data-stu-id="86b07-131">You can also use the mouse to move and size windows.</span></span>

<span data-ttu-id="86b07-132">Vous pouvez utiliser cette action dans n'importe quelle fenêtre, quel que soit l'affichage.</span><span class="sxs-lookup"><span data-stu-id="86b07-132">You can use this action on any window, in any view.</span></span>

> [!TIP]
> - <span data-ttu-id="86b07-133">Pour déplacer une fenêtre sans la redimensionner, entrez des valeurs pour les arguments **droite** et **bas** , mais laissez les arguments **largeur** et **hauteur** vides.</span><span class="sxs-lookup"><span data-stu-id="86b07-133">To move a window without resizing it, enter values for the **Right** and **Down** arguments but leave the **Width** and **Height** arguments blank.</span></span>
> - <span data-ttu-id="86b07-134">Pour redimensionner une fenêtre sans la déplacer, entrez des valeurs pour les arguments **largeur** et **hauteur** , mais laissez les arguments **droite** et **bas** vides.</span><span class="sxs-lookup"><span data-stu-id="86b07-134">To resize a window without moving it, enter values for the **Width** and **Height** arguments but leave the **Right** and **Down** arguments blank.</span></span>

<span data-ttu-id="86b07-135">Pour exécuter l'action **déplaceretdimensionnerfenêtre** dans un module Visual Basic pour applications (VBA), utilisez la méthode **MoveSize** de l'objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="86b07-135">To run the **MoveAndSizeWindow** action in a Visual Basic for Applications (VBA) module, use the **MoveSize** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="86b07-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="86b07-136">Example</span></span>

<span data-ttu-id="86b07-137">**Synchroniser des formulaires à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="86b07-137">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="86b07-p104">La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="86b07-p104">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86b07-142">Condition</span><span class="sxs-lookup"><span data-stu-id="86b07-142">Condition</span></span></p></th>
<th><p><span data-ttu-id="86b07-143">Action</span><span class="sxs-lookup"><span data-stu-id="86b07-143">Action</span></span></p></th>
<th><p><span data-ttu-id="86b07-144">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="86b07-144">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="86b07-145">Commentaire</span><span class="sxs-lookup"><span data-stu-id="86b07-145">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="86b07-146"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-146"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-147"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-147"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-148">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="86b07-148">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b07-149">IsNull ([ID fournisseur])</span><span class="sxs-lookup"><span data-stu-id="86b07-149">IsNull([Supplier ID])</span></span></p></td>
<td><p><span data-ttu-id="86b07-150"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-150"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-151"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="86b07-151"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="86b07-152"><strong>Bip</strong>: <strong>YesType</strong>: <strong>aucuntitre</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="86b07-152"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="86b07-153">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="86b07-153">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="86b07-154"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-154"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-155"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="86b07-155"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="86b07-156">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="86b07-156">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86b07-157">...</span><span class="sxs-lookup"><span data-stu-id="86b07-157"></span></span></p></td>
<td><p><span data-ttu-id="86b07-158"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-158"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="86b07-159">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="86b07-159">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="86b07-160"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-160"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-161"><strong>Nom du formulaire</strong>: liste des produits <strong>affichage</strong>: <strong>nom donnéesnom du filtre</strong>: <strong>condition WHERE</strong>: [Réf fournisseur] = [Forms]! [Fournisseurs]! Fournisseur <strong>Mode données</strong>: <strong>mode lecture seulemode fenêtre</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-161"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [Supplier ID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-162">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="86b07-162">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="86b07-163"><strong>Déplaceretdimensionnerfenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="86b07-163"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="86b07-164"><strong>droite</strong>: 0,7799&quot; <strong>bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="86b07-164"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="86b07-165">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="86b07-165">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

