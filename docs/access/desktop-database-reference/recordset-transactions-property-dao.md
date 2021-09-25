---
title: Recordset.Transactions, propriété (DAO)
TOCTitle: Transactions Property
ms:assetid: 7830c056-8d6a-7942-7993-aa04b29cd77f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196110(v=office.15)
ms:contentKeyID: 48545746
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4fba23cc40abc732ffceb8fe91529965e404b806
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602058"
---
# <a name="recordsettransactions-property-dao"></a>Recordset.Transactions, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Renvoie une valeur qui indique si un objet prend en charge les transactions. Valeur **Boolean** en lecture seule.

## <a name="syntax"></a>Syntaxe

*.* Transactions

*expression* Variable qui représente un objet **Recordset**.

## <a name="remarks"></a>Remarques

Dans un espace de travail Microsoft Access, vous pouvez également utiliser la propriété **Transactions** avec des objets **Recordset** de type table ou feuille de réponse dynamique. Les objets **[Recordset](recordset-object-dao.md)** de type capture instantanée et avant uniquement retournent toujours **la forme False**.

Si un objet **Recordset** de type table ou feuille de réponse dynamique est basé sur une table de moteur de base de données Microsoft Access, la propriété **Transactions** a la valeur **True** et vous pouvez utiliser des transactions. Il se peut que d'autres moteurs de base de données ne prennent pas en charge les transactions. Ainsi, vous ne pouvez pas utiliser des transactions dans un objet **Recordset** de type feuille de réponse dynamique basé sur une table Paradox.

Vérifiez la propriété **Transactions** avant d'utiliser la méthode **[BeginTrans](dbengine-begintrans-method-dao.md)** sur l'objet [**Workspace**](workspace-object-dao.md) de l'objet **Recordset** pour vous assurer que les transactions sont prises en charge. L'appel des méthodes **BeginTrans**, **CommitTrans** ou **Rollback** sur un objet non pris en charge n'a aucun effet.

## <a name="example"></a>Exemple

Cet exemple illustre la propriété **Transactions** dans des espaces de travail Microsoft Access.

```vb 
Sub TransactionsX() 
 
 Dim wrkAcc As Workspace 
 Dim dbsNorthwind As Database 
 Dim conPubs As Connection 
 Dim rstTemp As Recordset 
 
 Set wrkAcc = CreateWorkspace("", "admin", "", dbUseJet) 
 Set dbsNorthwind = wrkAcc.OpenDatabase("Northwind.mdb") 
 
 ' Open two different Recordset objects and display the 
 ' Transactions property of each. 
 
 Debug.Print "Opening Microsoft Access table-type " & _ 
 "recordset..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "Employees", dbOpenTable) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 Debug.Print "Opening forward-only-type " & _ 
 "recordset where the source is an SQL statement..." 
 Set rstTemp = dbsNorthwind.OpenRecordset( _ 
 "SELECT * FROM Employees", dbOpenForwardOnly) 
 Debug.Print " Transactions = " & rstTemp.Transactions 
 
 rstTemp.Close 
 dbsNorthwind.Close 
 conPubs.Close 
 wrkAcc.Close 
End Sub 
 
```

