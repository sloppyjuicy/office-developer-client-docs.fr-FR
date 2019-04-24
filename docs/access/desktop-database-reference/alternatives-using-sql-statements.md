---
title: 'Alternatives : Utilisation d’instructions SQL'
TOCTitle: 'Alternatives: Using SQL statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 185f5c1eb7e11a9425ff6cc4a16f1387424f3219
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297150"
---
# <a name="alternatives-using-sql-statements"></a><span data-ttu-id="bc3ba-102">Alternatives : Utilisation d’instructions SQL</span><span class="sxs-lookup"><span data-stu-id="bc3ba-102">Alternatives: Using SQL statements</span></span>


<span data-ttu-id="bc3ba-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc3ba-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc3ba-p101">Au lieu d'utiliser ses propriétés et méthodes intégrées pour modifier des données, ADO permet aussi d'utiliser des commandes. En fonction de votre fournisseur, toutes les opérations mentionnées dans ce chapitre peuvent également être effectuées en passant des commandes à votre source de données. Par exemple, vous pouvez utiliser les instructions SQL UPDATE pour modifier des données sans utiliser la propriété **Value** d'un objet **Field**. Vous pouvez utiliser les instructions SQL INSERT pour ajouter des nouveaux enregistrements à une source de données au lieu de la méthode ADO **AddNew**. Pour plus d'informations sur SQL ou le langage de manipulation des données utilisé par votre fournisseur, consultez la documentation de votre source de données.</span><span class="sxs-lookup"><span data-stu-id="bc3ba-p101">ADO also allows using commands as alternatives to its built-in properties and methods for editing data. Depending upon your provider, all operations mentioned in this chapter could also be accomplished by passing commands to your data source. For example, SQL UPDATE statements can be used to modify data without using the **Value** property of a **Field**. SQL INSERT statements can be used to add new records to a data source, rather than the ADO method **AddNew**. For more information about SQL or the data-manipulation language of your provider, see the documentation of your data source.</span></span>

<span data-ttu-id="bc3ba-109">Par exemple, vous pouvez passer une chaîne SQL contenant une instruction DELETE à une base de données, comme l'illustre le code suivant :</span><span class="sxs-lookup"><span data-stu-id="bc3ba-109">For example, you can pass a SQL string containing a DELETE statement to a database, as shown in the following code:</span></span>

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

