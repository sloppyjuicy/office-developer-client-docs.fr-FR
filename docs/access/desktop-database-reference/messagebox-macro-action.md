---
title: Action de Macro contrôle zonemessage.
TOCTitle: MessageBox Macro Action
ms:assetid: 326a0e68-38fb-4f81-b319-5a70caa5aec4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192304(v=office.15)
ms:contentKeyID: 48544077
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6654d2994b472ff2d495b60fffd5fcdbd6e58089
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885233"
---
# <a name="messagebox-macro-action"></a><span data-ttu-id="a0c89-102">Action de Macro contrôle zonemessage.</span><span class="sxs-lookup"><span data-stu-id="a0c89-102">MessageBox Macro Action</span></span>


<span data-ttu-id="a0c89-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0c89-103">**Applies to**: Access 2013, Office 2013</span></span>




<span data-ttu-id="a0c89-104">Vous pouvez utiliser l’action de **contrôle zonemessage** pour afficher une boîte de message contenant un avertissement ou un message d’information.</span><span class="sxs-lookup"><span data-stu-id="a0c89-104">You can use the **MessageBox** action to display a message box containing a warning or an informational message.</span></span> <span data-ttu-id="a0c89-105">Par exemple, vous pouvez utiliser l’action de **contrôle zonemessage** avec des macros de validation.</span><span class="sxs-lookup"><span data-stu-id="a0c89-105">For example, you can use the **MessageBox** action with validation macros.</span></span> <span data-ttu-id="a0c89-106">Lorsqu’un contrôle ou un enregistrement échoue une condition de validation de la macro, une boîte de message peut afficher un message d’erreur et fournissent des instructions sur le type de données qui doivent être saisies.</span><span class="sxs-lookup"><span data-stu-id="a0c89-106">When a control or record fails a validation condition in the macro, a message box can display an error message and provide instructions about the kind of data that should be entered.</span></span>

## <a name="setting"></a><span data-ttu-id="a0c89-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0c89-107">Setting</span></span>

<span data-ttu-id="a0c89-108">L’action de **contrôle zonemessage** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="a0c89-108">The **MessageBox** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0c89-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="a0c89-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="a0c89-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0c89-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-111"><strong>Message</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-111"><strong>Message</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-112">Le texte dans la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-112">The text in the message box.</span></span> <span data-ttu-id="a0c89-113">Entrez le texte du message dans la boîte de <strong>Message</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro.</span><span class="sxs-lookup"><span data-stu-id="a0c89-113">Enter the message text in the <strong>Message</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="a0c89-114">Vous pouvez taper jusqu'à 255 caractères ou entrer une expression (précédée d’un signe égal).</span><span class="sxs-lookup"><span data-stu-id="a0c89-114">You can type up to 255 characters or enter an expression (preceded by an equal sign).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-115"><strong>Beep</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-115"><strong>Beep</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-116">Spécifie si le haut-parleur de votre ordinateur émet un signal sonore lorsque le message s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a0c89-116">Specifies whether your computer's speaker sounds a beep tone when the message displays.</span></span> <span data-ttu-id="a0c89-117">Cliquez sur <strong>Oui</strong> (pour émettre un bip sonore) ou <strong>non</strong> (ne pas émettre le signal sonore).</span><span class="sxs-lookup"><span data-stu-id="a0c89-117">Click <strong>Yes</strong> (sound the beep tone) or <strong>No</strong> (don't sound the beep tone).</span></span> <span data-ttu-id="a0c89-118">La valeur par défaut est <strong>Oui</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0c89-118">The default is <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-119"><strong>Type</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-119"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-120">Le type de boîte de message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-120">The type of message box.</span></span> <span data-ttu-id="a0c89-121">Chaque type a une autre icône.</span><span class="sxs-lookup"><span data-stu-id="a0c89-121">Each type has a different icon.</span></span> <span data-ttu-id="a0c89-122">Cliquez sur <strong>Aucun</strong>, <strong>critique</strong>, <strong>Avertissement ?</strong>, <strong>Avertissement !</strong>, ou les <strong>informations</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0c89-122">Click <strong>None</strong>, <strong>Critical</strong>, <strong>Warning?</strong>, <strong>Warning!</strong>, or <strong>Information</strong>.</span></span> <span data-ttu-id="a0c89-123">La valeur par défaut est <strong>None</strong>.</span><span class="sxs-lookup"><span data-stu-id="a0c89-123">The default is <strong>None</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-124"><strong>Titre</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-124"><strong>Title</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-125">Le texte affiché dans la barre de titre de boîte de message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-125">The text displayed in the message box title bar.</span></span> <span data-ttu-id="a0c89-126">Par exemple, vous pouvez avoir l’affichage de barre de titre &quot;Validation du code client&quot;.</span><span class="sxs-lookup"><span data-stu-id="a0c89-126">For example, you can have the title bar display &quot;Customer ID Validation&quot;.</span></span> <span data-ttu-id="a0c89-127">Si vous laissez cet argument vide, &quot;Microsoft Access&quot; s’affiche.</span><span class="sxs-lookup"><span data-stu-id="a0c89-127">If you leave this argument blank, &quot;Microsoft Access&quot; is displayed.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a0c89-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0c89-128">Remarks</span></span>

<span data-ttu-id="a0c89-129">Vous pouvez utiliser l’action de **contrôle zonemessage** pour créer un message d’erreur formaté semblable aux messages d’erreur intégrés affichés par Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a0c89-129">You can use the **MessageBox** action to create a formatted error message similar to built-in error messages displayed by Microsoft Access.</span></span> <span data-ttu-id="a0c89-130">L’action de **contrôle zonemessage** vous permet de fournir un message en trois sections pour l’argument Message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-130">The **MessageBox** action permits you to supply a message in three sections for the Message argument.</span></span> <span data-ttu-id="a0c89-131">Séparez les sections avec le « @ » caractères.</span><span class="sxs-lookup"><span data-stu-id="a0c89-131">You separate the sections with the "@" character.</span></span>

<span data-ttu-id="a0c89-132">L’exemple suivant affiche un message mis en forme avec un message en plusieurs parties.</span><span class="sxs-lookup"><span data-stu-id="a0c89-132">The following example displays a formatted message box with a sectioned message.</span></span> <span data-ttu-id="a0c89-133">La première section de texte dans le message s’affiche sous forme de titre en gras.</span><span class="sxs-lookup"><span data-stu-id="a0c89-133">The first section of text in the message is displayed as a bold heading.</span></span> <span data-ttu-id="a0c89-134">La deuxième section s’affiche sous forme de texte brut sous cet en-tête.</span><span class="sxs-lookup"><span data-stu-id="a0c89-134">The second section is displayed as plain text beneath that heading.</span></span> <span data-ttu-id="a0c89-135">La troisième section s’affiche en texte simple sous la seconde section, avec une ligne vide entre eux.</span><span class="sxs-lookup"><span data-stu-id="a0c89-135">The third section is displayed as plain text beneath the second section, with a blank line between them.</span></span>

<span data-ttu-id="a0c89-136">Tapez la chaîne suivante dans l’argument **Message** :</span><span class="sxs-lookup"><span data-stu-id="a0c89-136">Type the following string in the **Message** argument:</span></span>

<span data-ttu-id="a0c89-137">**Mauvais bouton\!@This bouton ne work.@Try une autre.**</span><span class="sxs-lookup"><span data-stu-id="a0c89-137">**Wrong button\!@This button doesn't work.@Try another.**</span></span>

<span data-ttu-id="a0c89-138">Vous ne pouvez pas exécuter l’action de **contrôle zonemessage** dans un module Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="a0c89-138">You can't run the **MessageBox** action in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="a0c89-139">Utilisez la fonction **MsgBox** .</span><span class="sxs-lookup"><span data-stu-id="a0c89-139">Use the **MsgBox** function instead.</span></span>

## <a name="examples"></a><span data-ttu-id="a0c89-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="a0c89-140">Examples</span></span>

<span data-ttu-id="a0c89-141">**Synchroniser des formulaires à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="a0c89-141">**Synchronize forms by using a macro**</span></span>

<span data-ttu-id="a0c89-p109">La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a0c89-p109">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0c89-146">Condition</span><span class="sxs-lookup"><span data-stu-id="a0c89-146">Condition</span></span></p></th>
<th><p><span data-ttu-id="a0c89-147">Action</span><span class="sxs-lookup"><span data-stu-id="a0c89-147">Action</span></span></p></th>
<th><p><span data-ttu-id="a0c89-148">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0c89-148">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a0c89-149">Commentaire</span><span class="sxs-lookup"><span data-stu-id="a0c89-149">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-150"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-150"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-151"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-151"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-152">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="a0c89-152">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-153">IsNull([N° fournisseur])</span><span class="sxs-lookup"><span data-stu-id="a0c89-153">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="a0c89-154"><strong>ZoneMessage</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-154"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-155"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="a0c89-155"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="a0c89-156"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="a0c89-156"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="a0c89-157">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-157">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-158">...</span><span class="sxs-lookup"><span data-stu-id="a0c89-158"></span></span></p></td>
<td><p><span data-ttu-id="a0c89-159"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-159"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-160"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="a0c89-160"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="a0c89-161">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="a0c89-161">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-162">...</span><span class="sxs-lookup"><span data-stu-id="a0c89-162"></span></span></p></td>
<td><p><span data-ttu-id="a0c89-163"><strong>ArrêtMacro</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-164">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="a0c89-164">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-165"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-165"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-166"><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [n° fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-166"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-167">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="a0c89-167">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-168"><strong>DéplacerEtDimensionnerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-168"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-169"><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="a0c89-169"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="a0c89-170">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a0c89-170">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0c89-171">**Valider des données à l’aide d’une macro**</span><span class="sxs-lookup"><span data-stu-id="a0c89-171">**Validate data by using a macro**</span></span>

<span data-ttu-id="a0c89-172">La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a0c89-172">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="a0c89-173">Elle illustre l'utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**.</span><span class="sxs-lookup"><span data-stu-id="a0c89-173">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="a0c89-174">Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a0c89-174">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="a0c89-175">Si le code postal n’est pas dans le format approprié pour le pays/région, la macro affiche une boîte de message et annule l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a0c89-175">If the postal code isn't in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="a0c89-176">Elle vous renvoie ensuite au contrôle de code postal, où vous pouvez corriger l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a0c89-176">It then returns you to the PostalCode control, where you can correct the error.</span></span> <span data-ttu-id="a0c89-177">Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="a0c89-177">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0c89-178">Condition</span><span class="sxs-lookup"><span data-stu-id="a0c89-178">Condition</span></span></p></th>
<th><p><span data-ttu-id="a0c89-179">Action</span><span class="sxs-lookup"><span data-stu-id="a0c89-179">Action</span></span></p></th>
<th><p><span data-ttu-id="a0c89-180">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="a0c89-180">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="a0c89-181">Commentaire</span><span class="sxs-lookup"><span data-stu-id="a0c89-181">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-182">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="a0c89-182">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="a0c89-183"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-183"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-184">Si PaysRégion est <strong>Null</strong>, le code postal ne peut pas être validé.</span><span class="sxs-lookup"><span data-stu-id="a0c89-184">If CountryRegion is <strong>Null</strong>, the postal code can't be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-185">[PaysRégion] Dans (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et Len([PostalCode]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="a0c89-185">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([PostalCode]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="a0c89-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-187"><strong>Message</strong>: le code postal doit contenir 5 caractères.</span><span class="sxs-lookup"><span data-stu-id="a0c89-187"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="a0c89-188"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="a0c89-188"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="a0c89-189">Si le code postal ne contient pas 5 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-189">If the postal code isn't 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-190">...</span><span class="sxs-lookup"><span data-stu-id="a0c89-190"></span></span></p></td>
<td><p><span data-ttu-id="a0c89-191"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-191"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-192">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="a0c89-192">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-193"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-193"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-194"><strong>Nom du contrôle</strong>: CodePostal</span><span class="sxs-lookup"><span data-stu-id="a0c89-194"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-195">[PaysRégion] Dans (&quot;Australie&quot;,&quot;Singapour&quot;) et Len([PostalCode]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="a0c89-195">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([PostalCode]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="a0c89-196"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-196"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-197"><strong>Message</strong>: le code postal doit contenir 4 caractères.</span><span class="sxs-lookup"><span data-stu-id="a0c89-197"><strong>Message</strong>: The postal code must be 4 characters.</span></span> <span data-ttu-id="a0c89-198"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="a0c89-198"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="a0c89-199">Si le code postal ne contient pas 4 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="a0c89-199">If the postal code isn't 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-200">...</span><span class="sxs-lookup"><span data-stu-id="a0c89-200"></span></span></p></td>
<td><p><span data-ttu-id="a0c89-201"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-201"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-202">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="a0c89-202">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-203"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-203"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-204"><strong>Nom du contrôle</strong>: CodePostal</span><span class="sxs-lookup"><span data-stu-id="a0c89-204"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0c89-205">([PaysRégion] = &quot;Canada&quot;) Et ([code postal] pas comme&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="a0c89-205">([CountryRegion] = &quot;Canada&quot;) And ([PostalCode] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="a0c89-206"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-206"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="a0c89-207"><strong>Message</strong>: le code postal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a0c89-207"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="a0c89-208">Exemple de code canadien : H1J 1C3 <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="a0c89-208">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="a0c89-p115">Si le code postal n’est pas correct pour le Canada, affiche un message. (Exemple de code postal canadien : H1J 1C3.)</span><span class="sxs-lookup"><span data-stu-id="a0c89-p115">If the postal code isn't correct for Canada, display a message. (Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0c89-211">...</span><span class="sxs-lookup"><span data-stu-id="a0c89-211"></span></span></p></td>
<td><p><span data-ttu-id="a0c89-212"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="a0c89-212"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="a0c89-213">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="a0c89-213">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

