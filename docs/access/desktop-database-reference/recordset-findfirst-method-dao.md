---
title: Méthode Recordset.FindFirst (DAO)
TOCTitle: FindFirst Method
ms:assetid: 5fcf78cd-7d2c-2e47-14e5-996f2e14ff51
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194787(v=office.15)
ms:contentKeyID: 48545170
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 489e6060fdbaa4183c006e3f422c207d9a5013ee
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998853"
---
# <a name="recordsetfindfirst-method-dao"></a><span data-ttu-id="5973e-102">Méthode Recordset.FindFirst (DAO)</span><span class="sxs-lookup"><span data-stu-id="5973e-102">Recordset.FindFirst method (DAO)</span></span>

<span data-ttu-id="5973e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5973e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5973e-104">Localise le premier enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou capture instantanée qui remplit les critères spécifiés et rend l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="5973e-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5973e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5973e-105">Syntax</span></span>

<span data-ttu-id="5973e-106">*expression* . FindFirst (***critères***)</span><span class="sxs-lookup"><span data-stu-id="5973e-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="5973e-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5973e-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="5973e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5973e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5973e-109">Name</span><span class="sxs-lookup"><span data-stu-id="5973e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="5973e-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="5973e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="5973e-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="5973e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="5973e-112">Description</span><span class="sxs-lookup"><span data-stu-id="5973e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5973e-113"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="5973e-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="5973e-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5973e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="5973e-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="5973e-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="5973e-p101">Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="5973e-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="5973e-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="5973e-118">Remarks</span></span>

<span data-ttu-id="5973e-p102">Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d'un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="5973e-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="5973e-p103">Si un enregistrement correspondant aux critères n'est pas localisé, le pointeur d'enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l'occurrence suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="5973e-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="5973e-123">Chacune des méthodes **Find** commence sa recherche à partir de l'emplacement et dans le sens spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5973e-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5973e-124">Méthode Find</span><span class="sxs-lookup"><span data-stu-id="5973e-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="5973e-125">Point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="5973e-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="5973e-126">Sens de la recherche</span><span class="sxs-lookup"><span data-stu-id="5973e-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5973e-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="5973e-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="5973e-128">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="5973e-129">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5973e-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="5973e-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="5973e-131">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="5973e-132">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5973e-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="5973e-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="5973e-134">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="5973e-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="5973e-135">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5973e-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="5973e-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="5973e-137">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="5973e-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="5973e-138">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="5973e-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5973e-p104">L'utilisation de l'une des méthodes **Find** n'équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l'enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d'une opération Move.</span><span class="sxs-lookup"><span data-stu-id="5973e-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="5973e-p105">Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l'opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l'enregistrement actif n'est pas défini. Dans ce cas, vous devez positionner le pointeur d'enregistrement actif sur un enregistrement valide.</span><span class="sxs-lookup"><span data-stu-id="5973e-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="5973e-p106">L'utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s'avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.</span><span class="sxs-lookup"><span data-stu-id="5973e-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="5973e-p107">Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l'utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5973e-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="5973e-p108">Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="5973e-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="5973e-152">Si l’argument critères se compose d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Appelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="5973e-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="5973e-153">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="5973e-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> - <span data-ttu-id="5973e-154">Pour optimiser les performances, les *critères* doivent être dans un le formulaire «*champ* = *valeur*» où *champ* représente un champ indexé dans la table de base sous-jacente, ou «*champ* LIKE *préfixe » où *le champ* est*un les champs indexés dans la table de base sous-jacente et le *préfixe* est une chaîne de recherche de préfixe (par exemple, « ART \* »).</span><span class="sxs-lookup"><span data-stu-id="5973e-154">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*" ).</span></span>
> 
> - <span data-ttu-id="5973e-p110">En règle générale, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que la méthode **Find**. Cela suppose que les objets **Recordset** de type table peuvent à eux seuls répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="5973e-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="5973e-157">Exemple</span><span class="sxs-lookup"><span data-stu-id="5973e-157">Example</span></span>

<span data-ttu-id="5973e-158">L'exemple suivant montre comment utiliser les méthodes FindFirst et FindNext pour rechercher un enregistrement dans un Recordset.</span><span class="sxs-lookup"><span data-stu-id="5973e-158">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="5973e-159">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="5973e-159">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub FindOrgName()
    
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset
        
        'Get the database and Recordset
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblCustomers")
    
        'Search for the first matching record   
        rst.FindFirst "[OrgName] LIKE '*parts*'"
        
        'Check the result
        If rst.NoMatch Then
            MsgBox "Record not found."
            GotTo Cleanup
        Else
            Do While Not rst.NoMatch
                MsgBox "Customer name: " & rst!CustName
                rst.FindNext "[OrgName] LIKE '*parts*'"
            Loop
    
            'Search for the next matching record
            rst.FindNext "[OrgName] LIKE '*parts*'"
        End If
       
        Cleanup:
            rst.Close
            Set rst = Nothing
            Set dbs = Nothing
    
    End Sub
```
