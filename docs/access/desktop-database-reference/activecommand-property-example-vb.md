---
<<<<<<< Titre tête : TOCTitle ActiveCommand propriété-Exemple (VB) : ActiveCommand propriété-Exemple (VB) ms:assetid : 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID : ms.date 48545999 : mtps_ 18/09/2015 version : v=office.15
---

# <a name="activecommand-property-example-vb"></a>ActiveCommand, propriété - Exemple (VB)
=== titre : ActiveCommand, propriété-Exemple (VB) TOCTitle : ActiveCommand propriété-Exemple (VB) ms:assetid : 831032cb-d557-aa98-5637-07bad65f924a ms:mtpsurl : https://msdn.microsoft.com/library/JJ249569(v=office.15) ms:contentKeyID : ms.date 48545999 : 17/10/2018 mtps_version : v=office.15
---

# <a name="activecommand-property-example-vb"></a>ActiveCommand, propriété-Exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Cet exemple illustre la propriété [ActiveCommand ](activecommand-property-ado.md).

Une sous-routine comprend un objet [Recordset](recordset-object-ado.md) dont la propriété **ActiveCommand** permet d'afficher le texte et le paramètre de la commande, qui ont servi à créer l'objet **Recordset**.

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

La routine **ActiveCommandXprint** ne comprend qu'un objet **Recordset** et pourtant, elle doit imprimer le texte et le paramètre de la commande qui ont servi à créer l'objet **Recordset**. Cette opération est possible car la propriété **ActiveCommand** de l'objet **Recordset** donne l'objet [Command](command-object-ado.md) qui lui est associé.

La propriété [CommandText](commandtext-property-ado.md) de l’objet **Command** permet d’obtenir la commande paramétrée, qui a servi à créer l’objet **Recordset**. La collection [Parameters](parameters-collection-ado.md) de l’objet **Command** permet d’obtenir la valeur qui a été substituée à l’espace réservé du paramètre de la commande ("**?**").

Enfin, un message d'erreur ou le nom et l'ID de l'auteur sont imprimés.

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

