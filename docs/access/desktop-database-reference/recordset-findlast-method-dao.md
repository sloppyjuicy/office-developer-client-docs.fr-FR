---
title: Recordset.FindLast Method (DAO)
TOCTitle: FindLast Method
ms:assetid: 65236519-3474-a760-99bc-2e8f6bfeee7a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195128(v=office.15)
ms:contentKeyID: 48545311
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32c1f5f5cefe0930ba67f47367584c8c5489e963
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469922"
---
# <a name="recordsetfindlast-method-dao"></a><span data-ttu-id="a3d59-102">Recordset.FindLast Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a3d59-102">Recordset.FindLast Method (DAO)</span></span>


<span data-ttu-id="a3d59-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3d59-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a3d59-104">Recherche le dernier enregistrement dans un objet **[Recordset](recordset-object-dao.md)** de type feuille de réponse dynamique ou instantané qui satisfait aux critères spécifiés, et en fait l'enregistrement actif (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="a3d59-104">Locates the last record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d59-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3d59-105">Syntax</span></span>

<span data-ttu-id="a3d59-106">*expression* . FindLast (***critères***)</span><span class="sxs-lookup"><span data-stu-id="a3d59-106">*expression* .FindLast(***Criteria***)</span></span>

<span data-ttu-id="a3d59-107">*expression* Variable qui représente un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a3d59-107">*expression* A variable that represents a **Recordset** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a3d59-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3d59-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3d59-109">Name</span><span class="sxs-lookup"><span data-stu-id="a3d59-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a3d59-110">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="a3d59-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a3d59-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="a3d59-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a3d59-112">Description</span><span class="sxs-lookup"><span data-stu-id="a3d59-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3d59-113">Critères</span><span class="sxs-lookup"><span data-stu-id="a3d59-113">Criteria</span></span></p></td>
<td><p><span data-ttu-id="a3d59-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3d59-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a3d59-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="a3d59-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d59-p101">Données de type String utilisées pour localiser l'enregistrement. S'apparente à la clause WHERE d'une instruction SQL sans toutefois le mot WHERE.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a3d59-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3d59-118">Remarks</span></span>

<span data-ttu-id="a3d59-p102">Si vous souhaitez inclure tous les enregistrements dans votre recherche, et non uniquement ceux qui remplissent une condition particulière, utilisez les méthodes **Move** pour passer d'un enregistrement à un autre. Pour localiser un enregistrement dans un **Recordset** de type table, utilisez la méthode **Seek**.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="a3d59-p103">Si un enregistrement correspondant aux critères n'est pas localisé, le pointeur d'enregistrement actif est inconnu et la propriété **NoMatch** est définie sur **True**. Si le recordset contient plusieurs enregistrements correspondant aux critères, **FindFirst** localise la première occurrence, **FindNext** localise l'occurrence suivante, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="a3d59-123">Chacune des méthodes **Find** commence sa recherche à partir de l'emplacement et dans le sens spécifiés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3d59-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3d59-124">Méthode Find</span><span class="sxs-lookup"><span data-stu-id="a3d59-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="a3d59-125">Point de départ de la recherche</span><span class="sxs-lookup"><span data-stu-id="a3d59-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="a3d59-126">Sens de la recherche</span><span class="sxs-lookup"><span data-stu-id="a3d59-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3d59-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="a3d59-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d59-128">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="a3d59-129">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3d59-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="a3d59-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d59-131">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="a3d59-132">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a3d59-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="a3d59-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d59-134">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="a3d59-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="a3d59-135">Fin du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3d59-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="a3d59-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d59-137">Enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="a3d59-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="a3d59-138">Début du jeu d'enregistrements</span><span class="sxs-lookup"><span data-stu-id="a3d59-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3d59-139">Lorsque vous utilisez la méthode **FindLast**, le moteur de base de données Microsoft Access remplit entièrement votre objet **Recordset** avant de lancer la recherche, si cela n'a pas déjà été fait.</span><span class="sxs-lookup"><span data-stu-id="a3d59-139">When you use the **FindLast** method, the Microsoft Access database engine fully populates your **Recordset** before beginning the search, if this hasn't already happened.</span></span>

<span data-ttu-id="a3d59-p104">L'utilisation de l'une des méthodes **Find** n'équivaut pas à utiliser une méthode **Move**, qui ne fait que rendre actif l'enregistrement initial, final, suivant ou précédent sans spécifier de condition. Vous pouvez faire suivre une opération Find d'une opération Move.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="a3d59-p105">Vérifiez toujours la valeur de la propriété **NoMatch** pour déterminer si l'opération Find a réussi. Si la recherche aboutit, **NoMatch** a la valeur **False**. Si elle échoue, **NoMatch** a la valeur **True** et l'enregistrement actif n'est pas défini. Dans ce cas, vous devez positionner le pointeur d'enregistrement actif sur un enregistrement valide.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="a3d59-p106">L'utilisation des méthodes **Find** avec les recordsets ODBC connectés au moteur de base de données Microsoft Access peut s'avérer inefficace. Il se peut que la reformulation de vos critères pour localiser un enregistrement spécifique soit plus rapide, surtout si vous travaillez avec des recordsets volumineux.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="a3d59-p107">Lorsque vous utilisez des bases de données ODBC connectées au moteur de base de données Microsoft Access et de grands objets **Recordset** de type feuille de réponse dynamique, il se peut que l'utilisation des méthodes **Find** ou des propriétés **Sort** ou **Filter** soit lente. Pour améliorer les performances, utilisez des requêtes SQL avec des clauses ORDER BY ou WHERE personnalisées, des requêtes avec paramètres ou des objets **QueryDef** qui récupèrent des enregistrements indexés spécifiques.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="a3d59-p108">Vous devez utiliser un format de date américain (mois-jour-année) lorsque vous recherchez des champs contenant des dates, même si vous n'utilisez pas la version américaine du moteur de base de données Microsoft Access. Sinon, les données risquent de ne pas être trouvées. Utilisez la fonction **Format** de Visual Basic pour convertir la date. Par exemple :</span><span class="sxs-lookup"><span data-stu-id="a3d59-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="a3d59-153">Si l’argument critères se compose d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix \> » & lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez de Appelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="a3d59-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="a3d59-154">En effet, au cours de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut de votre système et le langage SQL Microsoft Access n'accepte que les caractères décimaux américains.</span><span class="sxs-lookup"><span data-stu-id="a3d59-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="a3d59-155">Pour optimiser les performances, les <EM>critères</EM> doivent être dans un le formulaire «<EM>champ</EM> = <EM>valeur</EM>» où <EM>champ</EM> représente un champ indexé dans la table de base sous-jacente, ou «<EM>champ</EM> LIKE <EM>préfixe » où <EM>le champ</EM> est</EM>un les champs indexés dans la table de base sous-jacente et le <EM>préfixe</EM> est une chaîne de recherche de préfixe (par exemple, « ART \* »).</span><span class="sxs-lookup"><span data-stu-id="a3d59-155">For best performance, the <EM>criteria</EM> should be in either the form "<EM>field</EM> = <EM>value</EM>" where <EM>field</EM> is an indexed field in the underlying base table, or "<EM>field</EM> LIKE <EM>prefix</EM>" where <EM>field</EM> is an indexed field in the underlying base table and <EM>prefix</EM> is a prefix search string (for example, "ART\*" ).</span></span></P>
> <LI>
> <P><span data-ttu-id="a3d59-p110">En règle générale, pour des types de recherches équivalents, la méthode <STRONG>Seek</STRONG> offre de meilleures performances que la méthode <STRONG>Find</STRONG>. Cela suppose que les objets <STRONG>Recordset</STRONG> de type table peuvent à eux seuls répondre à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="a3d59-p110">In general, for equivalent types of searches, the <STRONG>Seek</STRONG> method provides better performance than the <STRONG>Find</STRONG> methods. This assumes that table-type <STRONG>Recordset</STRONG> objects alone can satisfy your needs.</span></span></P></LI></UL>


