---
title: Action de macro OuvrirFormulaire
TOCTitle: OpenForm Macro Action
ms:assetid: c519a9d7-99d4-4765-ad96-59c3fe1be9e3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823095(v=office.15)
ms:contentKeyID: 48547604
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba0314fff63014b36565b178f97950660ffec14f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472106"
---
# <a name="openform-macro-action"></a><span data-ttu-id="b75be-102">Action de macro OuvrirFormulaire</span><span class="sxs-lookup"><span data-stu-id="b75be-102">OpenForm Macro Action</span></span>


<span data-ttu-id="b75be-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b75be-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="b75be-p101">Faites appel à l'action **OuvrirFormulaire** pour ouvrir un formulaire en mode Formulaire, Création, Aperçu avant impression ou Feuille de données. Vous pouvez sélectionner des modes d'affichage et de saisie des données pour le formulaire et limiter les enregistrements affichés par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b75be-p101">You can use the **OpenForm** action to open a form in Form view, Design view, Print Preview, or Datasheet view. You can select data entry and window modes for the form and restrict the records that the form displays.</span></span>

## <a name="setting"></a><span data-ttu-id="b75be-106">Paramètre</span><span class="sxs-lookup"><span data-stu-id="b75be-106">Setting</span></span>

<span data-ttu-id="b75be-107">L'action **OuvrirFormulaire** utilise les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="b75be-107">The **OpenForm** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b75be-108">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="b75be-108">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b75be-109">Description</span><span class="sxs-lookup"><span data-stu-id="b75be-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b75be-110"><strong>Nom du formulaire</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-110"><strong>Form Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-p102">Nom du formulaire à ouvrir. La zone <strong>Nom du formulaire</strong> dans la section <strong>Arguments de l'action</strong> du volet Générateur de macro présente tous les formulaires dans la base de données actuelle. Il s'agit d'un argument obligatoire. Si vous exécutez une macro contenant l'action <strong>OuvrirFormulaire</strong> dans une base de données bibliothèque, Microsoft Access recherche d'abord le formulaire portant ce nom dans la base de données bibliothèque, puis dans la base de données actuelle.  </span><span class="sxs-lookup"><span data-stu-id="b75be-p102">The name of the form to open. The <strong>Form Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all forms in the current database. This is a required argument. If you run a macro containing the <strong>OpenForm</strong> action in a library database, Microsoft Access first looks for the form with this name in the library database, and then in the current database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-115"><strong>Affichage</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-115"><strong>View</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-p103">Affichage dans lequel le formulaire s'ouvre. Cliquez sur <strong>Formulaire</strong>, <strong>Création</strong>, <strong>Aperçu avant impression</strong>, <strong>Feuille de données</strong>, <strong>Tableau croisé dynamique</strong> ou <strong>Graphique croisé dynamique</strong> dans la zone <strong>Affichage</strong>. La valeur par défaut est <strong>Formulaire</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b75be-p103">The view in which the form will open. Click <strong>Form</strong>, <strong>Design</strong>, <strong>Print Preview</strong>, <strong>Datasheet</strong>, <strong>PivotTable</strong>, or <strong>PivotChart</strong> in the <strong>View</strong> box. The default is <strong>Form</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b75be-p104">Le paramètre d’argument <STRONG>View</STRONG> remplace les paramètres des propriétés <STRONG>DefaultView</STRONG> et <STRONG>ViewsAllowed</STRONG> du formulaire. Par exemple, si la propriété <STRONG>ViewsAllowed</STRONG> d’un formulaire est définie sur <STRONG>Feuille de données</STRONG>, vous pouvez toujours utiliser l’action <STRONG>OuvrirFormulaire</STRONG> pour ouvrir le formulaire en mode Formulaire.</span><span class="sxs-lookup"><span data-stu-id="b75be-p104">The <STRONG>View</STRONG> argument setting overrides the settings of the form's <STRONG>DefaultView</STRONG> and <STRONG>ViewsAllowed</STRONG> properties. For example, if a form's <STRONG>ViewsAllowed</STRONG> property is set to <STRONG>Datasheet</STRONG>, you can still use the <STRONG>OpenForm</STRONG> action to open the form in Form view.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b75be-121"><strong>Nom du filtre</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-121"><strong>Filter Name</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-p105">Filtre qui limite ou trie les enregistrements du formulaire. Vous pouvez entrer le nom d'une requête existante ou d'un filtre enregistré en tant que requête. La requête doit toutefois inclure tous les champs du formulaire que vous ouvrez, ou sa propriété <strong>OutputAllFields</strong> doit avoir la valeur <strong>Oui</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b75be-p105">A filter that restricts or sorts the form's records. You can enter the name of either an existing query or a filter that was saved as a query. However, the query must include all the fields in the form you are opening or have its <strong>OutputAllFields</strong> property set to <strong>Yes</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-125"><strong>Condition Where</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-125"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-126">Clause ou expression WHERE SQL valable (sans le mot WHERE) utilisée par Access pour sélectionner des enregistrements dans la table ou requête sous-jacente du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b75be-126">A valid SQL WHERE clause (without the word WHERE) or expression that Access uses to select records from the form's underlying table or query.</span></span> <span data-ttu-id="b75be-127">Si vous sélectionnez un filtre avec l'argument <strong>Filter Name</strong>, Access applique cette clause WHERE aux résultats du filtre.</span><span class="sxs-lookup"><span data-stu-id="b75be-127">If you select a filter with the <strong>Filter Name</strong> argument, Access applies this WHERE clause to the results of the filter.</span></span> <span data-ttu-id="b75be-128">Pour ouvrir un formulaire et limiter ses enregistrements à ceux spécifiés par la valeur d’un contrôle sur un autre formulaire, utilisez l’expression suivante : <strong>[</strong><em>fieldname</em><strong>] = Forms ! [</strong> <em>FormName</em> <strong>]! [</strong> <em>NomChamp<em>NomContrôle autre formulaire</em><strong>]</strong> portant le nom d’un champ dans la table ou requête du formulaire à ouvrir sous-jacente</em> .</span><span class="sxs-lookup"><span data-stu-id="b75be-128">To open a form and restrict its records to those specified by the value of a control on another form, use the following expression: <strong>[</strong><em>fieldname</em><strong>] = Forms![</strong><em>formname</em><strong>]![</strong><em>controlname on other form</em><strong>]</strong> Replace <em>fieldname</em> with the name of a field in the underlying table or query of the form you want to open.</span></span> <span data-ttu-id="b75be-129">Remplacez le nom de l’autre formulaire et du contrôle dans l’autre formulaire qui contient la valeur à laquelle les enregistrements du premier formulaire correspondent <em>formname</em> et <em>controlname sur un autre formulaire</em> .</span><span class="sxs-lookup"><span data-stu-id="b75be-129">Replace <em>formname</em> and <em>controlname on other form</em> with the name of the other form and the control on the other form that contains the value you want records in the first form to match.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b75be-p107">La longueur maximale de l’argument <STRONG>Where Condition</STRONG> est de 255 caractères. Si vous devez entrer une clause SQL WHERE plus complexe et plus longue, utilisez plutôt la méthode <STRONG>OpenForm</STRONG> de l’objet <STRONG>DoCmd</STRONG> d’un module Visual Basic pour Applications (VBA). VBA vous permet d’entrer des instructions de clause SQL WHERE comportant jusqu’à 32 768 caractères.</span><span class="sxs-lookup"><span data-stu-id="b75be-p107">The maximum length of the <STRONG>Where Condition</STRONG> argument is 255 characters. If you need to enter a more complex SQL WHERE clause longer than this, use the <STRONG>OpenForm</STRONG> method of the <STRONG>DoCmd</STRONG> object in a Visual Basic for Applications (VBA) module instead. You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b75be-133"><strong>Mode Données</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-133"><strong>Data Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-p108">Mode de saisie de données du formulaire. S'applique uniquement aux formulaires ouverts en mode Formulaire ou Feuille de données. Cliquez sur <strong>Ajouter</strong> (l'utilisateur ne peut pas modifier les enregistrements existants, mais peut en ajouter de nouveaux), <strong>Modifier</strong> (l'utilisateur peut modifier les enregistrements existants et en ajouter de nouveaux) ou <strong>Lecture seule</strong> (l'utilisateur peut uniquement consulter les enregistrements). La valeur par défaut est <strong>Modifier</strong>. <strong>Notes</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-p108">The data entry mode for the form. This applies only to forms opened in Form view or Datasheet view. Click <strong>Add</strong> (the user can add new records but can't edit existing records), <strong>Edit</strong> (the user can edit existing records and add new records), or <strong>Read Only</strong> (the user can only view records). The default is <strong>Edit</strong>. <strong>Notes</strong></span></span></p>
<ul>
<li><p><span data-ttu-id="b75be-p109">Le paramètre d'argument <strong>Mode Données</strong> remplace les paramètres des propriétés <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> et <strong>DataEntry</strong> du formulaire. Par exemple, si la propriété <strong>AllowEdits</strong> d'un formulaire est définie sur <strong>Non</strong>, vous pouvez toujours utiliser l'action <strong>OuvrirFormulaire</strong> pour ouvrir le formulaire en mode Édition.  </span><span class="sxs-lookup"><span data-stu-id="b75be-p109">The <strong>Data Mode</strong> argument setting overrides the settings of the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties. For example, if a form's <strong>AllowEdits</strong> property is set to <strong>No</strong>, you can still use the <strong>OpenForm</strong> action to open the form in Edit mode.</span></span></p></li>
<li><p><span data-ttu-id="b75be-141">Si vous laissez cet argument vide, Access ouvre le formulaire dans le mode d'entrée de données défini par les propriétés <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong> et <strong>DataEntry</strong> du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b75be-141">If you leave this argument blank, Access opens the form in the data entry mode set by the form's <strong>AllowEdits</strong>, <strong>AllowDeletions</strong>, <strong>AllowAdditions</strong>, and <strong>DataEntry</strong> properties.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-142"><strong>Mode Fenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-142"><strong>Window Mode</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-p110">Mode de fenêtre dans laquelle le formulaire s'ouvre. Cliquez sur <strong>Normal</strong> (le formulaire s'ouvre dans le mode défini par ses propriétés), <strong>Masqué</strong> (le formulaire est masqué), <strong>Icône</strong> (le formulaire s'ouvre à la taille réduite sous la forme d'une barre de titre en bas de l'écran) ou <strong>Boîte de dialogue</strong> (les propriétés <strong>Modal</strong> et <strong>PopUp</strong> du formulaire sont définies sur <strong>Oui</strong>). La valeur par défaut est <strong>Normal</strong>.  </span><span class="sxs-lookup"><span data-stu-id="b75be-p110">The window mode in which the form opens. Click <strong>Normal</strong> (the form opens in the mode set by its properties), <strong>Hidden</strong> (the form is hidden), <strong>Icon</strong> (the form opens minimized as a small title bar at the bottom of the screen), or <strong>Dialog</strong> (the form's <strong>Modal</strong> and <strong>PopUp</strong> properties are set to <strong>Yes</strong>). The default is <strong>Normal</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="b75be-p111">Certains paramètres de l’argument <STRONG>Window Mode</STRONG> ne s’appliquent pas lors de l’utilisation de documents à onglets. Pour passer à des fenêtres superposées :</span><span class="sxs-lookup"><span data-stu-id="b75be-p111">Some <STRONG>Window Mode</STRONG> argument settings do not apply when using tabbed documents. To switch to overlapping windows:</span></span></P>


<p></p>
<ol>
<li><p><span data-ttu-id="b75be-148">Cliquez sur l’onglet fichier, puis cliquez sur <strong>Options</strong>.</span><span class="sxs-lookup"><span data-stu-id="b75be-148">Click the File tab and then click <strong>Options</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b75be-149">Dans la boîte dialogue <strong>Options Access</strong>, cliquez sur <strong>Base de données active</strong>.</span><span class="sxs-lookup"><span data-stu-id="b75be-149">In the <strong>Access Options</strong> dialog box, click <strong>Current Database</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b75be-150">Dans la section <strong>Options de l’application</strong>, sous <strong>Options de la fenêtre Document</strong>, cliquez sur <strong>Fenêtres superposées</strong>.</span><span class="sxs-lookup"><span data-stu-id="b75be-150">In the <strong>Application Options</strong>section, under <strong>Document Window Options</strong>, click <strong>Overlapping Windows</strong>.</span></span></p></li>
<li><p><span data-ttu-id="b75be-151">Cliquez sur <strong>OK</strong>, puis fermez et rouvrez la base de données.</span><span class="sxs-lookup"><span data-stu-id="b75be-151">Click <strong>OK</strong>, then close and reopen the database.</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b75be-152">Remarques</span><span class="sxs-lookup"><span data-stu-id="b75be-152">Remarks</span></span>

<span data-ttu-id="b75be-153">Cette action équivaut à double-cliquer sur un formulaire dans le volet de navigation ou à cliquer avec le bouton droit sur le formulaire dans le volet de navigation et à choisir un affichage.</span><span class="sxs-lookup"><span data-stu-id="b75be-153">This action is similar to double-clicking a form in the Navigation Pane, or right-clicking the form in the Navigation Pane and then selecting a view.</span></span>

<span data-ttu-id="b75be-p112">Un formulaire peut être modal (il doit être fermé ou masqué avant que l'utilisateur puisse effectuer une autre action) ou non modal (l'utilisateur peut accéder à d'autres fenêtres lorsque le formulaire est ouvert). Il peut également être contextuel (un formulaire utilisé pour collecter ou afficher des informations qui reste au-dessus des autres fenêtres Access). Vous définissez les propriétés **Modal** et **PopUp** lorsque vous créez le formulaire. Si vous utilisez **Normal** pour l'argument **Mode fenêtre**, le formulaire s'ouvre dans le mode spécifié par les paramètres de ces propriétés. Si vous utilisez **Boîte de dialogue** pour l'argument **Mode fenêtre**, ces propriétés sont définies sur **Oui**. Un formulaire ouvert masqué ou sous forme d'icône retourne au mode spécifié par ses paramètres de propriété lorsque vous l'affichez ou le restaurez.</span><span class="sxs-lookup"><span data-stu-id="b75be-p112">A form can be modal (it must be closed or hidden before the user can perform any other action) or modeless (the user can move to other windows while the form is open). It can also be a pop-up form (a form used to collect or display information that remains on top of all other Access windows). You set the **Modal** and **PopUp** properties when you design the form. If you use **Normal** for the **Window Mode** argument, the form opens in the mode specified by these property settings. If you use **Dialog** for the **Window Mode** argument, these properties are both set to **Yes**. A form opened as hidden or as an icon returns to the mode specified by its property settings when you show or restore it.</span></span>

<span data-ttu-id="b75be-p113">Lorsque vous ouvrez un formulaire avec l'argument **Mode fenêtre** défini sur **Boîte de dialogue**, Access suspend la macro jusqu'à ce que le formulaire soit fermé ou masqué. Vous pouvez masquer un formulaire en définissant sa propriété **Visible** sur **Non** à l'aide de l'action **DéfinirValeur**.</span><span class="sxs-lookup"><span data-stu-id="b75be-p113">When you open a form with the **Window Mode** argument set to **Dialog**, Access suspends the macro until the form is closed or hidden. You can hide a form by setting its **Visible** property to **No** by using the **SetValue** action.</span></span>


> [!TIP]
> <P><span data-ttu-id="b75be-p114">[!CONSEIL] Vous pouvez sélectionner un formulaire dans le volet de navigation et le faire glisser vers une ligne d'action de macro. Ceci crée automatiquement une action <STRONG>OuvrirFonction</STRONG> qui ouvre le formulaire en mode Formulaire.</span><span class="sxs-lookup"><span data-stu-id="b75be-p114">You can select a form in the Navigation Pane and drag it to a macro action row. This automatically creates an <STRONG>OpenForm</STRONG> action that opens the form in Form view.</span></span></P>



<span data-ttu-id="b75be-164">Le filtre et la condition WHERE que vous appliquez deviennent les paramètres de la propriété **Filter** du formulaire.</span><span class="sxs-lookup"><span data-stu-id="b75be-164">The filter and WHERE condition you apply become the setting of the form's **Filter** property.</span></span>

## <a name="examples"></a><span data-ttu-id="b75be-165">Exemples</span><span class="sxs-lookup"><span data-stu-id="b75be-165">Examples</span></span>

<span data-ttu-id="b75be-166">**Définissez la valeur d'un contrôle en utilisant une macro**</span><span class="sxs-lookup"><span data-stu-id="b75be-166">**Set the value of a control by using a macro**</span></span>

<span data-ttu-id="b75be-p115">La macro suivante ouvre le formulaire Ajouter des produits à partir d'un bouton dans le formulaire Fournisseurs. Elle présente l'utilisation des actions **Écho**, **FermerFenêtre**, **OuvrirFormulaire**, **DéfinirValeur** et **AtteindreContrôle**. L'action **DéfinirValeur** définit le contrôle N° fournisseur dans le formulaire Produits sur le fournisseur actif dans le formulaire Fournisseurs. L'action **AtteindreContrôle** déplace ensuite le focus vers le champ N° catégorie, où vous pouvez commencer à entrer des données pour le nouveau produit. Cette macro doit être associée au bouton Ajouter des produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b75be-p115">The following macro opens the Add Products form from a button on the Suppliers form. It shows the use of the **Echo**, **CloseWindow**, **OpenForm**, **SetValue**, and **GoToControl** actions. The **SetValue** action sets the Supplier ID control on the Products form to the current supplier on the Suppliers form. The **GoToControl** action then moves the focus to the Category ID field, where you can begin to enter data for the new product. This macro should be attached to the Add Products button on the Suppliers form.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b75be-172">Action</span><span class="sxs-lookup"><span data-stu-id="b75be-172">Action</span></span></p></th>
<th><p><span data-ttu-id="b75be-173">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="b75be-173">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b75be-174">Commentaire</span><span class="sxs-lookup"><span data-stu-id="b75be-174">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b75be-175"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-175"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-176"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-176"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-177">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="b75be-177">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-178"><strong>FermerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-178"><strong>CloseWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-179"><strong>Type d’objet</strong>: <strong>FormObject nom</strong>: produit liste <strong>Enregistrer</strong>: <strong>non</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-179"><strong>Object Type</strong>: <strong>FormObject Name</strong>: Product List <strong>Save</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-180">Fermer le formulaire Liste des produits.</span><span class="sxs-lookup"><span data-stu-id="b75be-180">Close the Product List form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b75be-181"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-181"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-182"><strong>Nom du formulaire</strong>: <strong>affichage</strong>des produits : <strong>Mode FormData</strong>: <strong>Mode fenêtre Ajouter</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-182"><strong>Form Name</strong>: Products <strong>View</strong>: <strong>FormData Mode</strong>: <strong>AddWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-183">Ouvrir le formulaire Produits.</span><span class="sxs-lookup"><span data-stu-id="b75be-183">Open the Products form.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-184"><strong>DéfinirValeur</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-184"><strong>SetValue</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-185"><strong>Élément</strong>: [Forms]![Produits]![N° fournisseur] <strong>Expression</strong>: N° fournisseur</span><span class="sxs-lookup"><span data-stu-id="b75be-185"><strong>Item</strong>: [Forms]![Products]![SupplierID] <strong>Expression</strong>: SupplierID</span></span></p></td>
<td><p><span data-ttu-id="b75be-186">Définissez le contrôle N° fournisseur sur le fournisseur actuel dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b75be-186">Set the Supplier ID control to the current supplier on the Suppliers form.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b75be-187"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-187"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-188"><strong>Nom du contrôle</strong>: N° catégorie</span><span class="sxs-lookup"><span data-stu-id="b75be-188"><strong>Control Name</strong>: CategoryID</span></span></p></td>
<td><p><span data-ttu-id="b75be-189">Accéder au contrôle N° catégorie.</span><span class="sxs-lookup"><span data-stu-id="b75be-189">Go to the Category ID control.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b75be-p116">La macro suivante ouvre un formulaire de liste de produits dans le coin inférieur droit du formulaire Fournisseurs, affichant les produits du fournisseur actuel. Elle présente l'utilisation des actions **Écho**, **ZoneMessage**, **AtteindreContrôle**, **ArrêtMacro**, **OuvrirFormulaire** et **DéplacerEtDimensionnerFenêtre**. Elle décrit également l'utilisation d'une expression conditionnelle avec les actions **ZoneMessage**, **AtteindreContrôle**, et **ArrêtMacro**. Cette macro doit être associée au bouton Consulter les produits dans le formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b75be-p116">The following macro opens a Product List form in the lower-right corner of the Suppliers form, displaying the current supplier's products. It shows the use of the **Echo**, **MessageBox**, **GoToControl**, **StopMacro**, **OpenForm**, and **MoveAndSizeWindow** actions. It also shows the use of a conditional expression with the **MessageBox**, **GoToControl**, and **StopMacro** actions. This macro should be attached to the Review Products button on the Suppliers form.</span></span>

<span data-ttu-id="b75be-194">**Synchroniser des formulaires à l'aide d'une macro**</span><span class="sxs-lookup"><span data-stu-id="b75be-194">**Synchronize forms by using a macro**</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b75be-195">Condition</span><span class="sxs-lookup"><span data-stu-id="b75be-195">Condition</span></span></p></th>
<th><p><span data-ttu-id="b75be-196">Action</span><span class="sxs-lookup"><span data-stu-id="b75be-196">Action</span></span></p></th>
<th><p><span data-ttu-id="b75be-197">Arguments : Paramètre</span><span class="sxs-lookup"><span data-stu-id="b75be-197">Arguments: Setting</span></span></p></th>
<th><p><span data-ttu-id="b75be-198">Commentaire</span><span class="sxs-lookup"><span data-stu-id="b75be-198">Comment</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b75be-199"><strong>Écho</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-199"><strong>Echo</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-200"><strong>Écho sur</strong>: <strong>Non</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-200"><strong>Echo On</strong>: <strong>No</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-201">Arrêter l'actualisation de l'écran pendant l'exécution de la macro.</span><span class="sxs-lookup"><span data-stu-id="b75be-201">Stop screen updating while the macro is running.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-202">IsNull([N° fournisseur])</span><span class="sxs-lookup"><span data-stu-id="b75be-202">IsNull([SupplierID])</span></span></p></td>
<td><p><span data-ttu-id="b75be-203"><strong>ZoneMessage</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-203"><strong>MessageBox</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-204"><strong>Message</strong>: Passez à l'enregistrement du fournisseur dont vous voulez voir les produits, puis cliquez à nouveau sur le bouton Consulter les produits.</span><span class="sxs-lookup"><span data-stu-id="b75be-204"><strong>Message</strong>: Move to the supplier record whose products you want to see, then click the Review Products button again.</span></span> <span data-ttu-id="b75be-205"><strong>Bip</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: sélectionnez un fournisseur</span><span class="sxs-lookup"><span data-stu-id="b75be-205"><strong>Beep</strong>: <strong>YesType</strong>: <strong>NoneTitle</strong>: Select a Supplier</span></span></p></td>
<td><p><span data-ttu-id="b75be-206">S'il n'existe aucun fournisseur actif dans le formulaire Fournisseurs, afficher un message.</span><span class="sxs-lookup"><span data-stu-id="b75be-206">If there is no current supplier on the Suppliers form, display a message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b75be-207">...</span><span class="sxs-lookup"><span data-stu-id="b75be-207"></span></span></p></td>
<td><p><span data-ttu-id="b75be-208"><strong>AtteindreContrôle</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-208"><strong>GoToControl</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-209"><strong>Nom du contrôle</strong>: NomSociété</span><span class="sxs-lookup"><span data-stu-id="b75be-209"><strong>Control Name</strong>: CompanyName</span></span></p></td>
<td><p><span data-ttu-id="b75be-210">Déplacer le focus sur le contrôle NomSociété.</span><span class="sxs-lookup"><span data-stu-id="b75be-210">Move focus to the CompanyName control.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b75be-211">...</span><span class="sxs-lookup"><span data-stu-id="b75be-211"></span></span></p></td>
<td><p><span data-ttu-id="b75be-212"><strong>ArrêtMacro</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-212"><strong>StopMacro</strong></span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="b75be-213">Arrêter la macro.</span><span class="sxs-lookup"><span data-stu-id="b75be-213">Stop the macro.</span></span></p></td>
</tr>
<tr class="odd">
<td><p></p></td>
<td><p><span data-ttu-id="b75be-214"><strong>OuvrirFormulaire</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-214"><strong>OpenForm</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-215"><strong>Nom du formulaire</strong>: produit liste <strong>affichage</strong>: <strong>DatasheetFilter nom</strong>: <strong>Condition Where</strong>: [n° fournisseur] = [Forms] ! [Fournisseurs] ! [N° fournisseur] <strong>Mode données</strong>: <strong>Le Mode lecture OnlyWindow</strong>: <strong>Normal</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-215"><strong>Form Name</strong>: Product List <strong>View</strong>: <strong>DatasheetFilter Name</strong>: <strong>Where Condition</strong>: [SupplierID] = [Forms]![Suppliers]![SupplierID] <strong>Data Mode</strong>: <strong>Read OnlyWindow Mode</strong>: <strong>Normal</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-216">Ouvrir le formulaire Liste de produits et afficher les produits du fournisseur actuel.</span><span class="sxs-lookup"><span data-stu-id="b75be-216">Open the Product List form and show the current supplier's products.</span></span></p></td>
</tr>
<tr class="even">
<td><p></p></td>
<td><p><span data-ttu-id="b75be-217"><strong>DéplacerEtDimensionnerFenêtre</strong></span><span class="sxs-lookup"><span data-stu-id="b75be-217"><strong>MoveAndSizeWindow</strong></span></span></p></td>
<td><p><span data-ttu-id="b75be-218"><strong>Droite</strong>: 0.7799&quot; <strong>vers le bas</strong>: 1,8&quot;</span><span class="sxs-lookup"><span data-stu-id="b75be-218"><strong>Right</strong>: 0.7799&quot; <strong>Down</strong>: 1.8&quot;</span></span></p></td>
<td><p><span data-ttu-id="b75be-219">Positionnez le formulaire Liste de produits dans le coin inférieur droit du formulaire Fournisseurs.</span><span class="sxs-lookup"><span data-stu-id="b75be-219">Position the Product List form in the lower right of the Suppliers form.</span></span></p></td>
</tr>
</tbody>
</table>

