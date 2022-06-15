---
title: Expressions SQL (référence de base de données de bureau Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: cd43f35af5a0c413f5f295cfecebec71318ec274
ms.sourcegitcommit: a6d13fdae7eb2e503236c1b629a59b36a4fb76f1
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2022
ms.locfileid: "66084094"
---
# <a name="sql-expressions"></a>Expressions SQL

**S’applique à** : Access 2013, Office 2013

Une  SQL est une chaîne occupe tout ou partie d’une instruction SQL. Par exemple, la méthode FindFirst sur un objet Recordset[ utilise une expression SQL constituée des critères de sélection trouvés dans une clause SQL WHERE.

Le moteur de base de données Microsoft Access utilise le service d’expressions Microsoft Visual Basic pour Applications (VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples. Tous les opérateurs utilisés dans les expressions SQL du moteur de base de données Microsoft Access (sauf **[Between](/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** et **[Like](/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) sont définis par le service d’expressions VBA.

En outre, le service d'expressions VBA offre plus de 100 fonctions VBA que vous pouvez utiliser dans les expressions SQL. Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL en mode Création de requête dans Microsoft Access, et vous pouvez également utiliser ces fonctions dans une requête SQL de la méthode **OpenRecordset** DAO créée en code Microsoft Visual C++, Microsoft Visual Basic, et Microsoft Excel.

## <a name="see-also"></a>Voir aussi

- [Concepts de VBA Access](/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
