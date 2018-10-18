---
<span data-ttu-id="23bf8-101"><<<<<<< Titre tête : TOCTitle ActiveCommand propriété-Exemple (VB) : ActiveCommand propriété-Exemple (VB) ms:assetid : 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID : ms.date 48545999 : mtps_ 18/09/2015 version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="23bf8-101"><<<<<<< HEAD title: ActiveCommand Property Example (VB) TOCTitle: ActiveCommand Property Example (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-vb"></a><span data-ttu-id="23bf8-102">ActiveCommand, propriété - Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="23bf8-102">ActiveCommand Property Example (VB)</span></span>
<span data-ttu-id="23bf8-103">=== titre : ActiveCommand, propriété-Exemple (VB) TOCTitle : ActiveCommand propriété-Exemple (VB) ms:assetid : 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID : ms.date 48545999 : 17/10/2018 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="23bf8-103">======= title: ActiveCommand property example (VB) TOCTitle: ActiveCommand property example (VB) ms:assetid: 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID: 48545999 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-example-vb"></a><span data-ttu-id="23bf8-104">ActiveCommand, propriété-Exemple (VB)</span><span class="sxs-lookup"><span data-stu-id="23bf8-104">ActiveCommand property example (VB)</span></span>
>>>>>>> <span data-ttu-id="23bf8-105">master</span><span class="sxs-lookup"><span data-stu-id="23bf8-105">master</span></span>


<span data-ttu-id="23bf8-106">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="23bf8-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23bf8-107">Cet exemple illustre la propriété [ActiveCommand ](activecommand-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="23bf8-107">This example demonstrates the [ActiveCommand](activecommand-property-ado.md) property.</span></span>

<span data-ttu-id="23bf8-108">Une sous-routine comprend un objet [Recordset](recordset-object-ado.md) dont la propriété **ActiveCommand** permet d'afficher le texte et le paramètre de la commande, qui ont servi à créer l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="23bf8-108">A subroutine is given a [Recordset](recordset-object-ado.md) object whose **ActiveCommand** property is used to display the command text and parameter that created the **Recordset**.</span></span>

```vb 
 
'BeginActiveCommandVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim cmd As ADODB.Command 
 Dim rst As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 'record variables 
 Dim strPrompt As String 
 Dim strName As String 
 
 Set Cnxn = New ADODB.Connection 
 Set cmd = New ADODB.Command 
 
 strPrompt = "Enter an author's name (e.g., Ringer): " 
 strName = Trim(InputBox(strPrompt, "ActiveCommandX Example")) 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 'create SQL command string 
 cmd.CommandText = "SELECT * FROM Authors WHERE au_lname = ?" 
 cmd.Parameters.Append cmd.CreateParameter("LastName", adChar, adParamInput, 20, strName) 
 
 Cnxn.Open strCnxn 
 cmd.ActiveConnection = Cnxn 
 
 'create the recordset by executing command string 
 Set rst = cmd.Execute(, , adCmdText) 
 'see the results 
 Call ActiveCommandXprint(rst) 
 
 ' clean up 
 Cnxn.Close 
 Set rst = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rst Is Nothing Then 
 If rst.State = adStateOpen Then rst.Close 
 End If 
 Set rst = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndActiveCommandVB 
```

<span data-ttu-id="23bf8-p101">La routine **ActiveCommandXprint** ne comprend qu'un objet **Recordset** et pourtant, elle doit imprimer le texte et le paramètre de la commande qui ont servi à créer l'objet **Recordset**. Cette opération est possible car la propriété **ActiveCommand** de l'objet **Recordset** donne l'objet [Command](command-object-ado.md) qui lui est associé.</span><span class="sxs-lookup"><span data-stu-id="23bf8-p101">The **ActiveCommandXprint** routine is given only a **Recordset** object, yet it must print the command text and parameter that created the **Recordset**. This can be done because the **Recordset** object's **ActiveCommand** property yields the associated [Command](command-object-ado.md) object.</span></span>

<span data-ttu-id="23bf8-p102">La propriété [CommandText](commandtext-property-ado.md) de l’objet **Command** permet d’obtenir la commande paramétrée, qui a servi à créer l’objet **Recordset**. La collection [Parameters](parameters-collection-ado.md) de l’objet **Command** permet d’obtenir la valeur qui a été substituée à l’espace réservé du paramètre de la commande ("**?**").</span><span class="sxs-lookup"><span data-stu-id="23bf8-p102">The **Command** object's [CommandText](commandtext-property-ado.md) property yields the parameterized command that created the **Recordset**. The **Command** object's [Parameters](parameters-collection-ado.md) collection yields the value that was substituted for the command's parameter placeholder ("**?**").</span></span>

<span data-ttu-id="23bf8-113">Enfin, un message d'erreur ou le nom et l'ID de l'auteur sont imprimés.</span><span class="sxs-lookup"><span data-stu-id="23bf8-113">Finally, an error message or the author's name and ID are printed.</span></span>

```vb 
 
'BeginActiveCommandPrintVB 
Public Sub ActiveCommandXprint(rstp As ADODB.Recordset) 
 
 Dim strName As String 
 
 strName = rstp.ActiveCommand.Parameters.Item("LastName").Value 
 
 Debug.Print "Command text = '"; rstp.ActiveCommand.CommandText; "'" 
 Debug.Print "Parameter = '"; strName; "'" 
 
 If rstp.BOF = True Then 
 Debug.Print "Name = '"; strName; "', not found." 
 Else 
 Debug.Print "Name = '"; rstp!au_fname; " "; rstp!au_lname; _ 
 "', author ID = '"; rstp!au_id; "'" 
 End If 
 
 rstp.Close 
 Set rstp = Nothing 
End Sub 
'EndActiveCommandPrintVB 
```

