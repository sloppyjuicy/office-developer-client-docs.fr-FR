---
title: Recordset2.FindFirst, méthode (DAO)
TOCTitle: FindFirst Method
ms:assetid: 2a18e81a-a9e5-cc1a-50b2-40c1f1b7fa06
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192064(v=office.15)
ms:contentKeyID: 48543902
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 823a9b0e095bb726d749021cca99d26f1cc8ceba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309407"
---
# <a name="recordset2findfirst-method-dao"></a><span data-ttu-id="ab6db-102">Recordset2.FindFirst, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="ab6db-102">Recordset2.FindFirst method (DAO)</span></span>

<span data-ttu-id="ab6db-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab6db-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab6db-104">Localise le premier enregistrement dans un objet **Recordset** de type feuille de réponse dynamique ou capture instantanée qui remplit les critères spécifiés et rend l’enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="ab6db-104">Locates the first record in a dynaset- or snapshot-type **Recordset** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ab6db-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab6db-105">Syntax</span></span>

<span data-ttu-id="ab6db-106">*expression* .FindFirst(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="ab6db-106">*expression* .FindFirst(***Criteria***)</span></span>

<span data-ttu-id="ab6db-107">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="ab6db-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab6db-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="ab6db-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab6db-109">Nom</span><span class="sxs-lookup"><span data-stu-id="ab6db-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ab6db-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="ab6db-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ab6db-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="ab6db-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ab6db-112">Description</span><span class="sxs-lookup"><span data-stu-id="ab6db-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab6db-113"><em>Critères</em></span><span class="sxs-lookup"><span data-stu-id="ab6db-113"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="ab6db-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ab6db-114">Required</span></span></p></td>
<td><p><span data-ttu-id="ab6db-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="ab6db-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6db-p101">Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="ab6db-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ab6db-118">Remarks</span></span>

<span data-ttu-id="ab6db-p102">Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d’un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="ab6db-p103">Si un enregistrement correspondant aux critères n’est pas localisé, le pointeur d’enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l’occurrence suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="ab6db-123">Chacune des méthodes **Find** commence sa recherche à partir de l’emplacement et dans le sens spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ab6db-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ab6db-124">Méthode Find</span><span class="sxs-lookup"><span data-stu-id="ab6db-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="ab6db-125">Point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="ab6db-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="ab6db-126">Sens de la recherche</span><span class="sxs-lookup"><span data-stu-id="ab6db-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ab6db-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="ab6db-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6db-128">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="ab6db-129">Fin du jeu d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab6db-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="ab6db-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6db-131">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="ab6db-132">Début du jeu d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ab6db-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="ab6db-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6db-134">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="ab6db-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="ab6db-135">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ab6db-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="ab6db-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="ab6db-137">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="ab6db-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="ab6db-138">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="ab6db-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab6db-p104">L’utilisation de l’une des méthodes **Find** n’équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l’enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d’une opération Move.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="ab6db-p105">Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l’opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l’enregistrement actif n’est pas défini. Dans ce cas, vous devez positionner le pointeur d’enregistrement actif sur un enregistrement valide.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="ab6db-p106">L’utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s’avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="ab6db-p107">Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l’utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="ab6db-p108">Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n’utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="ab6db-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="ab6db-152">Si les critères se composent d’une chaîne concaténée comportant une valeur non entière, et que les paramètres système spécifient un caractère décimal d’un format différent de celui des États-Unis, tel qu’une virgule (par exemple, strSQL = "PRICE \> " & lngPrice, et lngPrice = 125,50), une erreur se produit lorsque vous tentez d’appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="ab6db-152">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="ab6db-153">Il s’agit, car lors de la concaténation, le nombre est converti en une chaîne à l’aide du caractère décimal par défaut de votre système et Microsoft Access SQL accepte uniquement des caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="ab6db-153">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="ab6db-154">Pour de meilleures performances, le critère \*\*\* doit se trouver sous la forme « valeur de champ » où le champ est un champ indexé dans la table de base sous-jacente, ou « préfixe like de champ » où le champ est un champ indexé dans la table de base sous-jacente etle préfixe est une chaîne de recherche de  =  préfixe (par exemple, « ART\* »).     </span><span class="sxs-lookup"><span data-stu-id="ab6db-154">For best performance, the *criteria*\* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="ab6db-p110">En général, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que les méthodes **Find**. Cela suppose que les objets **Recordset** de type table suffisent à répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="ab6db-p110">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>


