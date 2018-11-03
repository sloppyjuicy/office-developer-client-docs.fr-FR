---
title: Filter, propriété (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d067d26120e694975c662c3d018443e325e75119
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937133"
---
# <a name="filter-property-ado"></a><span data-ttu-id="51268-102">Filter, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="51268-102">Filter property (ADO)</span></span>


<span data-ttu-id="51268-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51268-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51268-104">Indique le filtre utilisé pour les données d'un [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="51268-104">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="51268-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="51268-105">Settings and return values</span></span>

<span data-ttu-id="51268-106">Définit ou renvoie une valeur **Variant** qui peut l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="51268-106">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="51268-107">**Chaîne de critères**: chaîne constituée d'une ou plusieurs clauses individuelles concaténées avec les opérateurs **AND** ou **OR**.</span><span class="sxs-lookup"><span data-stu-id="51268-107">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="51268-108">**Tableau de signets**: tableau de valeurs de signets uniques pointant vers des enregistrements de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="51268-108">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="51268-109">Valeur [FilterGroupEnum](filtergroupenum.md).</span><span class="sxs-lookup"><span data-stu-id="51268-109">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="51268-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="51268-110">Remarks</span></span>

<span data-ttu-id="51268-p101">Utilisez la propriété **Filter** pour filtrer les enregistrements d'un objet **Recordset**. Le **Recordset** filtré devient le curseur actuel. Les autres propriétés qui renvoient des valeurs dépendant du curseur actuel sont affectées (par exemple [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [CpteEnregistrement](recordcount-property-ado.md) et [ComptePage](pagecount-property-ado.md)). Cela est dû au fait que l'attribution d'une valeur spécifique à la propriété **Filter** déplace l'enregistrement actuel et le définit comme le premier enregistrement satisfaisant la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="51268-p101">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor. Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md). This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="51268-115">La chaîne de critères est composée de clauses de *Type NomChamp-Opérateur-valeur* type (par exemple, « LastName = 'Martin' »).</span><span class="sxs-lookup"><span data-stu-id="51268-115">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="51268-116">Vous pouvez créer des clauses composées en concaténant des clauses avec **AND** (par exemple, « LastName = 'Martin' AND FirstName = 'John' ») ou **OR** (par exemple, »).</span><span class="sxs-lookup"><span data-stu-id="51268-116">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="51268-117">Vous pouvez créer des clauses composées en concaténant des clauses avec **AND** (par exemple, « LastName = 'Martin' AND FirstName = 'John' ») ou **ou** (par exemple, « LastName = 'Martin' OR LastName = 'Jones' »).</span><span class="sxs-lookup"><span data-stu-id="51268-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="51268-118">Lorsque vous utilisez des chaînes de critères, gardez les points suivants à l'esprit :</span><span class="sxs-lookup"><span data-stu-id="51268-118">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="51268-119">*FieldName* doit être un nom de champ valide du **jeu d’enregistrements**.</span><span class="sxs-lookup"><span data-stu-id="51268-119">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="51268-120">Si le nom de champ contient des espaces, vous devez le mettre entre crochets.</span><span class="sxs-lookup"><span data-stu-id="51268-120">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="51268-121">*Opérateur* doit être une des opérations suivantes : \<, \>, \<= \>=, \< \>, = ou **LIKE**.</span><span class="sxs-lookup"><span data-stu-id="51268-121">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="51268-122">*Valeur* est la valeur à laquelle vous comparez les valeurs de champ (par exemple, « Smith », \#24/8/95\#, 12.345 ou $50.00).</span><span class="sxs-lookup"><span data-stu-id="51268-122">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="51268-123">Utilisez des guillemets simples avec les chaînes et les signes dièse (\#) avec des dates.</span><span class="sxs-lookup"><span data-stu-id="51268-123">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="51268-124">Pour les nombres, vous pouvez utiliser les points décimaux, le signe dollar et les notations scientifiques.</span><span class="sxs-lookup"><span data-stu-id="51268-124">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="51268-125">Si *l’opérateur* est **semblable**, *valeur* peut utiliser des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="51268-125">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="51268-126">Uniquement l’astérisque (\*) et le signe de pourcentage (%) les caractères génériques sont autorisés, et ils doivent être le dernier caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="51268-126">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="51268-127">*Valeur* ne peut pas être null.</span><span class="sxs-lookup"><span data-stu-id="51268-127">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="51268-p105">[!REMARQUE] Pour insérer des guillemets simples (') dans la valeur Value du filtre, utilisez deux guillemets simples pour en représenter un. Par exemple, pour créer un filtre O'Malley, la chaîne de critères doit être « col1 = 'O''Malley' ». Pour insérer des guillemets simples au début et à la fin de la valeur du filtre, placez un signe dièse (#) devant et derrière la chaîne. Par exemple, pour filtrer la valeur '1', la chaîne de critères doit apparaître ainsi « col1 = #'1'# ».</span><span class="sxs-lookup"><span data-stu-id="51268-p105">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one. For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'". To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#). For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span>



  - <span data-ttu-id="51268-p106">Il n'y a aucune priorité entre **AND** et **OR**. Les clauses peuvent être regroupées entre parenthèses. Vous ne pouvez toutefois pas regrouper les clauses liées par un **OR** puis joindre le groupe à une autre clause avec un **AND**:</span><span class="sxs-lookup"><span data-stu-id="51268-p106">There is no precedence between **AND** and **OR**. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="51268-135">Construisez plutôt ce filtre de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="51268-135">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="51268-136">Dans une clause **LIKE** , vous pouvez utiliser un caractère générique au début et fin de la chaîne (par exemple, LastName Like '\*mit\*»), ou uniquement à la fin de la chaîne (par exemple LastName Like ' Smit\*»).</span><span class="sxs-lookup"><span data-stu-id="51268-136">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="51268-137">Les constantes de filtre facilitent la résolution des conflits d'enregistrement ponctuels lors des mises à jour par lot en vous permettant d'afficher, par exemple, uniquement les enregistrements concernés par le dernier appel de la méthode [UpdateBatch](updatebatch-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="51268-137">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="51268-p107">La définition de la propriété **Filter** à proprement parler peut échouer en raison d'un conflit avec les données sous-jacentes (par exemple si l'enregistrement a déjà été supprimé par un autre utilisateur). Dans ce cas, le fournisseur renvoie des avertissements vers la collection [Errors](errors-collection-ado.md), mais n'arrête pas d'exécution de programme. Une erreur d'exécution n'est générée que s'il existe des conflits sur tous les enregistrements demandés. Utilisez la propriété [Status](status-property-ado-recordset.md) pour localiser les enregistrements générant des conflits.</span><span class="sxs-lookup"><span data-stu-id="51268-p107">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user). In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="51268-142">L'attribution d'une chaîne vide à la propriété **Filter** ("") a le même effet que l'utilisation de la constante **adFilterNone**.</span><span class="sxs-lookup"><span data-stu-id="51268-142">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="51268-p108">Lorsque la propriété **Filter** est définie, la position de l'enregistrement actuel se déplace vers le premier enregistrement du sous-ensemble d'enregistrements filtré du **Recordset**. De même, quand la propriété **Filter** est effacée, la position d'enregistrement actuel passe au premier enregistrement du **Recorset**.</span><span class="sxs-lookup"><span data-stu-id="51268-p108">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**. Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="51268-145">Pour plus d'explications sur les valeurs de signets à partir desquelles vous pourrez construire un tableau utilisable avec la propriété [Filter](bookmark-property-ado.md), voir la propriété **Bookmark**.</span><span class="sxs-lookup"><span data-stu-id="51268-145">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="51268-146">Seuls les **filtres** sous la forme de chaînes de critères (P.ex \> ' 12/31/1999 ') affectent le contenu du **jeu d’enregistrements**persistant.</span><span class="sxs-lookup"><span data-stu-id="51268-146">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="51268-147">Les **filtres** créés avec un tableau de **signets** ou en utilisant une valeur provenant de **FilterGroupEnum** ne modifient pas le contenu du jeu d'enregistrements persistant.</span><span class="sxs-lookup"><span data-stu-id="51268-147">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="51268-148">Ces règles s'appliquent aux **jeux d'enregistrements** créés avec des curseurs côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="51268-148">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

> [!NOTE]
> <span data-ttu-id="51268-p110">[!REMARQUE] Lorsque vous appliquez l'indicateur **adFilterPendingRecords** à un **jeu d'enregistrements** filtré et modifié lors d'une mise à jour par lot, le **jeu d'enregistrements** résultant est vide si le filtrage portait sur le champ clé d'une table à clé unique et si la modification a été apportée sur les valeurs de ce champ clé. Le **jeu d'enregistrements** résultant n'est pas vide si l'une des affirmations suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="51268-p110">When you apply the **adFilterPendingRecords** flag to a filtered and modified **Recordset** in the batch update mode, the resultant **Recordset** is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values. The resultant **Recordset** will be non-empty if one of the following is true:</span></span>
> - <span data-ttu-id="51268-151">Le filtrage portait sur des champs non-clé d'une table à clé unique.</span><span class="sxs-lookup"><span data-stu-id="51268-151">The filtering was based on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="51268-152">Le filtrage portait sur l'un des champs d'une table à clés multiples.</span><span class="sxs-lookup"><span data-stu-id="51268-152">The filtering was based on any fields in a multiple-keyed table.</span></span>
> - <span data-ttu-id="51268-153">Les modifications ont été apportées sur des champs non-clés d'une table à clé unique.</span><span class="sxs-lookup"><span data-stu-id="51268-153">Modifications were made on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="51268-154">Les modifications ont été apportées sur l'un des champs d'une table à clés multiples.</span><span class="sxs-lookup"><span data-stu-id="51268-154">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="51268-p111">Le tableau suivant résume les effets d' **adFilterPendingRecords** dans différentes combinaisons de filtrage et de modifications. La colonne de gauche indique les modifications possibles ; les modifications peuvent être apportées sur tous les champs non-clés, sur le champ clé d'une table à clé unique ou l'un des champs clé d'une table à clés multiples. La ligne supérieure indique le critère de filtrage ; le filtrage peut porter sur l'un des champs non-clés, sur le champ clé d'une table à clé unique ou sur n'importe lequel des champs clé d'une table à clés multiples. Les cellules qui se recoupent présentent les résultats : + signifie que l'application de **adFilterPendingRecords** donne un **Recordset** non vide ; **-** indique un **Recordset** vide.</span><span class="sxs-lookup"><span data-stu-id="51268-p111">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications. The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table. The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table. The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="51268-159">Non-clés</span><span class="sxs-lookup"><span data-stu-id="51268-159">Non keys</span></span></p></th>
<th><p><span data-ttu-id="51268-160">Clé unique</span><span class="sxs-lookup"><span data-stu-id="51268-160">Single Key</span></span></p></th>
<th><p><span data-ttu-id="51268-161">Clés multiples</span><span class="sxs-lookup"><span data-stu-id="51268-161">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51268-162">Non-clés</span><span class="sxs-lookup"><span data-stu-id="51268-162">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51268-163">Clé unique</span><span class="sxs-lookup"><span data-stu-id="51268-163">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="51268-164">S/O</span><span class="sxs-lookup"><span data-stu-id="51268-164">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51268-165">Clés multiples</span><span class="sxs-lookup"><span data-stu-id="51268-165">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="51268-166">S/O</span><span class="sxs-lookup"><span data-stu-id="51268-166">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

