---
title: Autre solution : Utilisation des instructions SQL
TOCTitle: 'Alternatives: Using SQL Statements'
ms:assetid: 9ed787da-7099-2ef5-b2c6-c4f6bce5ddfe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249727(v=office.15)
ms:contentKeyID: 48546668
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9451dfef969120e6ffc4835263a7ad02881748d2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470131"
---
# <a name="alternatives-using-sql-statements"></a>Autre solution : Utilisation des instructions SQL


**S’applique à**: Access 2013 | Office 2013

Au lieu d'utiliser ses propriétés et méthodes intégrées pour modifier des données, ADO permet aussi d'utiliser des commandes. En fonction de votre fournisseur, toutes les opérations mentionnées dans ce chapitre peuvent également être effectuées en passant des commandes à votre source de données. Par exemple, vous pouvez utiliser les instructions SQL UPDATE pour modifier des données sans utiliser la propriété **Value** d'un objet **Field**. Vous pouvez utiliser les instructions SQL INSERT pour ajouter des nouveaux enregistrements à une source de données au lieu de la méthode ADO **AddNew**. Pour plus d'informations sur SQL ou le langage de manipulation des données utilisé par votre fournisseur, consultez la documentation de votre source de données.

Par exemple, vous pouvez passer une chaîne SQL contenant une instruction DELETE à une base de données, comme l'illustre le code suivant :

```vb 
'BeginSQLDelete 
strSQL = "DELETE FROM Shippers WHERE ShipperID = " & intId 
objConn.Execute strSQL, , adCmdText + adExecuteNoRecords 
'EndSQLDelete 
```

