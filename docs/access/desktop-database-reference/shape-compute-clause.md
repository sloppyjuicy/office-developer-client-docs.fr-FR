---
title: Shape Compute, clause
TOCTitle: Shape Compute clause
ms:assetid: f4fee4a6-ec9e-c0b6-40e0-258f76c4696f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250245(v=office.15)
ms:contentKeyID: 48548699
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eadc448d59814f0573a959c6c1038f9c4afdbac9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711524"
---
# <a name="shape-compute-clause"></a><span data-ttu-id="05b82-102">Shape Compute, clause</span><span class="sxs-lookup"><span data-stu-id="05b82-102">Shape Compute clause</span></span>

<span data-ttu-id="05b82-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05b82-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05b82-104">Une clause COMPUTE de commande SHAPE génère un objet **Recordset** parent dont les colonnes se composent d'une référence à l'objet **Recordset** enfant, de colonnes facultatives contenant des colonnes de chapitre, des nouvelles colonnes ou des colonnes calculées ou encore le résultat de l'exécution de fonctions d'agrégation sur l'objet **Recordset** enfant ou un objet **Recordset** précédemment mis en forme et de toutes colonnes provenant de l'objet **Recordset** enfant répertoriées dans la clause BY facultative.</span><span class="sxs-lookup"><span data-stu-id="05b82-104">A shape COMPUTE clause generates a parent **Recordset**, whose columns consist of a reference to the child **Recordset**; optional columns whose contents are chapter, new, or calculated columns, or the result of executing aggregate functions on the child **Recordset** or a previously shaped **Recordset**; and any columns from the child **Recordset** listed in the optional BY clause.</span></span>

## <a name="syntax"></a><span data-ttu-id="05b82-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05b82-105">Syntax</span></span>

```vb 
 
SHAPE child-command [AS] child-alias 
   COMPUTE child-alias [[AS] name], [appended-column-list] 
   [BY grp-field-list] 
```

## <a name="description"></a><span data-ttu-id="05b82-106">Description</span><span class="sxs-lookup"><span data-stu-id="05b82-106">Description</span></span>

<span data-ttu-id="05b82-107">Cette clause comporte les parties suivantes :</span><span class="sxs-lookup"><span data-stu-id="05b82-107">The parts of this clause are as follows:</span></span>

- <span data-ttu-id="05b82-108">*child-command*</span><span class="sxs-lookup"><span data-stu-id="05b82-108">*child-command*</span></span>

  - <span data-ttu-id="05b82-109">Est constituée de l'un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="05b82-109">Consists of one of the following:</span></span>
    
    - <span data-ttu-id="05b82-p101">Commande de requête entre accolades (« {} ») qui retourne un objet **Recordset** enfant. La commande est transmise au fournisseur de données sous-jacent et sa syntaxe dépend des exigences du fournisseur. Elle est en général écrite en langage SQL, même si ADO n'exige pas de langage de requête particulier.</span><span class="sxs-lookup"><span data-stu-id="05b82-p101">A query command within curly braces ("{}") that returns a child **Recordset** object. The command is issued to the underlying data provider, and its syntax depends on the requirements of that provider. This will typically be the SQL language, although ADO does not require any particular query language.</span></span>
    
    - <span data-ttu-id="05b82-113">Nom d'un objet **Recordset** mis en forme existant.</span><span class="sxs-lookup"><span data-stu-id="05b82-113">The name of an existing shaped **Recordset**.</span></span>
    
    - <span data-ttu-id="05b82-114">Autre commande SHAPE.</span><span class="sxs-lookup"><span data-stu-id="05b82-114">Another shape command.</span></span>
    
    - <span data-ttu-id="05b82-115">Mot-clé TABLE, suivi du nom d'une table du fournisseur de données.</span><span class="sxs-lookup"><span data-stu-id="05b82-115">The TABLE keyword, followed by the name of a table in the data provider.</span></span>

- <span data-ttu-id="05b82-116">*child-alias*</span><span class="sxs-lookup"><span data-stu-id="05b82-116">*child-alias*</span></span>

  - <span data-ttu-id="05b82-117">Alias utilisé pour faire référence à l' **objet Recordset** renvoyé par la *commande child-command.*</span><span class="sxs-lookup"><span data-stu-id="05b82-117">An alias used to refer to the **Recordset** returned by the *child-command.*</span></span> <span data-ttu-id="05b82-118">L' *alias-enfant* est requise dans la liste des colonnes dans la clause COMPUTE et définit la relation entre les objets **Recordset** parent et enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-118">The *child-alias* is required in the list of columns in the COMPUTE clause and defines the relation between the parent and child **Recordset** objects.</span></span>

- <span data-ttu-id="05b82-119">*appended-column-list*</span><span class="sxs-lookup"><span data-stu-id="05b82-119">*appended-column-list*</span></span>

  - <span data-ttu-id="05b82-p103">Liste dans laquelle chaque élément définit une colonne dans le parent généré. Chaque élément contient une colonne de chapitre, une nouvelle colonne, une colonne calculée ou une valeur résultant d'une fonction d'agrégation exécutée sur l'objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-p103">A list in which each element defines a column in the generated parent. Each element contains either a chapter column, a new column, a calculated column, or a value resulting from an aggregate function on the child **Recordset**.</span></span>

- <span data-ttu-id="05b82-122">*grp-field-list*</span><span class="sxs-lookup"><span data-stu-id="05b82-122">*grp-field-list*</span></span>

  - <span data-ttu-id="05b82-123">Une liste de colonnes dans les objets **Recordset** parent et enfant qui spécifie la façon dont les lignes doivent être regroupés dans l’enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-123">A list of columns in the parent and child **Recordset** objects that specifies how rows should be grouped in the child.</span></span> <span data-ttu-id="05b82-124">Pour chaque colonne dans le *groupe champ liste,* il existe une colonne correspondante dans les objets **Recordset** parent et enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-124">For each column in the *grp-field-list,* there is a corresponding column in the child and parent **Recordset** objects.</span></span> <span data-ttu-id="05b82-125">Ont des valeurs uniques pour chaque ligne dans **l’objet Recordset**parent, les colonnes de la *liste de champs de groupe* et l’enfant **Recordset** référencé par la ligne parente se compose uniquement d’enfants dont la *liste de champs de groupe* de lignes colonnes ont la même valeur que la ligne parente.</span><span class="sxs-lookup"><span data-stu-id="05b82-125">For each row in the parent **Recordset**, the *grp-field-list* columns have unique values, and the child **Recordset** referenced by the parent row consists solely of child rows whose *grp-field-list* columns have the same values as the parent row.</span></span>

<span data-ttu-id="05b82-p105">Si la clause BY est incluse, les lignes de l'objet **Recordset** enfant sont groupées en fonction des colonnes dans la clause COMPUTE. L'objet **Recordset** parent contiendra une ligne pour chaque groupe de lignes de l'objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-p105">If the BY clause is included, the child **Recordset**'s rows will be grouped based on the columns in the COMPUTE clause. The parent **Recordset** will contain one row for each group of rows in the child **Recordset**.</span></span>

<span data-ttu-id="05b82-p106">En revanche, si la clause BY est omise, l'intégralité de l'objet **Recordset** enfant est traité comme un seul groupe et l'objet **Recordset** parent contient exactement une ligne. Cette ligne référence tout l'objet **Recordset** enfant. L'omission de la clause BY vous permet de calculer des agrégats de « totaux » pour tout l'objet **Recordset** enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-p106">If the BY clause is omitted, the entire child **Recordset** is treated as a single group and the parent **Recordset** will contain exactly one row. That row will reference the entire child **Recordset**. Omitting the BY clause allows you to compute "grand total" aggregates over the entire child **Recordset**.</span></span>

<span data-ttu-id="05b82-131">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="05b82-131">For example:</span></span>

```vb
    SHAPE {select * from Orders} AS orders
       COMPUTE orders, SUM(orders.OrderAmount) as TotalSales
```

<span data-ttu-id="05b82-p107">Quelle que soit la façon dont l'objet **Recordset** parent est formé (à l'aide de la clause COMPUTE ou APPEND), celui-ci contiendra une colonne de chapitre utilisée pour établir une relation avec un objet **Recordset** enfant. Si vous le souhaitez, l'objet **Recordset** parent peut également contenir des colonnes comportant des agrégats (SUM, MIN, MAX, etc.) sur les lignes enfants. Les objets **Recordset** parent et enfant peuvent tous deux contenir des colonnes comportant une expression sur la ligne dans l'objet **Recordset** ainsi que des nouvelles colonnes, initialement vides.</span><span class="sxs-lookup"><span data-stu-id="05b82-p107">Regardless of which way the parent **Recordset** is formed (using COMPUTE or using APPEND), it will contain a chapter column that is used to relate it to a child **Recordset**. If you wish, the parent **Recordset** may also contain columns that contain aggregates (SUM, MIN, MAX, and so on) over the child rows. Both the parent and the child **Recordset** may contain columns that contain an expression on the row in the **Recordset**, as well as columns that are new and initially empty.</span></span>

## <a name="operation"></a><span data-ttu-id="05b82-135">Déroulement de l'opération</span><span class="sxs-lookup"><span data-stu-id="05b82-135">Operation</span></span>

<span data-ttu-id="05b82-136">La *commande child-command* est transmise au fournisseur, qui renvoie un **objet Recordset**enfant.</span><span class="sxs-lookup"><span data-stu-id="05b82-136">The *child-command* is issued to the provider, which returns a child **Recordset**.</span></span>

<span data-ttu-id="05b82-p108">La clause COMPUTE spécifie les colonnes de l'objet **Recordset** parent, par exemple une référence à l'objet **Recordset** enfant, un ou plusieurs agrégats, une expression calculée ou de nouvelles colonnes. Si une clause BY est employée, les colonnes qu'elle définit sont également ajoutées à l'objet **Recordset** parent. La clause BY spécifie la façon dont les lignes d'un objet **Recordset** enfant sont groupées.</span><span class="sxs-lookup"><span data-stu-id="05b82-p108">The COMPUTE clause specifies the columns of the parent **Recordset**, which may be a reference to the child **Recordset**, one or more aggregates, a calculated expression, or new columns. If there is a BY clause, the columns it defines are also appended to the parent **Recordset**. The BY clause specifies how the rows of the child **Recordset** are grouped.</span></span>

<span data-ttu-id="05b82-140">Par exemple, supposons que nous disposons d'une table, Demographics, comportant les champs State, City et Population (les chiffres ne sont donnés qu'à titre d'exemple).</span><span class="sxs-lookup"><span data-stu-id="05b82-140">For example, assume you have a table — Demographics — consisting of State, City, and Population fields (the population figures are solely for illustration).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b82-141">State</span><span class="sxs-lookup"><span data-stu-id="05b82-141">State</span></span></p></th>
<th><p><span data-ttu-id="05b82-142">City</span><span class="sxs-lookup"><span data-stu-id="05b82-142">City</span></span></p></th>
<th><p><span data-ttu-id="05b82-143">Population</span><span class="sxs-lookup"><span data-stu-id="05b82-143">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b82-144">WA</span><span class="sxs-lookup"><span data-stu-id="05b82-144">WA</span></span></p></td>
<td><p><span data-ttu-id="05b82-145">Seattle</span><span class="sxs-lookup"><span data-stu-id="05b82-145">Seattle</span></span></p></td>
<td><p><span data-ttu-id="05b82-146">700 000</span><span class="sxs-lookup"><span data-stu-id="05b82-146">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-147">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-147">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-148">Medford</span><span class="sxs-lookup"><span data-stu-id="05b82-148">Medford</span></span></p></td>
<td><p><span data-ttu-id="05b82-149">200 000</span><span class="sxs-lookup"><span data-stu-id="05b82-149">200,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b82-150">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-150">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-151">Portland</span><span class="sxs-lookup"><span data-stu-id="05b82-151">Portland</span></span></p></td>
<td><p><span data-ttu-id="05b82-152">400 000</span><span class="sxs-lookup"><span data-stu-id="05b82-152">400,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-153">CA</span><span class="sxs-lookup"><span data-stu-id="05b82-153">CA</span></span></p></td>
<td><p><span data-ttu-id="05b82-154">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="05b82-154">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="05b82-155">800 000</span><span class="sxs-lookup"><span data-stu-id="05b82-155">800,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b82-156">CA</span><span class="sxs-lookup"><span data-stu-id="05b82-156">CA</span></span></p></td>
<td><p><span data-ttu-id="05b82-157">San Diego</span><span class="sxs-lookup"><span data-stu-id="05b82-157">San Diego</span></span></p></td>
<td><p><span data-ttu-id="05b82-158">600 000</span><span class="sxs-lookup"><span data-stu-id="05b82-158">600,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-159">WA</span><span class="sxs-lookup"><span data-stu-id="05b82-159">WA</span></span></p></td>
<td><p><span data-ttu-id="05b82-160">Tacoma</span><span class="sxs-lookup"><span data-stu-id="05b82-160">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="05b82-161">500 000</span><span class="sxs-lookup"><span data-stu-id="05b82-161">500,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b82-162">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-162">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-163">Corvallis</span><span class="sxs-lookup"><span data-stu-id="05b82-163">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="05b82-164">300 000</span><span class="sxs-lookup"><span data-stu-id="05b82-164">300,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05b82-165">Émettez à présent cette commande SHAPE :</span><span class="sxs-lookup"><span data-stu-id="05b82-165">Now, issue this shape command:</span></span>

```vb 
 
rst.Open  "SHAPE {select * from demographics} AS rs "  & _ 
          "COMPUTE rs, SUM(rs.population) BY state", _ 
           objConnection 
```

<span data-ttu-id="05b82-166">Cette commande ouvre un objet **Recordset** mis en forme comportant deux niveaux.</span><span class="sxs-lookup"><span data-stu-id="05b82-166">This command opens a shaped **Recordset** with two levels.</span></span> <span data-ttu-id="05b82-167">Le niveau parent est un **jeu d’enregistrements** de généré avec une colonne agrégée (SUM(rs.population)), une colonne référençant l' **objet Recordset** (rs) enfant et une colonne permettant de grouper l’enfant du **jeu d’enregistrements** (état).</span><span class="sxs-lookup"><span data-stu-id="05b82-167">The parent level is a generated **Recordset** with an aggregate column (SUM(rs.population) ), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="05b82-168">Le niveau enfant est le **jeu d’enregistrements** renvoyé par la commande de requête (), une colonne référençant l' **objet Recordset** (rs) enfant et une colonne permettant de grouper l’enfant du **jeu d’enregistrements** (état).</span><span class="sxs-lookup"><span data-stu-id="05b82-168">The child level is the **Recordset** returned by the query command (), a column referencing the child **Recordset** (rs ), and a column for grouping the child **Recordset** (state ).</span></span> <span data-ttu-id="05b82-169">Le niveau enfant est l' **objet Recordset** renvoyé par la commande de requête (sélectionnez \* à partir de données démographiques).</span><span class="sxs-lookup"><span data-stu-id="05b82-169">The child level is the **Recordset** returned by the query command (select \* from demographics ).</span></span>

<span data-ttu-id="05b82-p110">Les lignes de détail de l'objet **Recordset** sont groupées en fonction de la colonne State, mais dans aucun ordre particulier. En d'autres termes, les groupes ne sont pas classés par ordre alphabétique ou numérique. Si vous voulez trier l'objet **Recordset** parent, utilisez la méthode **Sort** **Recordset** pour trier l'objet **Recordset** parent.</span><span class="sxs-lookup"><span data-stu-id="05b82-p110">The child **Recordset** detail rows will be grouped by state, but otherwise in no particular order. That is, the groups will not be in alphabetical or numerical order. If you want the parent **Recordset** to be ordered, you can use the **Recordset** **Sort** method to order the parent **Recordset**.</span></span>

<span data-ttu-id="05b82-p111">Vous pouvez désormais parcourir l'objet **Recordset** parent et accéder aux objets **Recordset** de détail enfants. Pour plus d'informations, consultez [Accès aux lignes d'un jeu d'enregistrements hiérarchique](accessing-rows-in-a-hierarchical-recordset.md).</span><span class="sxs-lookup"><span data-stu-id="05b82-p111">You can now navigate the opened parent **Recordset** and access the child detail **Recordset** objects. For more information, see [Accessing Rows in a Hierarchical Recordset](accessing-rows-in-a-hierarchical-recordset.md).</span></span>

<span data-ttu-id="05b82-175">**Objets Recordset parent et enfants résultants**</span><span class="sxs-lookup"><span data-stu-id="05b82-175">**Resultant Parent and Child Detail Recordsets**</span></span>

<span data-ttu-id="05b82-176">**Parent**</span><span class="sxs-lookup"><span data-stu-id="05b82-176">**Parent**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b82-177">SUM (rs.Population)</span><span class="sxs-lookup"><span data-stu-id="05b82-177">SUM (rs.Population)</span></span></p></th>
<th><p><span data-ttu-id="05b82-178">rs</span><span class="sxs-lookup"><span data-stu-id="05b82-178">rs</span></span></p></th>
<th><p><span data-ttu-id="05b82-179">State</span><span class="sxs-lookup"><span data-stu-id="05b82-179">State</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b82-180">1,300,000</span><span class="sxs-lookup"><span data-stu-id="05b82-180">1,300,000</span></span></p></td>
<td><p><span data-ttu-id="05b82-181">Référence à Enfant 1</span><span class="sxs-lookup"><span data-stu-id="05b82-181">Reference to child1</span></span></p></td>
<td><p><span data-ttu-id="05b82-182">CA</span><span class="sxs-lookup"><span data-stu-id="05b82-182">CA</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-183">1,200,000</span><span class="sxs-lookup"><span data-stu-id="05b82-183">1,200,000</span></span></p></td>
<td><p><span data-ttu-id="05b82-184">Référence à Enfant 2</span><span class="sxs-lookup"><span data-stu-id="05b82-184">Reference to child2</span></span></p></td>
<td><p><span data-ttu-id="05b82-185">WA</span><span class="sxs-lookup"><span data-stu-id="05b82-185">WA</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b82-186">1,100,000</span><span class="sxs-lookup"><span data-stu-id="05b82-186">1,100,000</span></span></p></td>
<td><p><span data-ttu-id="05b82-187">Référence à Enfant 3</span><span class="sxs-lookup"><span data-stu-id="05b82-187">Reference to child3</span></span></p></td>
<td><p><span data-ttu-id="05b82-188">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-188">OR</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05b82-189">**Enfant 1**</span><span class="sxs-lookup"><span data-stu-id="05b82-189">**Child1**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b82-190">State</span><span class="sxs-lookup"><span data-stu-id="05b82-190">State</span></span></p></th>
<th><p><span data-ttu-id="05b82-191">City</span><span class="sxs-lookup"><span data-stu-id="05b82-191">City</span></span></p></th>
<th><p><span data-ttu-id="05b82-192">Population</span><span class="sxs-lookup"><span data-stu-id="05b82-192">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b82-193">CA</span><span class="sxs-lookup"><span data-stu-id="05b82-193">CA</span></span></p></td>
<td><p><span data-ttu-id="05b82-194">Los Angeles</span><span class="sxs-lookup"><span data-stu-id="05b82-194">Los Angeles</span></span></p></td>
<td><p><span data-ttu-id="05b82-195">800 000</span><span class="sxs-lookup"><span data-stu-id="05b82-195">800,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-196">CA</span><span class="sxs-lookup"><span data-stu-id="05b82-196">CA</span></span></p></td>
<td><p><span data-ttu-id="05b82-197">San Diego</span><span class="sxs-lookup"><span data-stu-id="05b82-197">San Diego</span></span></p></td>
<td><p><span data-ttu-id="05b82-198">600 000</span><span class="sxs-lookup"><span data-stu-id="05b82-198">600,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05b82-199">**Enfant 2**</span><span class="sxs-lookup"><span data-stu-id="05b82-199">**Child2**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b82-200">State</span><span class="sxs-lookup"><span data-stu-id="05b82-200">State</span></span></p></th>
<th><p><span data-ttu-id="05b82-201">City</span><span class="sxs-lookup"><span data-stu-id="05b82-201">City</span></span></p></th>
<th><p><span data-ttu-id="05b82-202">Population</span><span class="sxs-lookup"><span data-stu-id="05b82-202">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b82-203">WA</span><span class="sxs-lookup"><span data-stu-id="05b82-203">WA</span></span></p></td>
<td><p><span data-ttu-id="05b82-204">Seattle</span><span class="sxs-lookup"><span data-stu-id="05b82-204">Seattle</span></span></p></td>
<td><p><span data-ttu-id="05b82-205">700 000</span><span class="sxs-lookup"><span data-stu-id="05b82-205">700,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-206">WA</span><span class="sxs-lookup"><span data-stu-id="05b82-206">WA</span></span></p></td>
<td><p><span data-ttu-id="05b82-207">Tacoma</span><span class="sxs-lookup"><span data-stu-id="05b82-207">Tacoma</span></span></p></td>
<td><p><span data-ttu-id="05b82-208">500 000</span><span class="sxs-lookup"><span data-stu-id="05b82-208">500,000</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05b82-209">**Enfant 3**</span><span class="sxs-lookup"><span data-stu-id="05b82-209">**Child3**</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05b82-210">State</span><span class="sxs-lookup"><span data-stu-id="05b82-210">State</span></span></p></th>
<th><p><span data-ttu-id="05b82-211">City</span><span class="sxs-lookup"><span data-stu-id="05b82-211">City</span></span></p></th>
<th><p><span data-ttu-id="05b82-212">Population</span><span class="sxs-lookup"><span data-stu-id="05b82-212">Population</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05b82-213">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-213">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-214">Medford</span><span class="sxs-lookup"><span data-stu-id="05b82-214">Medford</span></span></p></td>
<td><p><span data-ttu-id="05b82-215">200 000</span><span class="sxs-lookup"><span data-stu-id="05b82-215">200,000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05b82-216">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-216">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-217">Portland</span><span class="sxs-lookup"><span data-stu-id="05b82-217">Portland</span></span></p></td>
<td><p><span data-ttu-id="05b82-218">400 000</span><span class="sxs-lookup"><span data-stu-id="05b82-218">400,000</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05b82-219">OR</span><span class="sxs-lookup"><span data-stu-id="05b82-219">OR</span></span></p></td>
<td><p><span data-ttu-id="05b82-220">Corvallis</span><span class="sxs-lookup"><span data-stu-id="05b82-220">Corvallis</span></span></p></td>
<td><p><span data-ttu-id="05b82-221">300 000</span><span class="sxs-lookup"><span data-stu-id="05b82-221">300,000</span></span></p></td>
</tr>
</tbody>
</table>

