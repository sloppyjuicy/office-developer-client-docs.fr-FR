---
title: Paramètres de l'objet Command
TOCTitle: Command Object Parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3ce61f514e174595a458f66ea0a6c671ce5a9dc
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880172"
---
# <a name="command-object-parameters"></a><span data-ttu-id="adc22-102">Paramètres de l'objet Command</span><span class="sxs-lookup"><span data-stu-id="adc22-102">Command Object Parameters</span></span>


<span data-ttu-id="adc22-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="adc22-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adc22-p101">L'exemple suivant illustre une utilisation plus intéressante de l'objet **Command**. En effet, le texte de la commande SQL y a été modifié pour le rendre paramétrable. Il est donc possible de réutiliser la commande, en passant une autre valeur pour le paramètre à chaque nouvelle opération. Étant donné que la propriété **Prepared** de l'objet **Command** est égale à **True**, ADO exige du fournisseur qu'il compile la commande spécifiée dans **CommandText** avant sa première exécution. Il conserve également la commande compilée en mémoire. La première exécution de la commande est légèrement ralentie en raison de la charge de traitement imposée par sa préparation. Toutefois, les performances sont améliorées par la suite, à chaque nouvel appel de la commande. En d'autres termes, les commandes doivent être préparées uniquement si vous comptez les utiliser plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="adc22-p101">A more interesting use for the **Command** object is shown in the next example, in which the text of the SQL command has been modified to make it parameterized. This makes it possible to reuse the command, passing in a different value for the parameter each time. Because the **Prepared** property on the **Command** object is set equal to **True**, ADO will require the provider to compile the command specified in **CommandText** before executing it for the first time. It also will retain the compiled command in memory. This slows the execution of the command slightly the first time it is executed because of the overhead required to prepare it, but results in a performance gain each time the command is called thereafter. Thus, commands should be prepared only if they will be used more than once.</span></span>

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
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
'EndManualParamCmd 
```

<span data-ttu-id="adc22-p102">Tous les fournisseurs ne prennent pas en charge les commandes préparées. Si c'est le cas de votre fournisseur, il peut retourner une erreur dès que cette propriété a la valeur **True**. S'il ne retourne pas d'erreur, il ignore la demande de préparation de la commande et affecte à la propriété **Prepared** la valeur **False**.</span><span class="sxs-lookup"><span data-stu-id="adc22-p102">Not all providers support prepared commands. If the provider does not support command preparation, it might return an error as soon as this property is set to **True**. If it does not return an error, it ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

