---
title: Recordset.FindNext Method (DAO)
TOCTitle: FindNext Method
ms:assetid: 5457dfc8-e561-5624-74d0-34278ba2e7cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194099(v=office.15)
ms:contentKeyID: 48544893
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d9e4651b2fb5fa9f0ef8569b9f4b28d4c031e87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885296"
---
# <a name="recordsetfindnext-method-dao"></a><span data-ttu-id="a5d2b-102">Recordset.FindNext Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-102">Recordset.FindNext Method (DAO)</span></span>

<span data-ttu-id="a5d2b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5d2b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5d2b-104">Recherche l’enregistrement suivant dans un objet **[Recordset](recordset-object-dao.md)** de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés et en fait l’enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a5d2b-104">Locates the next record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a5d2b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a5d2b-105">Syntax</span></span>

<span data-ttu-id="a5d2b-106">*expression* . FindNext (***critères***)</span><span class="sxs-lookup"><span data-stu-id="a5d2b-106">*expression* .FindNext(***Criteria***)</span></span>

<span data-ttu-id="a5d2b-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a5d2b-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a5d2b-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a5d2b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5d2b-109">Name</span><span class="sxs-lookup"><span data-stu-id="a5d2b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a5d2b-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="a5d2b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a5d2b-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a5d2b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a5d2b-112">Description</span><span class="sxs-lookup"><span data-stu-id="a5d2b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5d2b-113">Critères</span><span class="sxs-lookup"><span data-stu-id="a5d2b-113">Criteria</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a5d2b-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="a5d2b-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a5d2b-p101">Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a5d2b-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a5d2b-118">Remarks</span></span>

<span data-ttu-id="a5d2b-p102">Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d'un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="a5d2b-p103">Si un enregistrement correspondant aux critères n'est pas localisé, le pointeur d'enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l'occurrence suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="a5d2b-123">Chacune des méthodes **Find** commence sa recherche à partir de l'emplacement et dans le sens spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a5d2b-124">Méthode Find</span><span class="sxs-lookup"><span data-stu-id="a5d2b-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="a5d2b-125">Point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="a5d2b-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="a5d2b-126">Sens de la recherche</span><span class="sxs-lookup"><span data-stu-id="a5d2b-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a5d2b-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="a5d2b-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="a5d2b-128">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-129">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5d2b-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="a5d2b-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="a5d2b-131">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-132">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a5d2b-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="a5d2b-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="a5d2b-134">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="a5d2b-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-135">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a5d2b-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="a5d2b-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="a5d2b-137">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="a5d2b-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="a5d2b-138">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a5d2b-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a5d2b-p104">L'utilisation de l'une des méthodes **Find** n'équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l'enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d'une opération Move.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="a5d2b-p105">Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l'opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l'enregistrement actif n'est pas défini. Dans ce cas, vous devez positionner le pointeur d'enregistrement actif sur un enregistrement valide.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="a5d2b-p106">L'utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s'avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="a5d2b-147">Dans un espace de travail ODBCDirect, les méthodes **Find** et **Seek** ne sont disponibles pour aucun objet **Recordset**, quel qu'en soit le type, car l'exécution d'une méthode **Find** ou **Seek** via une connexion ODBC n'est pas très efficace sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-147">In an ODBCDirect workspace, the **Find** and **Seek** methods are not available on any type of **Recordset** object, because executing a **Find** or **Seek** through an ODBC connection is not very efficient over the network.</span></span> <span data-ttu-id="a5d2b-148">Au lieu de cela, vous devez concevoir la requête (c'est-à-dire, en utilisant l’argument source de la méthode **OpenRecordset** ) avec une clause WHERE appropriée qui limite les enregistrements renvoyés à ceux qui répondent aux critères vous utiliseriez autrement dans une **recherche** ou Méthode **Seek** .</span><span class="sxs-lookup"><span data-stu-id="a5d2b-148">Instead, you should design the query (that is, using the source argument to the **OpenRecordset** method) with an appropriate WHERE clause that restricts the returned records to only those that meet the criteria you would otherwise use in a **Find** or **Seek** method.</span></span>

<span data-ttu-id="a5d2b-p108">Lorsque vous travaillez avec des bases de données ODBC connectées au moteur de base de données Microsoft Access et des objets de type feuille de réponse dynamique volumineux, il est possible que vous notiez une certaine lenteur d'exécution lorsque vous utilisez la méthode **Find** ou la propriété **Sort** ou **Filter**. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses personnalisées ORDER BY ou WHERE, des requêtes Paramètre ou des objets **QueryDef** qui extraient des enregistrements indexés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type v objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="a5d2b-p109">Il est recommandé d'utiliser le format de date des États-Unis (mois-jour-année) lorsque vous effectuez des recherches dans des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access ; à défaut, les données risquent d'être introuvables. Vous pouvez utiliser la fonction **Format** de Visual Basic pour convertir la date. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="a5d2b-154">Si l’argument critères se compose d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Appelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-154">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="a5d2b-155">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-155">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="a5d2b-156">Pour optimiser les performances, les *critères* doivent être dans un le formulaire «*champ* = *valeur*» où *champ* représente un champ indexé dans la table de base sous-jacente, ou «*champ* LIKE *préfixe » où *le champ* est*un les champs indexés dans la table de base sous-jacente et le *préfixe* est une chaîne de recherche de préfixe (par exemple, « ART \* »).</span><span class="sxs-lookup"><span data-stu-id="a5d2b-156">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*" ).</span></span>
> 
> - <span data-ttu-id="a5d2b-p111">En règle générale, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que la méthode **Find**. Cela suppose que les objets **Recordset** de type table peuvent à eux seuls répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


## <a name="example"></a><span data-ttu-id="a5d2b-159">Exemple</span><span class="sxs-lookup"><span data-stu-id="a5d2b-159">Example</span></span>

<span data-ttu-id="a5d2b-160">L'exemple suivant montre comment utiliser les méthodes FindFirst et FindNext pour rechercher un enregistrement dans un Recordset.</span><span class="sxs-lookup"><span data-stu-id="a5d2b-160">The following example shows how to use the FindFirst and FindNext methods to find a record in a Recordset.</span></span>

<span data-ttu-id="a5d2b-161">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="a5d2b-161">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>


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
