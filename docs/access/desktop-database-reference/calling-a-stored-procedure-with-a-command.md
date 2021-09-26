---
title: Appel d’une procédure stockée à l’aide d’une commande
TOCTitle: Calling a stored procedure with a command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2bb56f998a6508b3a30c1efa45270c296aa80540
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607030"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Appel d’une procédure stockée à l’aide d’une commande


**S’applique à** : Access 2013, Office 2013

Vous pouvez aussi utiliser une commande lorsque vous appelez une procédure stockée. Le code suivant appelle une procédure stockée dans l'exemple de base de données Northwind, appelée CustOrdersOrders, qui est définie comme suit :

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Cette procédure stockée est similaire à la commande utilisée dans [Paramètres de l'objet Command](command-object-parameters.md), dans la mesure où elle prend un paramètre CustomerID et retourne des informations sur les commandes de ce client. Le code suivant utilise cette procédure stockée comme source d'un objet **Recordset** ADO.

L'utilisation de la procédure stockée vous permet d'accéder à une autre fonctionnalité d'ADO : la méthode **Refresh** de la collection **Parameters**. Grâce à cette méthode, ADO peut remplir automatiquement toutes les informations sur les paramètres requis par la commande, au moment de l'exécution. Cette technique pénalise les performances car ADO doit interroger la source de données pour obtenir des informations sur les paramètres.

Il existe d'autres différences importantes entre le code suivant et le code illustré dans [Paramètres de l'objet Command](command-object-parameters.md), où les paramètres ont été entrés manuellement. D'une part, ce code n'affecte pas à la propriété **Prepared** la valeur **True** car il s'agit d'une procédure stockée SQL Server, par nature précompilée. D'autre part, la propriété **CommandType** de l'objet **Command** a été affectée de la valeur **adCmdStoredProc** dans le deuxième exemple pour informer ADO que la commande est une procédure stockée.

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndAutoParamCmd 
```

