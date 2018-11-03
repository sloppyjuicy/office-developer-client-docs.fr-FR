---
title: Expressions SQL (référence de base de données du bureau Access)
TOCTitle: SQL Expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92ad643c2a602a24a411db33def62af89520f9b7
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937777"
---
# <a name="sql-expressions"></a><span data-ttu-id="22d38-102">Expressions SQL</span><span class="sxs-lookup"><span data-stu-id="22d38-102">SQL Expressions</span></span>


<span data-ttu-id="22d38-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="22d38-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="22d38-p101">Une expression SQL est une chaîne qui constitue la totalité ou une partie d’une instruction SQL. Par exemple, la méthode**FindFirst** sur un objet **Recordset** utilise une expression SQL constituée des critères de sélection trouvés dans une [clause WHERE](https://msdn.microsoft.com/library/ff195245\(v=office.15\)) SQL.</span><span class="sxs-lookup"><span data-stu-id="22d38-p101">An SQL expression is a string that makes up all or part of an SQL statement. For example, the**FindFirst** method on a **Recordset** object uses an SQL expression consisting of the selection criteria found in an SQL [WHERE clause](https://msdn.microsoft.com/library/ff195245\(v=office.15\)).</span></span>

<span data-ttu-id="22d38-106">Le moteur de base de données Microsoft Access utilise le service d’expression Microsoft Visual Basic pour Applications (ou VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples.</span><span class="sxs-lookup"><span data-stu-id="22d38-106">The Microsoft Access database engine uses the Microsoft Visual Basic for Applications (or VBA) expression service to perform simple arithmetic and function evaluation.</span></span> <span data-ttu-id="22d38-107">Tous les opérateurs utilisés dans les expressions du SQL du moteur de base de données Microsoft Access (sauf **[entre](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))** et **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) sont définis par le service d’expression VBA.</span><span class="sxs-lookup"><span data-stu-id="22d38-107">All of the operators used in Microsoft Access database engine SQL expressions (except **[Between](https://msdn.microsoft.com/library/ff192436\(v=office.15\))**, **[In](https://msdn.microsoft.com/library/ff836369\(v=office.15\))**, and **[Like](https://msdn.microsoft.com/library/ff195752\(v=office.15\))**) are defined by the VBA expression service.</span></span> <span data-ttu-id="22d38-108">En outre, le service d'expressions VBA offre plus de 100 fonctions VBA que vous pouvez utiliser dans les expressions SQL, par exemple, pour composer une requête SQL en mode création dans Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="22d38-108">In addition, the VBA expression service offers over 100 VBA functions that you can use in SQL expressions.</span></span> <span data-ttu-id="22d38-109">Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL de la requête Microsoft Access en mode Création, et vous pouvez également utiliser ces fonctions dans une requête SQL dans la méthode DAO **OpenRecordset** dans Microsoft Visual C++, Microsoft Visual Basic et Microsoft Code d’Excel.</span><span class="sxs-lookup"><span data-stu-id="22d38-109">For example, you can use these VBA functions to compose an SQL query in the Microsoft Access query Design view, and you can also use these functions in an SQL query in the DAO **OpenRecordset** method in Microsoft Visual C++, Microsoft Visual Basic, and Microsoft Excel code.</span></span>

