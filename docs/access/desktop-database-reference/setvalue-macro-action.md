---
title: SetValue, action de macro
TOCTitle: SetValue Macro Action
ms:assetid: a08be0c1-a053-45f9-b4ae-709fedc58e8b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820771(v=office.15)
ms:contentKeyID: 48546712
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f845dc5512611aa948991ad2099169a25bbcb113
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469310"
---
# <a name="setvalue-macro-action"></a><span data-ttu-id="1ad4c-102">SetValue, action de macro</span><span class="sxs-lookup"><span data-stu-id="1ad4c-102">SetValue Macro Action</span></span>


<span data-ttu-id="1ad4c-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1ad4c-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="1ad4c-104">Vous pouvez utiliser l'action **DéfinirValeur** pour définir la valeur d'un champ, d'un contrôle ou d'une propriété Microsoft Access dans un formulaire, un formulaire feuille de données ou un état.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-104">You can use the **SetValue** action to set the value of a Microsoft Access field, control, or property on a form, a form datasheet, or a report.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1ad4c-105">[!REMARQUE] Vous ne pouvez pas utiliser l'action <STRONG>DéfinirValeur</STRONG> pour définir la valeur d'une propriété Access qui renvoie un objet.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-105">You cannot use the <STRONG>SetValue</STRONG> action to set the value of an Access property that returns an object.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="1ad4c-p101">[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p101">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="1ad4c-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="1ad4c-108">Setting</span></span>

<span data-ttu-id="1ad4c-109">L'action **DéfinirValeur** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-109">The **SetValue** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ad4c-110">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="1ad4c-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="1ad4c-111">Description</span><span class="sxs-lookup"><span data-stu-id="1ad4c-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ad4c-112"><strong>Item</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-112"><strong>Item</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-p102">Nom du champ, du contrôle ou de la propriété dont vous souhaitez définir la valeur. Entrez le nom du champ, du contrôle ou de la propriété dans la zone <strong>Élément</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Vous devez utiliser la syntaxe complète pour faire référence à cet élément, telle que <em>nom_contrôle</em> (pour un contrôle dans le formulaire ou l’état à partir duquel la macro a été appelée) ou <strong>Forms</strong>!<em>nom_formulaire</em>!<em>nom_contrôle</em>. Cet argument est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p102">The name of the field, control, or property whose value you want to set. Enter the field, control, or property name in the <strong>Item</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. You must use the full syntax to refer to this item, such as <em>controlname</em> (for a control on the form or report from which the macro was called) or <strong>Forms</strong>!<em>formname</em>!<em>controlname</em>. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad4c-117"><strong>Expression</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-117"><strong>Expression</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-p103">Expression utilisée par Access pour définir la valeur de cet élément. Vous devez toujours utiliser la syntaxe complète pour faire référence à des objets dans l’expression. Par exemple, pour augmenter la valeur d’un contrôle Salaire dans un formulaire Employés de 10 pour cent, utilisez Forms!Employees!Salary\*1.1.. Il s’agit d’un argument obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p103">The expression Access uses to set the value for this item. You must always use the full syntax to refer to any objects in the expression. For example, to increase the value in a Salary control on an Employees form by 10 percent, use Forms!Employees!Salary\*1.1. This is a required argument.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="1ad4c-122">Vous ne devez pas utiliser un signe égal (<STRONG>=</STRONG>) avant l’expression dans cet argument.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-122">You shouldn't use an equal sign (<STRONG>=</STRONG>) before the expression in this argument.</span></span> <span data-ttu-id="1ad4c-123">Si vous le faites, Access évalue l’expression, puis utilise cette valeur comme expression dans cet argument.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-123">If you do, Access evaluates the expression and then uses this value as the expression in this argument.</span></span> <span data-ttu-id="1ad4c-124">Cela peut produire des résultats inattendus si l’expression est une chaîne.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-124">This can produce unexpected results if the expression is a string.</span></span></P>


<p><span data-ttu-id="1ad4c-125">Par exemple, si vous tapez <strong> = &quot;chaîne1&quot; </strong> à cet argument, Access évalue l’expression comme chaîne1 d’abord.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-125">For example, if you type <strong>=&quot;String1&quot;</strong> for this argument, Access first evaluates the expression as String1.</span></span> <span data-ttu-id="1ad4c-126">Il utilise ensuite Chaîne1 comme expression dans cet argument, s’attendant à trouver un contrôle ou la propriété nommé Chaîne1 dans le formulaire ou l’état qui a appelé la macro.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-126">Then it uses String1 as the expression in this argument, expecting to find a control or property named String1 on the form or report that called the macro.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="1ad4c-127">[!REMARQUE] Dans une base de données Access (.mdb ou .accdb), cliquez sur le bouton <STRONG>Générer</STRONG> pour utiliser le Générateur d'expression et créer une expression pour l'un de ces arguments.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-127">In an Access database (.mdb or .accdb), click the <STRONG>Build</STRONG> button to use the Expression Builder to create an expression for either of these arguments.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="1ad4c-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="1ad4c-128">Remarks</span></span>

<span data-ttu-id="1ad4c-p106">Vous pouvez utiliser cette action pour définir une valeur pour un champ ou un contrôle dans un formulaire, un formulaire feuille de données ou un état. Vous pouvez également définir la valeur de presque toutes les propriétés de contrôle, de formulaire et d'état dans n'importe quel affichage. Pour déterminer si une propriété spécifique peut être configurée à l'aide d'une macro et les affichages pouvant être définis, consultez la rubrique d'aide relative à cette propriété dans Visual Basic Editor.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p106">You can use this action to set a value for a field or control on a form, a form datasheet, or a report. You can also set the value for almost all control, form, and report properties in any view. To find out whether a particular property can be set by using a macro and which views it can be set in, see the Help topic for that property in the Visual Basic Editor.</span></span>

<span data-ttu-id="1ad4c-132">Vous pouvez également définir la valeur d'un champ dans la table sous-jacente d'un formulaire, même si le formulaire ne contient pas de contrôle lié au champ.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-132">You can also set the value for a field in a form's underlying table even if the form doesn't contain a control bound to the field.</span></span> <span data-ttu-id="1ad4c-133">Utilisez la syntaxe **Forms**\!*formname*\!*fieldname* dans la zone **élément** pour définir la valeur pour ce champ.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-133">Use the syntax **Forms**\!*formname*\!*fieldname* in the **Item** box to set the value for such a field.</span></span> <span data-ttu-id="1ad4c-134">Vous pouvez également faire référence à un champ de table sous-jacente d’un état à l’aide de la syntaxe de **rapports**\!*reportname*\!*fieldname*, mais il doit exister un contrôle dépendant de ce champ ou le champ doit être référencé en une contrôle calculé dans l’état.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-134">You can also refer to a field in a report's underlying table by using the syntax **Reports**\!*reportname*\!*fieldname*, but there must be a control on the report bound to this field, or the field must be referred to in a calculated control on the report.</span></span>

<span data-ttu-id="1ad4c-p108">Si vous définissez la valeur d'un contrôle dans un formulaire, l'action **DéfinirValeur** ne déclenche pas les règles de validation au niveau du formulaire du contrôle, mais elle déclenche les règles de validation au niveau de la table du champ sous-jacent si le contrôle est un contrôle lié. L'action **DéfinirValeur** déclenche également le recalcul, mais ce dernier peut ne pas avoir lieu immédiatement. Pour déclencher la mise à jour immédiate et forcer l'exécution du recalcul, utilisez l'action **RedessinerObjet**. La valeur que vous définissez dans un contrôle à l'aide de l'action **DéfinirValeur** est également non affectée par un masque de saisie défini dans la propriété **InputMask** du contrôle ou du champ sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p108">If you set the value of a control on a form, the **SetValue** action doesn't trigger the control's form-level validation rules, but it does trigger the underlying field's table-level validation rules if the control is a bound control. The **SetValue** action also triggers recalculation, but the recalculation may not happen immediately. To trigger immediate repainting and force the recalculation to completion, use the **RepaintObject** action. The value you set in a control by using the **SetValue** action is also not affected by an input mask set in the control's or underlying field's **InputMask** property.</span></span>

<span data-ttu-id="1ad4c-p109">Pour modifier la valeur d'un contrôle, vous pouvez utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **AfterUpdate** du contrôle. Toutefois, vous ne pouvez pas utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété de type événement **BeforeUpdate** d'un contrôle pour modifier la valeur du contrôle (bien que vous puissiez utiliser l'action **DéfinirValeur** pour modifier la valeur d'autres contrôles). Vous pouvez également utiliser l'action **DéfinirValeur** dans une macro spécifiée par la propriété **AvantMAJ** ou **AprèsMAJ** d'un formulaire pour modifier la valeur de tous les contrôles de l'enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p109">To change the value of a control, you can use the **SetValue** action in a macro specified by the control's **AfterUpdate** event property. However, you can't use the **SetValue** action in a macro specified by a control's **BeforeUpdate** event property to change the value of the control (although you can use the **SetValue** action to change the value of other controls). You can also use the **SetValue** action in a macro specified by the **BeforeUpdate** or **AfterUpdate** property of a form to change the value of any controls in the current record.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1ad4c-142">Vous ne pouvez pas utiliser l’action <STRONG>DéfinirValeur</STRONG> pour définir la valeur des contrôles suivants :</span><span class="sxs-lookup"><span data-stu-id="1ad4c-142">You can't use the <STRONG>SetValue</STRONG> action to set the value of the following controls:</span></span></P>
> <UL>
> <LI>
> <P><span data-ttu-id="1ad4c-143">Les contrôles dépendants et les contrôles calculés dans des états.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-143">Bound controls and calculated controls on reports.</span></span></P>
> <LI>
> <P><span data-ttu-id="1ad4c-144">Les contrôles calculés dans des formulaires.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-144">Calculated controls on forms.</span></span></P></LI></UL>




> [!TIP]
> <P><span data-ttu-id="1ad4c-p110">Vous pouvez utiliser l’action <STRONG>DéfinirValeur</STRONG> pour masquer ou afficher un formulaire en mode Formulaire. Entrez <STRONG>Forms</STRONG>!<EM>nom_formulaire</EM><STRONG>.Visible</STRONG> dans la zone <STRONG>Élément</STRONG>, et <STRONG>Non</STRONG> ou <STRONG>Oui</STRONG> dans la zone <STRONG>Expression</STRONG>. La définition de la propriété <STRONG>Visible</STRONG> d’un formulaire modal sur <STRONG>Non</STRONG> masque le formulaire et le rend non modal. La définition de la propriété sur <STRONG>Oui</STRONG> affiche le formulaire et le rend à nouveau modal.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p110">You can use the <STRONG>SetValue</STRONG> action to hide or show a form in Form view. Enter <STRONG>Forms</STRONG>!<EM>formname</EM><STRONG>.Visible</STRONG> in the <STRONG>Item</STRONG> box and <STRONG>No</STRONG> or <STRONG>Yes</STRONG> in the <STRONG>Expression</STRONG> box. Setting a modal form's <STRONG>Visible</STRONG> property to <STRONG>No</STRONG> hides the form and makes it modeless. Setting the property to <STRONG>Yes</STRONG> displays the form and makes it modal again.</span></span></P>



<span data-ttu-id="1ad4c-p111">La modification de la valeur ou l'ajout des nouvelles données dans un contrôle à l'aide de l'action **DéfinirValeur** dans une macro ne déclenche pas des événements tels que **AvantMAJ**, **AvantInsertion** ou **Modifier** qui se produisent lorsque vous modifiez ou entrez des données dans ces contrôles dans l'interface utilisateur. Ces événements ne se produisent pas non plus si vous définissez la valeur du contrôle à l'aide d'un module Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p111">Changing the value of or adding new data in a control by using the **SetValue** action in a macro doesn't trigger events such as **BeforeUpdate**, **BeforeInsert**, or **Change** that occur when you change or enter data in these controls in the user interface. These events also don't occur if you set the value of the control by using a Visual Basic for Applications (VBA) module.</span></span>

<span data-ttu-id="1ad4c-p112">Cette action n'est pas disponible dans un module VBA. Définissez la valeur directement en langage VBA.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p112">This action isn't available in a VBA module. Set the value directly in VBA.</span></span>

## <a name="example"></a><span data-ttu-id="1ad4c-153">Exemple</span><span class="sxs-lookup"><span data-stu-id="1ad4c-153">Example</span></span>

<span data-ttu-id="1ad4c-154">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="1ad4c-154">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="1ad4c-p113">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-p113">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the SupplierID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the CategoryID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ad4c-160">Action</span><span class="sxs-lookup"><span data-stu-id="1ad4c-160">Action</span></span></p></th>
<th><p><span data-ttu-id="1ad4c-161">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="1ad4c-161">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="1ad4c-162">Commentaire</span><span class="sxs-lookup"><span data-stu-id="1ad4c-162">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ad4c-163"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-163"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-164"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-164"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-165">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-165">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad4c-166"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-166"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-167"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-167"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-168">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-168">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad4c-169"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-169"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-170"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-170"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-171">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-171">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ad4c-172"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-172"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-173"><strong>Élément</strong>: [Forms]![Produits]! [N° fournisseur] <strong>Expression</strong>: N° fournisseur  </span><span class="sxs-lookup"><span data-stu-id="1ad4c-173"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="1ad4c-174">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-174">Set the SupplierID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ad4c-175"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="1ad4c-175"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="1ad4c-176"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="1ad4c-176"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="1ad4c-177">Accédez au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="1ad4c-177">Go to the CategoryID control.</span></span></p></td>
</tr>
</tbody>
</table>

