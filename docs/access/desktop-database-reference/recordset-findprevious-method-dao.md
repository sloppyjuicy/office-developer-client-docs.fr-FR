---
title: Recordset.FindPrevious, méthode (DAO)
TOCTitle: FindPrevious Method
ms:assetid: 62f26b0b-f3f1-a6fe-e84d-f93623e1f7f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194940(v=office.15)
ms:contentKeyID: 48545252
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052885
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bbd678c460ed6c54a38e76faa2a2492cfd4e3384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300489"
---
# <a name="recordsetfindprevious-method-dao"></a><span data-ttu-id="db8ac-102">Recordset.FindPrevious, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="db8ac-102">Recordset.FindPrevious method (DAO)</span></span>

<span data-ttu-id="db8ac-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="db8ac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="db8ac-p101">Recherche l'enregistrement précédent dans un objet **[Recordset](recordset-object-dao.md)** de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="db8ac-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="db8ac-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db8ac-106">Syntax</span></span>

<span data-ttu-id="db8ac-107">*.* FindPrevious(***Criteria***)</span><span class="sxs-lookup"><span data-stu-id="db8ac-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="db8ac-108">*expression* Variable qui représente un objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="db8ac-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="db8ac-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="db8ac-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db8ac-110">Nom</span><span class="sxs-lookup"><span data-stu-id="db8ac-110">Name</span></span></p></th>
<th><p><span data-ttu-id="db8ac-111">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="db8ac-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="db8ac-112">Type de données</span><span class="sxs-lookup"><span data-stu-id="db8ac-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="db8ac-113">Description</span><span class="sxs-lookup"><span data-stu-id="db8ac-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db8ac-114"><em>Critères</em></span><span class="sxs-lookup"><span data-stu-id="db8ac-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="db8ac-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="db8ac-115">Required</span></span></p></td>
<td><p><span data-ttu-id="db8ac-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="db8ac-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="db8ac-p102">Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p102">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="db8ac-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="db8ac-119">Remarks</span></span>

<span data-ttu-id="db8ac-p103">Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d’un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="db8ac-p104">Si un enregistrement correspondant aux critères n’est pas localisé, le pointeur d’enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l’occurrence suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="db8ac-124">Chacune des méthodes **Find** commence sa recherche à partir de l’emplacement et dans le sens spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="db8ac-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="db8ac-125">Méthode Find</span><span class="sxs-lookup"><span data-stu-id="db8ac-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="db8ac-126">Point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="db8ac-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="db8ac-127">Sens de la recherche</span><span class="sxs-lookup"><span data-stu-id="db8ac-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="db8ac-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="db8ac-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="db8ac-129">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="db8ac-130">Fin du jeu d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db8ac-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="db8ac-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="db8ac-132">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="db8ac-133">Début du jeu d’enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="db8ac-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="db8ac-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="db8ac-135">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="db8ac-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="db8ac-136">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="db8ac-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="db8ac-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="db8ac-138">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="db8ac-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="db8ac-139">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="db8ac-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="db8ac-p105">L’utilisation de l’une des méthodes **Find** n’équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l’enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d’une opération Move.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="db8ac-p106">Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l’opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l’enregistrement actif n’est pas défini. Dans ce cas, vous devez positionner le pointeur d’enregistrement actif sur un enregistrement valide.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="db8ac-p107">L’utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s’avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="db8ac-p108">Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l’utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="db8ac-p109">Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n’utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="db8ac-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="db8ac-153">Si les critères se composent d’une chaîne concaténée comportant une valeur non entière, et que les paramètres système spécifient un caractère décimal d’un format différent de celui des États-Unis, tel qu’une virgule (par exemple, strSQL = "PRICE \> " & lngPrice, et lngPrice = 125,50), une erreur se produit lorsque vous tentez d’appeler la méthode.</span><span class="sxs-lookup"><span data-stu-id="db8ac-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="db8ac-154">Il s’agit, car lors de la concaténation, le nombre est converti en une chaîne à l’aide du caractère décimal par défaut de votre système et Microsoft Access SQL accepte uniquement des caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="db8ac-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="db8ac-155">Pour des performances optimales, les *critères* doivent être au format «*champ* = *valeur*» où *champ* est un champ indexé dans la table de base sous-jacente, ou au format «*champ* LIKE *préfixe*» où *champ* est un champ indexé dans la table de base sous-jacente et *préfixe* une chaîne de recherche de préfixe (par exemple, « ART\* »).</span><span class="sxs-lookup"><span data-stu-id="db8ac-155">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="db8ac-p111">En général, pour des types de recherches équivalents, la méthode **Seek** offre de meilleures performances que les méthodes **Find**. Cela suppose que les objets **Recordset** de type table suffisent à répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="db8ac-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>
