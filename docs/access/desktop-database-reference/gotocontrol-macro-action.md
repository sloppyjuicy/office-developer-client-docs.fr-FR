---
title: GoToControl, action de macro
TOCTitle: GoToControl macro action
ms:assetid: caff76dc-7ca8-4f87-8144-89445ed4600d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834370(v=office.15)
ms:contentKeyID: 48547705
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c056f2b0922402ea7cde7cf767969b73f912f572
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292166"
---
# <a name="gotocontrol-macro-action"></a><span data-ttu-id="1ac54-102">GoToControl, action de macro</span><span class="sxs-lookup"><span data-stu-id="1ac54-102">GoToControl macro action</span></span>

<span data-ttu-id="1ac54-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ac54-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ac54-104">Vous pouvez utiliser l'action **AtteindreContrôle** pour déplacer le focus sur le champ ou le contrôle spécifié dans l'enregistrement actif du formulaire ouvert, de la feuille de donnée de formulaire, de la feuille de donnée de table ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="1ac54-104">You can use the **GoToControl** action to move the focus to the specified field or control in the current record of the open form, form datasheet, table datasheet, or query datasheet.</span></span> <span data-ttu-id="1ac54-105">Vous pouvez utiliser cette action lorsque vous souhaitez mettre le focus sur un champ ou un contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="1ac54-105">You can use this action when you want a particular field or control to have the focus.</span></span> <span data-ttu-id="1ac54-106">Ce champ ou le contrôle puis utilisable pour des comparaisons ou des actions **TrouverEnregistrement**.</span><span class="sxs-lookup"><span data-stu-id="1ac54-106">This field or control can then be used for comparisons or **FindRecord** actions.</span></span> <span data-ttu-id="1ac54-107">Vous pouvez également utiliser cette action pour naviguer dans un formulaire sous certaines conditions.</span><span class="sxs-lookup"><span data-stu-id="1ac54-107">You can also use this action to navigate in a form according to certain conditions.</span></span> <span data-ttu-id="1ac54-108">Par exemple, si l'utilisateur saisit non dans un contrôle conjoint sur un formulaire d'assurance maladie, le focus peut automatiquement passer le contrôle nom du conjoint/partenaire et déplacer vers le contrôle suivant.</span><span class="sxs-lookup"><span data-stu-id="1ac54-108">For example, if the user enters No in a Married control on a health insurance form, the focus can automatically skip the Spouse/partner Name control and move to the next control.</span></span>

## <a name="setting"></a><span data-ttu-id="1ac54-109">Setting</span><span class="sxs-lookup"><span data-stu-id="1ac54-109">Setting</span></span>

> [!NOTE]
> <span data-ttu-id="1ac54-110">Cette action ne peut pas être utilisée avec des pages d'accès aux données.</span><span class="sxs-lookup"><span data-stu-id="1ac54-110">This action is not available for use with data access pages.</span></span>

<span data-ttu-id="1ac54-111">L’action **AtteindreContrôle** possède l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="1ac54-111">The **GoToControl** action has the following argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ac54-112">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="1ac54-112">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1ac54-113">Description</span><span class="sxs-lookup"><span data-stu-id="1ac54-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-114"><strong>Nom du contrôle</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-114"><strong>Control Name</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-115">Nom du champ ou du contrôle dans lequel vous souhaitez déplacer le focus.</span><span class="sxs-lookup"><span data-stu-id="1ac54-115">The name of the field or control where you want the focus.</span></span> <span data-ttu-id="1ac54-116">Entrez le nom du champ ou du contrôle dans la zone <strong>nom du contrôle</strong> de la section arguments de l' <strong>action</strong> du volet générateur de macro.</span><span class="sxs-lookup"><span data-stu-id="1ac54-116">Enter the field or control name in the <strong>Control Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane.</span></span> <span data-ttu-id="1ac54-117">Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1ac54-117">This is a required argument.</span></span></p>
<p><span data-ttu-id="1ac54-118"><strong>Remarque</strong>: entrez uniquement le nom du champ ou du contrôle dans l'argument <strong>nom du contrôle</strong> , et non pas l'identificateur complet, comme Forms! Articles! [Product ID].</span><span class="sxs-lookup"><span data-stu-id="1ac54-118"><strong>NOTE</strong>: Enter only the name of the field or control in the <strong>Control Name</strong> argument, not the fully qualified identifier, such as Forms!Products![Product ID].</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1ac54-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ac54-119">Remarks</span></span>

<span data-ttu-id="1ac54-120">Vous ne pouvez pas utiliser l'action **AtteindreContrôle** pour déplacer le focus sur un contrôle dans un formulaire masqué.</span><span class="sxs-lookup"><span data-stu-id="1ac54-120">You cannot use the **GoToControl** action to move the focus to a control on a hidden form.</span></span>

> [!TIP]
> <span data-ttu-id="1ac54-121">Vous pouvez utiliser l'action **AtteindreContrôle** pour accéder à un sous-formulaire, qui est un type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="1ac54-121">You can use the **GoToControl** action to move to a subform, which is a type of control.</span></span> <span data-ttu-id="1ac54-122">Vous pouvez ensuite utiliser l'action **AtteindreEnregistrement** pour accéder à un enregistrement particulier dans le sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ac54-122">You can then use the **GoToRecord** action to move to a particular record in the subform.</span></span> <span data-ttu-id="1ac54-123">Vous pouvez également déplacer un contrôle dans un sous-formulaire à l'aide de l'action **AtteindreContrôle** pour passer tout d'abord le sous-formulaire, puis le contrôle du sous-formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ac54-123">You can also move to a control on a subform by using the **GoToControl** action to move first to the subform and then to the control on the subform.</span></span>

<span data-ttu-id="1ac54-124">Pour exécuter l'action **AtteindreContrôle** dans un module Visual Basic pour applications (VBA), utilisez la méthode **GoToControl** de l'objet **DoCmd** .</span><span class="sxs-lookup"><span data-stu-id="1ac54-124">To run the **GoToControl** action in a Visual Basic for Applications (VBA) module, use the **GoToControl** method of the **DoCmd** object.</span></span> <span data-ttu-id="1ac54-125">Vous pouvez également utiliser la méthode **SetFocus** pour placer le focus sur un contrôle dans un formulaire ou un de ses sous-formulaires, ou à un champ dans une table ouverte, une requête ou une feuille de données de formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ac54-125">You can also use the **SetFocus** method to move the focus to a control on a form or any of its subforms, or to a field in an open table, query, or form datasheet.</span></span>

## <a name="examples"></a><span data-ttu-id="1ac54-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="1ac54-126">Examples</span></span>

<span data-ttu-id="1ac54-127">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="1ac54-127">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="1ac54-p105">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ac54-p105">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ac54-133">Action</span><span class="sxs-lookup"><span data-stu-id="1ac54-133">Action</span></span></p></th>
<th><p><span data-ttu-id="1ac54-134">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="1ac54-134">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1ac54-135">Commentaire</span><span class="sxs-lookup"><span data-stu-id="1ac54-135">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-136"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-136"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-137"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-137"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-138">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="1ac54-138">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac54-139"><strong>Fermerfenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-139"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-140"><strong>Type d'objet</strong>: <strong>Formulairenom nom</strong>: liste des produits <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-140"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-141">Fermez le formulaire liste des produits.</span><span class="sxs-lookup"><span data-stu-id="1ac54-141">Close Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-142"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-142"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-143"><strong>Nom du formulaire</strong>: <strong>produits affichage</strong>: <strong>formulairemode mode</strong> <strong>ajoutermode fenêtre</strong>: <strong>normal</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-143"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-144">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="1ac54-144">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac54-145"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-145"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-146"><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</span><span class="sxs-lookup"><span data-stu-id="1ac54-146"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="1ac54-147">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ac54-147">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-148"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-148"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-149"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="1ac54-149"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="1ac54-150">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="1ac54-150">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ac54-151">**Valider des données à l’aide d’une macro**</span><span class="sxs-lookup"><span data-stu-id="1ac54-151">**Validate data by using a macro**</span></span>

<span data-ttu-id="1ac54-152">La macro de validation suivante vérifie les codes postaux entrés dans un formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ac54-152">The following validation macro checks the postal codes entered in a Suppliers form.</span></span> <span data-ttu-id="1ac54-153">Elle illustre l’utilisation des actions **ArrêtMacro**, **ZoneMessage**, **AnnulerEvénement** et **AtteindreContrôle**.</span><span class="sxs-lookup"><span data-stu-id="1ac54-153">It shows the use of the **StopMacro**, **MessageBox**, **CancelEvent**, and **GoToControl** actions.</span></span> <span data-ttu-id="1ac54-154">Une expression conditionnelle vérifie le pays/la région et le code postal entrés dans un enregistrement du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1ac54-154">A conditional expression checks the country/region and postal code entered in a record on the form.</span></span> <span data-ttu-id="1ac54-155">Si le code postal n’est pas dans le format correct pour le pays/la région, la macro affiche une zone de message et annule la sauvegarde de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1ac54-155">If the postal code is not in the right format for the country/region, the macro displays a message box and cancels saving the record.</span></span> <span data-ttu-id="1ac54-156">La macro vous renvoie ensuite au contrôle de code postal, dans lequel vous pouvez corriger l'erreur.</span><span class="sxs-lookup"><span data-stu-id="1ac54-156">The macro then returns you to the Postal Code control, where you can correct the error.</span></span> <span data-ttu-id="1ac54-157">Cette macro doit être attachée à la propriété **AvantMAJ** du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ac54-157">This macro should be attached to the **BeforeUpdate** property of the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ac54-158">Condition</span><span class="sxs-lookup"><span data-stu-id="1ac54-158">Condition</span></span></p></th>
<th><p><span data-ttu-id="1ac54-159">Action</span><span class="sxs-lookup"><span data-stu-id="1ac54-159">Action</span></span></p></th>
<th><p><span data-ttu-id="1ac54-160">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="1ac54-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1ac54-161">Commentaire</span><span class="sxs-lookup"><span data-stu-id="1ac54-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-162">IsNull ([PaysRégion])</span><span class="sxs-lookup"><span data-stu-id="1ac54-162">IsNull([CountryRegion])</span></span></p></td>
<td><p><span data-ttu-id="1ac54-163"><strong>StopMacro</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-163"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-164">Si PaysRégion a la <strong>valeur null</strong>, le code postal ne peut pas être validé.</span><span class="sxs-lookup"><span data-stu-id="1ac54-164">If CountryRegion is <strong>Null</strong>, postal code cannot be validated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac54-165">Région Dans (&quot;France&quot;,&quot;Italie&quot;,&quot;Espagne&quot;) et NBCAR ([code postal]) &lt; &gt; 5</span><span class="sxs-lookup"><span data-stu-id="1ac54-165">[CountryRegion] In (&quot;France&quot;,&quot;Italy&quot;,&quot;Spain&quot;) And Len([Postal Code]) &lt;&gt; 5</span></span></p></td>
<td><p><span data-ttu-id="1ac54-166"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-166"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-167"><strong>Message</strong>: le code postal doit comporter 5 caractères.</span><span class="sxs-lookup"><span data-stu-id="1ac54-167"><strong>Message</strong>: The postal code must be 5 characters.</span></span> <span data-ttu-id="1ac54-168"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</span><span class="sxs-lookup"><span data-stu-id="1ac54-168"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="1ac54-169">Si le code postal n'est pas de 5 caractères, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="1ac54-169">If the postal code is not 5 characters, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-170">...</span><span class="sxs-lookup"><span data-stu-id="1ac54-170"></span></span></p></td>
<td><p><span data-ttu-id="1ac54-171"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-171"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-172">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="1ac54-172">Cancel the event.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-173"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-173"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-174"><strong>Nom du contrôle</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="1ac54-174"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-175">Région En (&quot;Australie&quot;,&quot;Singapour&quot;) et NBCAR ([code postal]) &lt; &gt; 4</span><span class="sxs-lookup"><span data-stu-id="1ac54-175">[CountryRegion] In (&quot;Australia&quot;,&quot;Singapore&quot;) And Len([Postal Code]) &lt;&gt; 4</span></span></p></td>
<td><p><span data-ttu-id="1ac54-176"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-176"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-177">Message : Le code postal doit contenir 4 caractères.</span><span class="sxs-lookup"><span data-stu-id="1ac54-177">Message: The postal code must be 4 characters.</span></span> <span data-ttu-id="1ac54-178"><strong>Bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</span><span class="sxs-lookup"><span data-stu-id="1ac54-178"><strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="1ac54-179">Si le code postal n'est pas 4 caractères, affichez un message.</span><span class="sxs-lookup"><span data-stu-id="1ac54-179">If the postal code is not 4 characters, display a message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac54-180">...</span><span class="sxs-lookup"><span data-stu-id="1ac54-180"></span></span></p></td>
<td><p><span data-ttu-id="1ac54-181"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-181"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-182">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="1ac54-182">Cancel the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-183"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-183"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-184"><strong>Nom du contrôle</strong>: PostalCode</span><span class="sxs-lookup"><span data-stu-id="1ac54-184"><strong>Control Name</strong>: PostalCode</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac54-185">([PaysRégion] = &quot;Canada&quot;) Et ([code postal] non comme&quot;[A-z] [0-9] [A-z] [0-9] [A-z] [0-9]&quot;</span><span class="sxs-lookup"><span data-stu-id="1ac54-185">([CountryRegion] = &quot;Canada&quot;) And ([Postal Code] Not Like&quot;[A-Z][0-9][A-Z] [0-9][A-Z][0-9]&quot;)</span></span></p></td>
<td><p><span data-ttu-id="1ac54-186"><strong>MessageBox</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-186"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="1ac54-187"><strong>Message</strong>: le code postal n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1ac54-187"><strong>Message</strong>: The postal code is not valid.</span></span> <span data-ttu-id="1ac54-188">Exemple de code canadien: H1J 1C3 <strong>bip</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: erreur de code postal</span><span class="sxs-lookup"><span data-stu-id="1ac54-188">Example of Canadian code: H1J 1C3 <strong>Beep</strong>: <strong>YesType</strong>: <strong>InformationTitle</strong>: Postal Code Error</span></span></p></td>
<td><p><span data-ttu-id="1ac54-189">Si le code postal n'est pas correct pour le Canada, affiche un message.</span><span class="sxs-lookup"><span data-stu-id="1ac54-189">If the postal code is not correct for Canada, display a message.</span></span> <span data-ttu-id="1ac54-190">(Exemple de code postal canadien : H1J 1C3.)</span><span class="sxs-lookup"><span data-stu-id="1ac54-190">(Example of Canadian code: H1J 1C3)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac54-191">...</span><span class="sxs-lookup"><span data-stu-id="1ac54-191"></span></span></p></td>
<td><p><span data-ttu-id="1ac54-192"><strong>CancelEvent</strong></span><span class="sxs-lookup"><span data-stu-id="1ac54-192"><strong>CancelEvent</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="1ac54-193">Annule l’événement.</span><span class="sxs-lookup"><span data-stu-id="1ac54-193">Cancel the event.</span></span></p></td>
</tr>
</tbody>
</table>

