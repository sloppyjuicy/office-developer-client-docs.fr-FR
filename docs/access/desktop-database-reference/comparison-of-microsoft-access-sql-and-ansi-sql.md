---
title: Comparaison de Microsoft Access SQL et ANSI SQL
TOCTitle: Comparison of Microsoft Access SQL and ANSI SQL
ms:assetid: 0686f98f-10fe-0e02-e9d1-84ff3e755b57
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844937(v=office.15)
ms:contentKeyID: 48543052
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e9f30401891452970fdbe80123fc373e26f26c6
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870856"
---
# <a name="comparison-of-microsoft-access-sql-and-ansi-sql"></a>Comparaison de Microsoft Access SQL et d’ANSI SQL

**S’applique à** : Access 2013, Office 2013

Le langage SQL du moteur de base de données Microsoft Access est en général conforme à la norme ANSI-89 de niveau 1. Toutefois, certaines fonctionnalités de SQL ANSI ne sont pas implémentées dans Microsoft Access SQL. Inversement, Microsoft Access SQL comporte des mots clés et des fonctionnalités qui ne sont pas prises en charge dans ANSI SQL.

## <a name="major-differences"></a>Principales différences

- Microsoft Access SQL et ANSI SQL utilisent des mots réservés et des types de données différents. Pour plus d'informations, voir [Mots réservés SQL du moteur de base de données Microsoft Access](sql-reserved-words.md) et [Types de données équivalents ANSI SQL](equivalent-ansi-sql-data-types.md). Le fournisseur OLE DB du moteur de base de données Microsoft Access utilise d'autres mots réservés.

- **[Between…And](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**
    
  *expr1* \[ NOT \] **Between** *value1* **and** *value2*
    
  Dans Microsoft Access SQL, la *valeur1* peut être supérieure à la *valeur2* ; dans ANSI SQL, la *valeur1* doit être égale ou inférieure à la *valeur2.*

- Microsoft Access SQL prend en charge les caractères génériques ANSI SQL et les [caractères génériques](using-wildcard-characters-in-string-comparisons.md) propres au moteur de base de données Microsoft Access qui sont utilisés avec l'opérateur **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**. Les caractères génériques ANSI et du moteur de base de données Microsoft Access s'excluent mutuellement dans les instructions SQL. Vous ne pouvez utiliser qu'un seul type de caractères génériques, vous ne pouvez pas mélanger les deux. Les caractères génériques ANSI SQL ne peuvent être utilisés qu'avec le moteur de base de données Microsoft Access et le fournisseur OLE DB du moteur de base de données Microsoft Access. Si vous essayez d'utiliser les caractères génériques ANSI SQL dans Microsoft Access ou DAO, ils seront interprétés en tant que texte. Le contraire est vrai avec le fournisseur OLE DB du moteur de base de données Microsoft Access.
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><p>Caractère correspondant</p></th>
    <th><p>Microsoft Access SQL</p></th>
    <th><p>ANSI SQL</p></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Un seul caractère</p></td>
    <td><p>?</p></td>
    <td><p>_ (soulignement)</p></td>
    </tr>
    <tr class="even">
    <td><p>Zéro ou plusieurs caractères</p></td>
    <td><p>*</p></td>
    <td><p>%</p></td>
    </tr>
    </tbody>
    </table>


- Microsoft Access SQL est en général moins restrictif. Il permet par exemple de regrouper et d'ordonner des expressions.

- Microsoft Access SQL prend en charge des expressions plus puissantes.

## <a name="enhanced-features-of-microsoft-access-sql"></a>Fonctionnalités améliorées de Microsoft Access SQL

Microsoft Access SQL comporte les fonctionnalités améliorées suivantes :

- l'instruction [TRANSFORM ](transform-statement-microsoft-access-sql.md) qui prend en charge les requêtes croisées ;

- des [fonctions d'agrégation](sql-aggregate-functions-sql.md), telles que **StDev** et **VarP**;

- la déclaration [PARAMETERS ](parameters-declaration-microsoft-access-sql.md) pour définir des requêtes Paramètres.

## <a name="ansi-sql-features-not-supported-in-microsoft-access-sql"></a>Les fonctionnalités SQL ANSI ne sont pas pris en charge dans Microsoft Access SQL

Microsoft Access SQL ne prend pas en charge les fonctionnalités ANSI SQL suivantes :

- les références à des fonctions d'agrégation DISTINCT (par exemple, Microsoft Access SQL n'autorise pas SUM(DISTINCT *nom de la colonne*) ;

- la clause LIMIT TO *nn* ROWS utilisée pour limiter le nombre de lignes renvoyées par une requête. Vous ne pouvez utiliser que la [clause WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) pour limiter l’étendue d’une requête.

