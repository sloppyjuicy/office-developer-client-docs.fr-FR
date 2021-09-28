---
title: Expressions SQL (référence de base de données de bureau Access)
TOCTitle: SQL expressions
ms:assetid: 91722f18-8589-d9fc-79ef-0be4ab11f822
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197629(v=office.15)
ms:contentKeyID: 48546349
ms.date: 06/13/2019
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 003462c4a16ca9a9de809f9dd87f661a0242992a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589098"
---
# <a name="sql-expressions"></a>Expressions SQL

**S’applique à** : Access 2013, Office 2013

Une  SQL est une chaîne occupe tout ou partie d’une instruction SQL. Par exemple, la méthode FindFirst sur un objet Recordset[ utilise une expression SQL constituée des critères de sélection trouvés dans une clause SQL WHERE.

Le moteur de base de données Microsoft Access utilise le service d’expressions Microsoft Visual Basic pour Applications (VBA) pour effectuer des évaluations arithmétiques et fonctionnelles simples. Tous les opérateurs utilisés dans les expressions SQL du moteur de base de données Microsoft Access (sauf **[Between](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/between-and-operator)**, **[In](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-operator-microsoft-access-sql)** et **[Like](https://docs.microsoft.com/office/vba/access/Concepts/Structured-Query-Language/like-operator-microsoft-access-sql)**) sont définis par le service d’expressions VBA. 

En outre, le service d'expressions VBA offre plus de 100 fonctions VBA que vous pouvez utiliser dans les expressions SQL. Par exemple, vous pouvez utiliser ces fonctions VBA pour composer une requête SQL en mode Création de requête dans Microsoft Access, et vous pouvez également utiliser ces fonctions dans une requête SQL de la méthode **OpenRecordset** DAO créée en code Microsoft Visual C++, Microsoft Visual Basic, et Microsoft Excel.

## <a name="see-also"></a>Voir aussi

- [Concepts de VBA Access](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/concepts-access-vba-reference)
