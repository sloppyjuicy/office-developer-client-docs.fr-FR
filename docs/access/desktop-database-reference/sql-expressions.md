---
title: Expressions SQL (référence de base de données du bureau Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5a8d340f008fd198068d6dacc1b2bf847838ede1
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025734"
---
# <a name="sql-expressions"></a><span data-ttu-id="ebfd4-102">Expressions SQL</span><span class="sxs-lookup"><span data-stu-id="ebfd4-102">SQL expressions</span></span>

<span data-ttu-id="ebfd4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ebfd4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ebfd4-p101">Une expression SQL est une chaîne qui constitue la totalité ou une partie d'une instruction SQL. Par exemple, la méthode **FindFirst** sur un objet **Recordset** utilise une expression SQL constituée des critères de sélection trouvés dans une [clause WHERE](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql) SQL.</span><span class="sxs-lookup"><span data-stu-id="ebfd4-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the **FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/where-clause-microsoft-access-sql).</span></span>

<span data-ttu-id="ebfd4-106">Le moteur de base de données Microsoft Access utilise le service d’expression Microsoft Visual Basic pour Applications (ou VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples.</span><span class="sxs-lookup"><span data-stu-id="ebfd4-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="ebfd4-107">Tous les opérateurs utilisés dans les expressions du SQL du moteur de base de données Microsoft Access (sauf **[entre](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** et **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) sont définis par le service d’expression VBA.</span><span class="sxs-lookup"><span data-stu-id="ebfd4-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)**, and **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) are defined by the VBA expression service.</span></span> <span data-ttu-id="ebfd4-108">En outre, le service d'expressions VBA offre plus de 100 fonctions VBA que vous pouvez utiliser dans les expressions SQL, par exemple, pour composer une requête SQL en mode création dans Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="ebfd4-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="ebfd4-109">Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL de la requête Microsoft Access en mode Création, et vous pouvez également utiliser ces fonctions dans une requête SQL dans la méthode DAO **OpenRecordset** dans Microsoft Visual C++, Microsoft Visual Basic et Microsoft Code d’Excel.</span><span class="sxs-lookup"><span data-stu-id="ebfd4-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

## <a name="see-also"></a><span data-ttu-id="ebfd4-110">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebfd4-110">See also</span></span>

- [<span data-ttu-id="ebfd4-111">Concepts liés à VBA Access</span><span class="sxs-lookup"><span data-stu-id="ebfd4-111">Access VBA Concepts</span></span>](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)