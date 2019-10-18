---
title: Expressions SQL (référence de base de données de bureau Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: f38932ed4744e5479c523446f9ab77065f4eb203
ms.sourcegitcommit: d0e1ce095a478d90411abb8c147eb9efe19ffa5f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/12/2019
ms.locfileid: "34870863"
---
# <a name="sql-expressions"></a><span data-ttu-id="52485-102">Expressions SQL</span><span class="sxs-lookup"><span data-stu-id="52485-102">SQL expressions</span></span>

<span data-ttu-id="52485-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="52485-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="52485-p101">Une \*\* SQL est une chaîne occupe tout ou partie d’une instruction SQL. Par exemple, la méthode **FindFirst** sur un objet \*\*Recordset[ utilise une expression SQL constituée des critères de sélection trouvés dans une clause SQL WHERE.</span><span class="sxs-lookup"><span data-stu-id="52485-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="52485-106">Le moteur de base de données Microsoft Access utilise le service d’expressions Microsoft Visual Basic pour Applications (VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples.</span><span class="sxs-lookup"><span data-stu-id="52485-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="52485-107">Tous les opérateurs utilisés dans les expressions SQL du moteur de base de données Microsoft Access (sauf **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** et **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) sont définis par le service d’expressions VBA.</span><span class="sxs-lookup"><span data-stu-id="52485-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> 

<span data-ttu-id="52485-108">De plus, le service d’expressions VBA propose plus de 100 fonctions VBA que vous pouvez utiliser dans des expressions SQL.</span><span class="sxs-lookup"><span data-stu-id="52485-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="52485-109">Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL dans le mode Création de requête Microsoft Access, ainsi que dans une requête SQL dans la méthode **OpenRecordset** de DAO en code Microsoft Visual C++, Microsoft Visual Basic et Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="52485-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="52485-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52485-110">See also</span></span>

- [<span data-ttu-id="52485-111">Concepts de VBA Access</span><span class="sxs-lookup"><span data-stu-id="52485-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
