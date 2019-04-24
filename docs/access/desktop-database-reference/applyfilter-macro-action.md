---
title: ApplyFilter, action de macro
TOCTitle: ApplyFilter macro action
ms:assetid: c63988c4-4506-cc51-98f7-478d1f3fe668
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823130(v=office.15)
ms:contentKeyID: 48547623
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm79035
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: e79ab56778f9429e7f1a985f0f81864ae4363606
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296996"
---
# <a name="applyfilter-macro-action"></a><span data-ttu-id="88ded-102">ApplyFilter, action de macro</span><span class="sxs-lookup"><span data-stu-id="88ded-102">ApplyFilter macro action</span></span>

<span data-ttu-id="88ded-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88ded-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88ded-p101">Utilisez l'action **AppliquerFiltre** pour appliquer un filtre, une requête ou une clause SQL WHERE à une table, un formulaire ou un état de manière à restreindre ou trier les enregistrements de la table ou bien les enregistrements de la table ou de la requête sous-jacente du formulaire ou de l'état. Dans le cas d'un état, utilisez cette action uniquement dans une macro spécifiée par la propriété de type événement **SurOuverture** de cet état.</span><span class="sxs-lookup"><span data-stu-id="88ded-p101">You can use the **ApplyFilter** action to apply a filter, a query, or an SQL WHERE clause to a table, form, or report to restrict or sort the records in the table, or the records from the underlying table or query of the form or report. For reports, you can use this action only in a macro specified by the report's **OnOpen** event property.</span></span>

> [!NOTE]
> <span data-ttu-id="88ded-p102">[!REMARQUE] Vous pouvez utiliser cette action pour appliquer une clause WHERE SQL seulement lorsque vous appliquez un filtre serveur. Il n'est pas possible d'appliquer un filtre serveur à une source d'enregistrement d'une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="88ded-p102">You can use this action to apply an SQL WHERE clause only when applying a server filter. A server filter cannot be applied to a stored procedure's record source.</span></span>

## <a name="setting"></a><span data-ttu-id="88ded-108">Setting</span><span class="sxs-lookup"><span data-stu-id="88ded-108">Setting</span></span>

<span data-ttu-id="88ded-109">L’action **AppliquerFiltre** possède les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="88ded-109">The **ApplyFilter** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88ded-110">Argument d’action</span><span class="sxs-lookup"><span data-stu-id="88ded-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="88ded-111">Description</span><span class="sxs-lookup"><span data-stu-id="88ded-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88ded-112">Nom du filtre</span><span class="sxs-lookup"><span data-stu-id="88ded-112">Filter Name</span></span></p></td>
<td><p><span data-ttu-id="88ded-113">Nom d’un filtre ou d’une requête qui restreint ou trie les enregistrements de la table, du formulaire ou du rapport.</span><span class="sxs-lookup"><span data-stu-id="88ded-113">The name of a filter or query that restricts or sorts the records of the table, form, or report.</span></span> <span data-ttu-id="88ded-114">Vous pouvez entrer le nom d'une requête existante ou d'un filtre enregistré en tant que requête dans la zone <strong>nom du filtre</strong> de la section <strong>arguments</strong> de l'action du volet <strong>Générateur de macro</strong> .</span><span class="sxs-lookup"><span data-stu-id="88ded-114">You can enter the name of either an existing query or a filter that has been saved as a query in the <strong>Filter Name</strong> box in the <strong>Action Arguments</strong> section of the <strong>Macro Builder</strong> pane.</span></span></p><p><span data-ttu-id="88ded-115"><strong>Remarque</strong>: lorsque vous utilisez cette action pour appliquer un filtre serveur, l'argument Nom du filtre doit être vide.</span><span class="sxs-lookup"><span data-stu-id="88ded-115"><strong>NOTE</strong>: When you are using this action to apply a server filter, the Filter Name argument must be blank.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88ded-116">Condition Where</span><span class="sxs-lookup"><span data-stu-id="88ded-116">Where Condition</span></span></p></td>
<td><p><span data-ttu-id="88ded-117">Clause SQL WHERE (sans le mot WHERE) valide ou expression qui restreint les enregistrements de la table, du formulaire ou de l’état.</span><span class="sxs-lookup"><span data-stu-id="88ded-117">A valid SQL WHERE clause (without the word WHERE) or an expression that restricts the records of the table, form, or report.</span></span></p>
<p><span data-ttu-id="88ded-118"><b>Remarque</b>: dans une expression d'argument condition WHERE, le côté gauche de l'expression contient généralement un nom de champ de la table ou de la requête sous-jacente du formulaire ou de l'État.</span><span class="sxs-lookup"><span data-stu-id="88ded-118"><b>NOTE</b>: In a Where Condition argument expression, the left side of the expression typically contains a field name from the underlying table or query for the form or report.</span></span> <span data-ttu-id="88ded-119">La partie droite de l’expression contient généralement les critères que vous souhaitez appliquer à ce champ pour restreindre ou trier les enregistrements.</span><span class="sxs-lookup"><span data-stu-id="88ded-119">The right side of the expression typically contains the criteria you want to apply to this field to restrict or sort the records.</span></span> <span data-ttu-id="88ded-120">Ces critères peuvent ainsi être le nom d’un contrôle dans un autre formulaire qui contient la valeur à laquelle doivent correspondre les enregistrements dans le premier formulaire.</span><span class="sxs-lookup"><span data-stu-id="88ded-120">For example, the criteria can be the name of a control on another form that contains the value you want the records in the first form to match.</span></span> <span data-ttu-id="88ded-121">Le nom du contrôle doit être complet, comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="88ded-121">The name of the control should be fully qualified, for example:</span></span></p>
<p><span data-ttu-id="88ded-122"><strong>Forms</strong>! <em>FormName</em>! <em>nomcontrôle</em> Les noms de champs doivent être entourés de guillemets doubles et les littéraux de chaîne doivent être entourés de guillemets simples.</span><span class="sxs-lookup"><span data-stu-id="88ded-122"><strong>Forms</strong>!<em>formname</em>!<em>controlname</em> Field names should be surrounded by double quotation marks and string literals should be surrounded by single quotation marks.</span></span> <span data-ttu-id="88ded-123">L’argument Condition Where est limité à 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="88ded-123">The maximum length of the Where Condition argument is 255 characters.</span></span> <span data-ttu-id="88ded-124">Si vous avez besoin d’entrer une clause SQL WHERE plus longue, utilisez la méthode <strong>ApplyFilter</strong> de l’objet <strong>DoCmd</strong> dans un module Visual Basic pour Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="88ded-124">If you need to enter a longer SQL WHERE clause, use the <strong>ApplyFilter</strong> method of the <strong>DoCmd</strong> object in a Visual Basic for Applications (VBA) module.</span></span> <span data-ttu-id="88ded-125">Dans VBA, les instructions de clause SQL WHERE peuvent contenir jusqu’à 32 768 caractères.</span><span class="sxs-lookup"><span data-stu-id="88ded-125">You can enter SQL WHERE clause statements of up to 32,768 characters in VBA.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="88ded-126">[!REMARQUE] Utilisez l'argument Nom du filtre si vous avez déjà défini un filtre qui fournit les données appropriées.</span><span class="sxs-lookup"><span data-stu-id="88ded-126">You can use the Filter Name argument if you have already defined a filter that provides the appropriate data.</span></span> <span data-ttu-id="88ded-127">Utilisez l'argument ConditionWhere pour entrer directement les critères de restriction.</span><span class="sxs-lookup"><span data-stu-id="88ded-127">You can use the Where Condition argument to enter the restriction criteria directly.</span></span> <span data-ttu-id="88ded-128">Si vous utilisez les deux arguments, Microsoft Office Access 2007 applique la clause WHERE aux résultats du filtre.</span><span class="sxs-lookup"><span data-stu-id="88ded-128">If you use both arguments, Microsoft Office Access 2007 applies the WHERE clause to the results of the filter.</span></span> <span data-ttu-id="88ded-129">Vous devez utiliser au moins l’un de ces deux arguments.</span><span class="sxs-lookup"><span data-stu-id="88ded-129">You must use one or both arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ded-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="88ded-130">Remarks</span></span>

<span data-ttu-id="88ded-131">Vous pouvez appliquer un filtre ou une requête à un formulaire en mode Formulaire ou Feuille de données.</span><span class="sxs-lookup"><span data-stu-id="88ded-131">You can apply a filter or query to a form in Form view or Datasheet view.</span></span>

<span data-ttu-id="88ded-132">Le filtre et la condition WHERE que vous appliquez deviennent les paramètres de la propriété **Filtre** ou **FiltreServeur** du formulaire ou de l'état.</span><span class="sxs-lookup"><span data-stu-id="88ded-132">The filter and WHERE condition you apply become the setting of the form's or report's **Filter** or **ServerFilter** property.</span></span>

<span data-ttu-id="88ded-p107">Pour les tables et les formulaires, cette action équivaut à cliquer sur **Appliquer le filtre/tri** ou **Appliquer un filtre serveur** dans le menu **Enregistrements**. La commande de menu applique le dernier filtre créé à la table ou au formulaire, alors que l'action **AppliquerFiltre** applique un filtre ou une requête spécifique.</span><span class="sxs-lookup"><span data-stu-id="88ded-p107">For tables and forms, this action is similar to clicking **Apply Filter/Sort** or **Apply Server Filter** on the **Records** menu. The menu command applies the most recently created filter to the table or form, whereas the **ApplyFilter** action applies a specified filter or query.</span></span>

<span data-ttu-id="88ded-135">Dans une base de données Access, si vous pointez sur **Filtrer** dans le menu **Enregistrements**, puis cliquez sur **Filtre/tri avancé** après avoir exécuté l'action **AppliquerFiltre**, la fenêtre Filtre/tri avancé affiche les critères de filtre sélectionnés avec cette action.</span><span class="sxs-lookup"><span data-stu-id="88ded-135">In an Access database, if you point to **Filter** on the **Records** menu and then click **Advanced Filter/Sort** after running the **ApplyFilter** action, the Advanced Filter/Sort window shows the filter criteria you have selected with this action.</span></span>

<span data-ttu-id="88ded-p108">Pour supprimer un filtre et afficher tous les enregistrements d'une table ou d'un formulaire dans une base de données Office Access 2007, utilisez l'action **AfficherTousEnreg** ou la commande **Afficher tous les enregistrements** du menu **Enregistrements**. Pour supprimer un filtre dans un projet Access (.adp), vous pouvez revenir dans la fenêtre Filtrer par formulaire sur serveur et supprimer tous les critères de filtre, puis cliquer sur **Appliquer un filtre serveur** dans le menu **Enregistrements** de la barre d'outils ou définir la propriété **FiltreParFormulaireSurServeur** sur **Faux** (0).</span><span class="sxs-lookup"><span data-stu-id="88ded-p108">To remove a filter and display all of the records for a table or form in an Office Access 2007 database, you can use the **ShowAllRecords** action or the **Remove Filter/Sort** command on the **Records** menu. To remove a filter in an Access project (.adp), you can return to the Server Filter By Form window and remove all filter criteria and then click **Apply Server Filter** on the **Records** menu on the toolbar, or set the **ServerFilterByForm** property to **False** (0).</span></span>

<span data-ttu-id="88ded-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span><span class="sxs-lookup"><span data-stu-id="88ded-p109">When you save a table or form, Access saves any filter currently defined in that object, but won't apply the filter automatically the next time the object is opened (although it will automatically apply any sort you applied to the object before it was saved). If you want to apply a filter automatically when a form is first opened, specify a macro containing the **ApplyFilter** action or an event procedure containing the **ApplyFilter** method of the **DoCmd** object as the **OnOpen** event property setting of the form. You can also apply a filter by using the **OpenForm** or **OpenReport** action, or their corresponding methods. To apply a filter automatically when a table is first opened, you can open the table by using a macro containing the **OpenTable** action, followed immediately by the **ApplyFilter** action.</span></span>

## <a name="example"></a><span data-ttu-id="88ded-142">Exemple</span><span class="sxs-lookup"><span data-stu-id="88ded-142">Example</span></span>

<span data-ttu-id="88ded-143">L'exemple suivant montre comment utiliser l'action AppliquerFiltre pour filtrer le formulaire frmFoods à l'ouverture.</span><span class="sxs-lookup"><span data-stu-id="88ded-143">The following example shows how to use the ApplyFilter action to filter the frmFoods form as it is opened.</span></span>

<span data-ttu-id="88ded-144">**Exemple de code fourni par** [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="88ded-144">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    OpenForm
        Form Name sfrmFoods
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    ApplyFilter
        Filter Name
        Where Condition=[display_name] Link "*cheese*"
        Control Name
```



