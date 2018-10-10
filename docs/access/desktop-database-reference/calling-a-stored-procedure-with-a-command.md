---
title: Appel d'une procédure stockée avec une commande
TOCTitle: Calling a Stored Procedure with a Command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 573b847f53d3fc7ca07691e9a92d152598531bce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470767"
---
# <a name="calling-a-stored-procedure-with-a-command"></a><span data-ttu-id="1f62e-102">Appel d'une procédure stockée avec une commande</span><span class="sxs-lookup"><span data-stu-id="1f62e-102">Calling a Stored Procedure with a Command</span></span>


<span data-ttu-id="1f62e-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f62e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1f62e-p101">Vous pouvez aussi utiliser une commande lorsque vous appelez une procédure stockée. Le code suivant appelle une procédure stockée dans l'exemple de base de données Northwind, appelée CustOrdersOrders, qui est définie comme suit :</span><span class="sxs-lookup"><span data-stu-id="1f62e-p101">You can also use a command when calling a stored procedure. The following code calls a stored procedure in the Northwind sample database, called CustOrdersOrders, which is defined as follows:</span></span>

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

<span data-ttu-id="1f62e-p102">Cette procédure stockée est similaire à la commande utilisée dans [Paramètres de l'objet Command](command-object-parameters.md), dans la mesure où elle prend un paramètre CustomerID et retourne des informations sur les commandes de ce client. Le code suivant utilise cette procédure stockée comme source d'un objet **Recordset** ADO.</span><span class="sxs-lookup"><span data-stu-id="1f62e-p102">This stored procedure is similar to the command used in [Command Object Parameters](command-object-parameters.md), in that it takes a customer ID parameter and returns information about that customer's orders. The code below uses this stored procedure as the source for an ADO **Recordset**.</span></span>

<span data-ttu-id="1f62e-p103">L'utilisation de la procédure stockée vous permet d'accéder à une autre fonctionnalité d'ADO : la méthode **Refresh** de la collection **Parameters**. Grâce à cette méthode, ADO peut remplir automatiquement toutes les informations sur les paramètres requis par la commande, au moment de l'exécution. Cette technique pénalise les performances car ADO doit interroger la source de données pour obtenir des informations sur les paramètres.</span><span class="sxs-lookup"><span data-stu-id="1f62e-p103">Using the stored procedure allows you to access another capability of ADO: the **Parameters** collection **Refresh** method. By using this method, ADO can automatically fill in all information about the parameters required by the command at run time. There is a performance penalty in using this technique, because ADO must query the data source for the information about the parameters.</span></span>

<span data-ttu-id="1f62e-p104">Il existe d'autres différences importantes entre le code suivant et le code illustré dans [Paramètres de l'objet Command](command-object-parameters.md), où les paramètres ont été entrés manuellement. D'une part, ce code n'affecte pas à la propriété **Prepared** la valeur **True** car il s'agit d'une procédure stockée SQL Server, par nature précompilée. D'autre part, la propriété **CommandType** de l'objet **Command** a été affectée de la valeur **adCmdStoredProc** dans le deuxième exemple pour informer ADO que la commande est une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="1f62e-p104">Other important differences exist between the code below and the code in [Command Object Parameters](command-object-parameters.md), where the parameters were entered manually. First, this code does not set the **Prepared** property to **True** because it is a SQL Server stored procedure and is precompiled by definition. Second, the **CommandType** property of the **Command** object changed to **adCmdStoredProc** in the second example to inform ADO that the command was a stored procedure.</span></span>

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

