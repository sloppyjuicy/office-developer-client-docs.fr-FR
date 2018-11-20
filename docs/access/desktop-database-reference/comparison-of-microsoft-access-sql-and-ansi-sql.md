---
title: Comparaison de Microsoft Access SQL et ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ce6b1ae1ab15a25eca61a22049d538736c3672d
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026182"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a><span data-ttu-id="3f633-102">Comparaison de Microsoft Access SQL et ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="3f633-102">Comparison of Microsoft Access SQL and ANSI SQL</span></span>

<span data-ttu-id="3f633-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f633-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3f633-104">Le langage SQL du moteur de base de données Microsoft Access est en général conforme à la norme ANSI-89 de niveau 1.</span><span class="sxs-lookup"><span data-stu-id="3f633-104">Microsoft Access database engine SQL is generally ANSI-89 Level 1 compliant.</span></span> <span data-ttu-id="3f633-105">Toutefois, certaines fonctionnalités ANSI SQL ne sont pas implémentées dans Microsoft Access SQL.</span><span class="sxs-lookup"><span data-stu-id="3f633-105">However, certain ANSI SQL features are not implemented in Microsoft Access SQL.</span></span> <span data-ttu-id="3f633-106">Inversement, Microsoft Access SQL comporte des mots clés et des fonctionnalités qui ne sont pas prises en charge dans ANSI SQL.</span><span class="sxs-lookup"><span data-stu-id="3f633-106">Conversely, Microsoft Access SQL includes reserved words and features not supported in ANSI SQL.</span></span>

## <a name="major-differences"></a><span data-ttu-id="3f633-107">Différences principales</span><span class="sxs-lookup"><span data-stu-id="3f633-107">Major differences</span></span>

- <span data-ttu-id="3f633-p102">Microsoft Access SQL et ANSI SQL utilisent des mots réservés et des types de données différents. Pour plus d'informations, voir [Mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md) et [Types de données équivalents ANSI SQL](equivalent-ansi-sql-data-types.md). Le fournisseur OLE DB du moteur de base de données Microsoft Access utilise d'autres mots réservés.</span><span class="sxs-lookup"><span data-stu-id="3f633-p102">Microsoft Access SQL and ANSI SQL each have different reserved words and data types. For more information, see [Microsoft Access Database Engine SQL Reserved Words](sql-reserved-words.md) and [Equivalent ANSI SQL Data Types](equivalent-ansi-sql-data-types.md). Using the Microsoft Access Database Engine OLE DB Provider there are additional reserved words.</span></span>

- <span data-ttu-id="3f633-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span><span class="sxs-lookup"><span data-stu-id="3f633-111">**[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**</span></span>
    
  <span data-ttu-id="3f633-112">*expr1* \[Pas\] **entre** *valeur1* **et** *valeur2*</span><span class="sxs-lookup"><span data-stu-id="3f633-112">*expr1* \[NOT\] **Between** *value1* **And** *value2*</span></span>
    
  <span data-ttu-id="3f633-113">Dans Microsoft Access SQL, la *valeur1* peut être supérieure à la *valeur2* ; dans ANSI SQL, la *valeur1* doit être égale ou inférieure à la *valeur2.*</span><span class="sxs-lookup"><span data-stu-id="3f633-113">In Microsoft Access SQL, *value1* can be greater than *value2*; in ANSI SQL, *value1* must be equal to or less than *value2.*</span></span>

- <span data-ttu-id="3f633-p103">Microsoft Access SQL prend en charge les caractères génériques ANSI SQL et les [caractères génériques](using-wildcard-characters-in-string-comparisons.md) propres au moteur de base de données Microsoft Access qui sont utilisés avec l'opérateur **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**. Les caractères génériques ANSI et du moteur de base de données Microsoft Access s'excluent mutuellement dans les instructions SQL. Vous ne pouvez utiliser qu'un seul type de caractères génériques, vous ne pouvez pas mélanger les deux. Les caractères génériques ANSI SQL ne peuvent être utilisés qu'avec le moteur de base de données Microsoft Access et le fournisseur OLE DB du moteur de base de données Microsoft Access. Si vous essayez d'utiliser les caractères génériques ANSI SQL dans Microsoft Access ou DAO, ils seront interprétés en tant que texte. Le contraire est vrai avec le fournisseur OLE DB du moteur de base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3f633-p103">Microsoft Access SQL supports both ANSI SQL wildcard characters and [wildcard characters](using-wildcard-characters-in-string-comparisons.md) that are specific to the Microsoft Access database engine to use with the **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)** operator. The use of the ANSI and Microsoft Access database engine wildcard characters is mutually exclusive. You must use one set or the other and cannot mix them. The ANSI SQL wildcards are only available when using the Microsoft Access database engine and the Microsoft Access Database Engine OLE DB Provider. If you try to use the ANSI SQL wildcards through Microsoft Access or DAO, then they will be interpreted as literals. The opposite is true when using the Microsoft Access Database Engine OLE DB Provider.</span></span>
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p><span data-ttu-id="3f633-120">Caractère correspondant</span><span class="sxs-lookup"><span data-stu-id="3f633-120">Matching character</span></span></p></th>
    <th><p><span data-ttu-id="3f633-121">Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="3f633-121">Microsoft Access SQL</span></span></p></th>
    <th><p><span data-ttu-id="3f633-122">ANSI SQL</span><span class="sxs-lookup"><span data-stu-id="3f633-122">ANSI SQL</span></span></p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="3f633-123">Un seul caractère</span><span class="sxs-lookup"><span data-stu-id="3f633-123">Any single character</span></span></p></td>
    <td><p><span data-ttu-id="3f633-124">?</span><span class="sxs-lookup"><span data-stu-id="3f633-124"></span></span></p></td>
    <td><p><span data-ttu-id="3f633-125">_ (soulignement)</span><span class="sxs-lookup"><span data-stu-id="3f633-125">_ (underscore)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="3f633-126">Zéro ou plusieurs caractères</span><span class="sxs-lookup"><span data-stu-id="3f633-126">Zero or more characters</span></span></p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- <span data-ttu-id="3f633-p104">Microsoft Access SQL est en général moins restrictif. Il permet par exemple de regrouper et d'ordonner des expressions.</span><span class="sxs-lookup"><span data-stu-id="3f633-p104">Microsoft Access SQL is generally less restrictive. For example, it permits grouping and ordering on expressions.</span></span>

- <span data-ttu-id="3f633-129">Microsoft Access SQL prend en charge des expressions plus puissantes.</span><span class="sxs-lookup"><span data-stu-id="3f633-129">Microsoft Access SQL supports more powerful expressions.</span></span>

## <a name="enhanced-features-of-microsoft-access-sql"></a><span data-ttu-id="3f633-130">Fonctionnalités améliorées de Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="3f633-130">Enhanced features of Microsoft Access SQL</span></span>

<span data-ttu-id="3f633-131">Microsoft Access SQL comporte les fonctionnalités améliorées suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f633-131">Microsoft Access SQL provides the following enhanced features:</span></span>

- <span data-ttu-id="3f633-132">l'instruction [TRANSFORM ](transform-statement-microsoft-access-sql.md) qui prend en charge les requêtes croisées ;</span><span class="sxs-lookup"><span data-stu-id="3f633-132">The [TRANSFORM](transform-statement-microsoft-access-sql.md) statement, which provides support for crosstab queries.</span></span>

- <span data-ttu-id="3f633-133">des [fonctions d'agrégation](sql-aggregate-functions-sql.md), telles que **StDev** et **VarP**;</span><span class="sxs-lookup"><span data-stu-id="3f633-133">Additional [aggregate functions](sql-aggregate-functions-sql.md), such as **StDev** and **VarP**.</span></span>

- <span data-ttu-id="3f633-134">la déclaration [PARAMETERS ](parameters-declaration-microsoft-access-sql.md) pour définir des requêtes Paramètres.</span><span class="sxs-lookup"><span data-stu-id="3f633-134">The [PARAMETERS](parameters-declaration-microsoft-access-sql.md) declaration for defining parameter queries.</span></span>

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a><span data-ttu-id="3f633-135">Fonctionnalités ANSI SQL non prises en charge dans Microsoft Access SQL</span><span class="sxs-lookup"><span data-stu-id="3f633-135">ANSI SQL features not supported in Microsoft Access SQL</span></span>

<span data-ttu-id="3f633-136">Microsoft Access SQL ne prend pas en charge les fonctionnalités ANSI SQL suivantes :</span><span class="sxs-lookup"><span data-stu-id="3f633-136">Microsoft Access SQL does not support the following ANSI SQL features:</span></span>

- <span data-ttu-id="3f633-p105">les références à des fonctions d'agrégation DISTINCT (par exemple, Microsoft Access SQL n'autorise pas SUM(DISTINCT *nom de la colonne*) ;</span><span class="sxs-lookup"><span data-stu-id="3f633-p105">DISTINCT aggregate function references. For example, Microsoft Access SQL does not allow SUM(DISTINCT *columnname*).</span></span>

- <span data-ttu-id="3f633-139">La clause LIMIT TO *nn* ROWS utilisée pour limiter le nombre de lignes retournées par une requête.</span><span class="sxs-lookup"><span data-stu-id="3f633-139">The LIMIT TO *nn* ROWS clause used to limit the number of rows returned by a query.</span></span> <span data-ttu-id="3f633-140">Vous ne pouvez utiliser que la [clause WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) pour limiter l'étendue d'une requête.</span><span class="sxs-lookup"><span data-stu-id="3f633-140">You can use only the [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) to limit the scope of a query.</span></span>

