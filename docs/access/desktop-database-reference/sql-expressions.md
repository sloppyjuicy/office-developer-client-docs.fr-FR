---
title: Expressions SQL (référence de base de données de bureau Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 5bbe9718bfb18ced5f09d2a9396e1e0829d0d81b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308567"
---
# <a name="sql-expressions"></a>Expressions SQL

**S’applique à** : Access 2013, Office 2013

Une ** SQL est une chaîne occupe tout ou partie d’une instruction SQL. Par exemple, la méthode **FindFirst** sur un objet **Recordset[ utilise une expression SQL constituée des critères de sélection trouvés dans une clause SQL WHERE.

Le moteur de base de données Microsoft Access utilise le service d’expressions Microsoft Visual Basic pour Applications (ou VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples. Tous les opérateurs utilisés dans les expressions SQL du moteur de base de données Microsoft Access (sauf **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** et **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) sont définis par le service d’expressions VBA. De plus, le service d’expressions VBA propose plus de 100 fonctions VBA que vous pouvez utiliser dans des expressions SQL. Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL dans le mode Création de requête Microsoft Access, ainsi que dans une requête SQL dans la méthode **OpenRecordset** de DAO en code Microsoft Visual C++, Microsoft Visual Basic et Microsoft Excel.

## <a name="see-also"></a>Voir aussi

- [Concepts de VBA Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
