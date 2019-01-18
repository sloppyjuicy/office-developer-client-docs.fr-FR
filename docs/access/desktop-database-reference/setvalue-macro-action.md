---
title: SetValue, action de macro
TOCTitle: SetValue macro action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 6b6f16c22e9265159c73279cfa1b2644adbc0277
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722689"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="60cf5-102">SetValue, action de macro</span><span class="sxs-lookup"><span data-stu-id="60cf5-102">SetValue macro action</span></span>

<span data-ttu-id="60cf5-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="60cf5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="60cf5-104">Vous pouvez utiliser l'action **DéfinirValeur** pour définir la valeur d'un champ, d'un contrôle ou d'une propriété Microsoft Access dans un formulaire, un formulaire feuille de données ou un état.</span><span class="sxs-lookup"><span data-stu-id="60cf5-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>

> [!NOTE]
> - <span data-ttu-id="60cf5-105">[!REMARQUE] Vous ne pouvez pas utiliser l'action **DéfinirValeur** pour définir la valeur d'une propriété Access qui renvoie un objet.</span><span class="sxs-lookup"><span data-stu-id="60cf5-105">You cannot use the **SetValue** action to set the value of an Access property that returns an object.</span></span>
> - <span data-ttu-id="60cf5-106">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée.</span><span class="sxs-lookup"><span data-stu-id="60cf5-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="60cf5-107">Paramètre</span><span class="sxs-lookup"><span data-stu-id="60cf5-107">Setting</span></span>

<span data-ttu-id="60cf5-108">L'action **DéfinirValeur** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="60cf5-108">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60cf5-109">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="60cf5-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="60cf5-110">Description</span><span class="sxs-lookup"><span data-stu-id="60cf5-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60cf5-111"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-111"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-p101">Nom du champ, du contrôle ou de la propriété dont vous souhaitez définir la valeur. Entrez le nom du champ, du contrôle ou de la propriété dans la zone <strong>Élément</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser la syntaxe complète pour faire référence à cet élément, telle que <em>nom_contrôle</em> (pour un contrôle dans le formulaire ou l’état à partir duquel la macro a été appelée) ou <strong>Forms</strong>!<em>nom_formulaire</em>!<em>nom_contrôle</em>. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p101">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60cf5-116"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-116"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-p102">Expression utilisée par Access pour définir la valeur de cet élément. Vous devez toujours utiliser la syntaxe complète pour faire référence à des objets dans l’expression. Par exemple, pour augmenter la valeur d’un contrôle Salaire dans un formulaire Employés de 10 pour cent, utilisez Forms!Employees!Salary\*1.1.. Il s’agit d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p102">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p><p><span data-ttu-id="60cf5-121"><strong>Remarque</strong>: n’utilisez pas un signe égal (=) avant l’expression dans cet argument.</span><span class="sxs-lookup"><span data-stu-id="60cf5-121"><strong>NOTE</strong>: You shouldn't use an equal sign (=) before the expression in this argument.</span></span> <span data-ttu-id="60cf5-122">Si vous le faites, Access évalue l’expression, puis utilise cette valeur comme expression dans cet argument.</span><span class="sxs-lookup"><span data-stu-id="60cf5-122">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="60cf5-123">Cela peut produire des résultats inattendus si l’expression est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="60cf5-123">This can produce unexpected results if the expression is a string.</span></span></p>
<p><span data-ttu-id="60cf5-124">Par exemple, si vous tapez <strong> = &quot;chaîne1&quot; </strong> à cet argument, Access évalue l’expression comme chaîne1 d’abord.</span><span class="sxs-lookup"><span data-stu-id="60cf5-124">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="60cf5-125">Il utilise ensuite Chaîne1 comme expression dans cet argument, s’attendant à trouver un contrôle ou la propriété nommé Chaîne1 dans le formulaire ou l’état qui a appelé la macro.</span><span class="sxs-lookup"><span data-stu-id="60cf5-125">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="60cf5-126">[!REMARQUE] Dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton **Générer** pour utiliser le Générateur d'expression et créer une expression pour l'un de ces arguments.</span><span class="sxs-lookup"><span data-stu-id="60cf5-126">In an Access database (.mdb or .accdb), click the **Build** button to use the Expression Builder to create an expression for either of these arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="60cf5-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="60cf5-127">Remarks</span></span>

<span data-ttu-id="60cf5-p105">Vous pouvez utiliser cette action pour définir une valeur pour un champ ou un contrôle dans un formulaire, un formulaire feuille de données ou un état. Vous pouvez également définir la valeur de presque toutes les propriétés de contrôle, de formulaire et d'état dans n'importe quel affichage. Pour déterminer si une propriété spécifique peut être configurée à l'aide d'une macro et les affichages pouvant être définis, consultez la rubrique d'aide relative à cette propriété dans Visual Basic Editor.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p105">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="60cf5-131">Vous pouvez également définir la valeur d'un champ dans la table sous-jacente d'un formulaire, même si le formulaire ne contient pas de contrôle lié au champ.</span><span class="sxs-lookup"><span data-stu-id="60cf5-131">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="60cf5-132">Utilisez la syntaxe **Forms**\!*formname*\!*fieldname* dans la zone **élément** pour définir la valeur pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="60cf5-132">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="60cf5-133">Vous pouvez également faire référence à un champ de table sous-jacente d’un état à l’aide de la syntaxe de **rapports**\!*reportname*\!*fieldname*, mais il doit exister un contrôle dépendant de ce champ ou le champ doit être référencé en une contrôle calculé dans l’état.</span><span class="sxs-lookup"><span data-stu-id="60cf5-133">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="60cf5-p107">Si vous définissez la valeur d'un contrôle dans un formulaire, l'action **DéfinirValeur** ne déclenche pas les règles de validation au niveau du formulaire du contrôle, mais elle déclenche les règles de validation au niveau de la table du champ sous-jacent si le contrôle est un contrôle lié. L'action **DéfinirValeur** déclenche également le recalcul, mais ce dernier peut ne pas avoir lieu immédiatement. Pour déclencher la mise à jour immédiate et forcer l'exécution du recalcul, utilisez l'action **RedessinerObjet**. La valeur que vous définissez dans un contrôle à l'aide de l'action **DéfinirValeur** est également non affectée par un masque de saisie défini dans la propriété **InputMask** du contrôle ou du champ sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p107">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="60cf5-p108">Pour modifier la valeur d'un contrôle, vous pouvez utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **AfterUpdate** du contrôle. Toutefois, vous ne pouvez pas utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **BeforeUpdate** d'un contrôle pour modifier la valeur du contrôle (bien que vous puissiez utiliser l'action **DéfinirValeur** pour modifier la valeur d'autres contrôles). Vous pouvez également utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété **AvantMAJ** ou **AprèsMAJ** d'un formulaire pour modifier la valeur de tous les contrôles de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p108">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>

> [!NOTE]
> <span data-ttu-id="60cf5-141">Vous ne pouvez pas utiliser l’action **DéfinirValeur** pour définir la valeur des contrôles suivants :</span><span class="sxs-lookup"><span data-stu-id="60cf5-141">You can't use the **SetValue** action to set the value of the following controls:</span></span>
> - <span data-ttu-id="60cf5-142">Les contrôles dépendants et les contrôles calculés dans des états.</span><span class="sxs-lookup"><span data-stu-id="60cf5-142">Bound controls and calculated controls on reports.</span></span>
> - <span data-ttu-id="60cf5-143">Les contrôles calculés dans des formulaires.</span><span class="sxs-lookup"><span data-stu-id="60cf5-143">Calculated controls on forms.</span></span>

> [!TIP]
> <span data-ttu-id="60cf5-144">[!CONSEIL] Vous pouvez utiliser l'action **DéfinirValeur** pour masquer ou afficher un formulaire en mode Formulaire.</span><span class="sxs-lookup"><span data-stu-id="60cf5-144">You can use the **SetValue** action to hide or show a form in Form view.</span></span> <span data-ttu-id="60cf5-145">Entrez **formulaires**! formname \*\*\*\*. Visible\*\* dans la zone de **l’élément** et **non** ou **Oui** dans la zone **Expression** .</span><span class="sxs-lookup"><span data-stu-id="60cf5-145">Enter **Forms**!*formname\*\*\*.Visible*\* in the **Item** box, and **No** or **Yes** in the **Expression** box.</span></span> <span data-ttu-id="60cf5-146">La définition de la propriété **Visible** d'un formulaire modal sur **Non** masque le formulaire et le rend non modal.</span><span class="sxs-lookup"><span data-stu-id="60cf5-146">Setting a modal form's **Visible** property to **No** hides the form and makes it modeless.</span></span> <span data-ttu-id="60cf5-147">La définition de la propriété sur **Oui** affiche le formulaire et le rend à nouveau modal.</span><span class="sxs-lookup"><span data-stu-id="60cf5-147">Setting the property to **Yes** displays the form and makes it modal again.</span></span>

<span data-ttu-id="60cf5-p110">La modification de la valeur ou l'ajout des nouvelles données dans un contrôle à l'aide de l'action **DéfinirValeur** dans une macro ne déclenche pas des événements tels que **AvantMAJ**, **AvantInsertion** ou **Modifier** qui se produisent lorsque vous modifiez ou entrez des données dans ces contrôles dans l'interface utilisateur. Ces événements ne se produisent pas non plus si vous définissez la valeur du contrôle à l'aide d'un module Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="60cf5-p110">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="60cf5-p111">Cette action n'est pas disponible dans un module VBA. Définissez la valeur directement en langage VBA.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p111">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="60cf5-152">Exemple</span><span class="sxs-lookup"><span data-stu-id="60cf5-152">Example</span></span>

<span data-ttu-id="60cf5-153">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="60cf5-153">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="60cf5-p112">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="60cf5-p112">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="60cf5-159">Action</span><span class="sxs-lookup"><span data-stu-id="60cf5-159">Action</span></span></p></th>
<th><p><span data-ttu-id="60cf5-160">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="60cf5-160">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="60cf5-161">Commentaire</span><span class="sxs-lookup"><span data-stu-id="60cf5-161">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="60cf5-162"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-162"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-163"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-163"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-164">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="60cf5-164">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60cf5-165"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-165"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-166"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-166"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-167">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="60cf5-167">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60cf5-168"><strong>OpenForm</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-168"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-169"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-169"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-170">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="60cf5-170">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="60cf5-171"><strong>SetValue</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-171"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-172"><strong>Élément</strong>: [Forms]![Produits]! [N° fournisseur] <strong>Expression</strong>: N° fournisseur  </span><span class="sxs-lookup"><span data-stu-id="60cf5-172"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="60cf5-173">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="60cf5-173">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="60cf5-174"><strong>GoToControl</strong></span><span class="sxs-lookup"><span data-stu-id="60cf5-174"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="60cf5-175"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="60cf5-175"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="60cf5-176">Accédez au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="60cf5-176">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

