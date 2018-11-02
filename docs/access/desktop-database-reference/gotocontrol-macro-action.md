---
title: GoToControl, action de macro
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9fafa3ea40b492baf8b49dd240c6f7767ffad655
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926653"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="897c5-102">GoToControl, action de macro</span><span class="sxs-lookup"><span data-stu-id="897c5-102">GoToControl macro action</span></span>


<span data-ttu-id="897c5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="897c5-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="897c5-104">Vous pouvez utiliser l’action **GoToControl** pour placer le focus sur le champ spécifié ou le contrôle de l’enregistrement actif du formulaire ouvert, formulaire, feuille de données de table ou feuille de données de requête.</span><span class="sxs-lookup"><span data-stu-id="897c5-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="897c5-105">Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="897c5-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="897c5-106">Ce champ ou le contrôle puis utilisable pour des comparaisons ou des actions **TrouverEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="897c5-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="897c5-107">Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="897c5-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="897c5-108">Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="897c5-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="897c5-109">Paramètre</span><span class="sxs-lookup"><span data-stu-id="897c5-109">Setting</span></span>


> [!NOTE]
> <P><span data-ttu-id="897c5-110">Cette action n’est pas disponible pour une utilisation avec des pages d’accès aux données.</span><span class="sxs-lookup"><span data-stu-id="897c5-110">This action is not available for use with data access pages.</span></span></P>



<span data-ttu-id="897c5-111">L’action **AtteindreContrôle** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="897c5-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="897c5-112">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="897c5-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="897c5-113">Description</span><span class="sxs-lookup"><span data-stu-id="897c5-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="897c5-114"><strong>Nom du contrôle</strong> :</span><span class="sxs-lookup"><span data-stu-id="897c5-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-115">Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus.</span><span class="sxs-lookup"><span data-stu-id="897c5-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="897c5-116">Entrez le nom de champ ou un contrôle dans la zone <strong>Nom du contrôle</strong> dans la section <strong>Arguments de l’Action</strong> du volet Générateur de Macro.</span><span class="sxs-lookup"><span data-stu-id="897c5-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="897c5-117">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="897c5-117">This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="897c5-118">Entrez uniquement le nom du champ ou du contrôle dans l’argument <STRONG>Nom du contrôle</STRONG> , pas l’identificateur complet, tels que des formulaires ! Produits ! [ID produit].</span><span class="sxs-lookup"><span data-stu-id="897c5-118">Enter only the name of the field or control in the <STRONG>Control Name</STRONG> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></P>


<p></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="897c5-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="897c5-119">Remarks</span></span>

<span data-ttu-id="897c5-120">Vous ne pouvez pas utiliser l’action **AtteindreContrôle** pour déplacer le focus vers un contrôle sur un formulaire masqué.</span><span class="sxs-lookup"><span data-stu-id="897c5-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>


> [!TIP]
> <P><span data-ttu-id="897c5-121">Vous pouvez utiliser l’action <STRONG>AtteindreContrôle</STRONG> pour déplacer un sous-formulaire, qui est un type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="897c5-121">You can use the <STRONG>GoToControl</STRONG> action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="897c5-122">Vous pouvez ensuite utiliser l’action <STRONG>AtteindreEnregistrement</STRONG> pour déplacer vers un enregistrement particulier du sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="897c5-122">You can then use the <STRONG>GoToRecord</STRONG> action to move to a particular record in the subform.</span></span> <span data-ttu-id="897c5-123">Vous pouvez également déplacer un contrôle dans un sous-formulaire à l’aide de l’action <STRONG>AtteindreContrôle</STRONG> pour accéder d’abord le sous-formulaire, puis le contrôle de sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="897c5-123">You can also move to a control on a subform by using the <STRONG>GoToControl</STRONG> action to move first to the subform and then to the control on the subform.</span></span></P>



<span data-ttu-id="897c5-124">Pour exécuter l’action **AtteindreContrôle** dans un module Visual Basic pour Applications (VBA), utilisez la méthode **GoToControl** de l’objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="897c5-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="897c5-125">Vous pouvez également utiliser la méthode **SetFocus** pour placer le focus sur un contrôle dans un formulaire ou un de ses sous-formulaires, ou à un champ dans une table ouverte, une requête ou une feuille de données de formulaire.</span><span class="sxs-lookup"><span data-stu-id="897c5-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="897c5-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="897c5-126">Examples</span></span>

<span data-ttu-id="897c5-127">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="897c5-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="897c5-p105">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="897c5-p105">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="897c5-133">Action</span><span class="sxs-lookup"><span data-stu-id="897c5-133">Action</span></span></p></th>
<th><p><span data-ttu-id="897c5-134">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="897c5-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="897c5-135">Commentaire</span><span class="sxs-lookup"><span data-stu-id="897c5-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="897c5-136"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-137"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-138">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="897c5-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="897c5-139"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-140"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-141">Fermer le formulaire liste des produits.</span><span class="sxs-lookup"><span data-stu-id="897c5-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="897c5-142"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-143"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-144">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="897c5-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="897c5-145"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-146"><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</span><span class="sxs-lookup"><span data-stu-id="897c5-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="897c5-147">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="897c5-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="897c5-148"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-149"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="897c5-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="897c5-150">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="897c5-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="897c5-151">**Valider des données à l’aide d’une macro**</span><span class="sxs-lookup"><span data-stu-id="897c5-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="897c5-152">La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="897c5-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="897c5-153">Elle illustre l'utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**.</span><span class="sxs-lookup"><span data-stu-id="897c5-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="897c5-154">Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="897c5-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="897c5-155">Si le code postal n'est pas dans le format correct pour le pays/la région, la macro affiche une zone de message et annule la sauvegarde de l'enregistrement.</span><span class="sxs-lookup"><span data-stu-id="897c5-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="897c5-156">La macro puis revenir au contrôle de Code Postal, où vous pouvez corriger l’erreur.</span><span class="sxs-lookup"><span data-stu-id="897c5-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="897c5-157">Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="897c5-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="897c5-158">Condition</span><span class="sxs-lookup"><span data-stu-id="897c5-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="897c5-159">Action</span><span class="sxs-lookup"><span data-stu-id="897c5-159">Action</span></span></p></th>
<th><p><span data-ttu-id="897c5-160">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="897c5-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="897c5-161">Commentaire</span><span class="sxs-lookup"><span data-stu-id="897c5-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="897c5-162">IsNull([CountryRegion])</span><span class="sxs-lookup"><span data-stu-id="897c5-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="897c5-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="897c5-164">Si PaysRégion est <strong>Null</strong>, le code postal ne peut pas être validé.</span><span class="sxs-lookup"><span data-stu-id="897c5-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="897c5-165">[PaysRégion] Dans (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et NBCAR ([Code Postal]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="897c5-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="897c5-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-167"><strong>Message</strong>: le code postal doit contenir 5 caractères.</span><span class="sxs-lookup"><span data-stu-id="897c5-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="897c5-168"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="897c5-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="897c5-169">Si le code postal n’est pas 5 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="897c5-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="897c5-170">...</span><span class="sxs-lookup"><span data-stu-id="897c5-170"></span></span></p></td>
<td><p><span data-ttu-id="897c5-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="897c5-172">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="897c5-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="897c5-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-174"><strong>Nom du contrôle</strong>: CodePostal</span><span class="sxs-lookup"><span data-stu-id="897c5-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="897c5-175">[PaysRégion] Dans (&quot;Australie&quot;,&quot;Singapour&quot;) et NBCAR ([Code Postal]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="897c5-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="897c5-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-177">Message : Le code postal doit contenir 4 caractères. 

</span><span class="sxs-lookup"><span data-stu-id="897c5-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="897c5-178"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="897c5-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="897c5-179">Si le code postal n’est pas 4 caractères, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="897c5-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="897c5-180">...</span><span class="sxs-lookup"><span data-stu-id="897c5-180"></span></span></p></td>
<td><p><span data-ttu-id="897c5-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="897c5-182">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="897c5-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="897c5-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-184"><strong>Nom du contrôle</strong>: CodePostal</span><span class="sxs-lookup"><span data-stu-id="897c5-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="897c5-185">([PaysRégion] = &quot;Canada&quot;) Et ([Code Postal] pas comme&quot;[A-Z] [0-9] [A-Z] [0-9] [A-Z] [0-9]&quot;)</span><span class="sxs-lookup"><span data-stu-id="897c5-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="897c5-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="897c5-187"><strong>Message</strong>: le code postal n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="897c5-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="897c5-188">Exemple de code canadien : H1J 1C3 <strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de Code Postal</span><span class="sxs-lookup"><span data-stu-id="897c5-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="897c5-189">Si le code postal n’est pas correct pour le Canada, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="897c5-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="897c5-190">(L’exemple de code canadien : H1J 1C3)</span><span class="sxs-lookup"><span data-stu-id="897c5-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="897c5-191">...</span><span class="sxs-lookup"><span data-stu-id="897c5-191"></span></span></p></td>
<td><p><span data-ttu-id="897c5-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="897c5-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="897c5-193">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="897c5-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

