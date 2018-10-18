---
<<<<<<< Titre tête : TOCTitle Version propriété-Exemple (VB) : Version propriété-Exemple (VB) === titre : Version, propriété-Exemple (VB) TOCTitle : Version, propriété-Exemple (VB)
>>>>>>> Master ms:assetid : ffb7b04a-55b9-fa2f-41ec-44af225bd15f ms:mtpsurl : https://msdn.microsoft.com/library/JJ250315(v=office.15) ms:contentKeyID : ms.date 48548968 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="version-property-example-vb"></a>Version, propriété - Exemple (VB)
=======
# <a name="version-property-example-vb"></a>Version, propriété-Exemple (VB)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Cet exemple utilise la propriété [Version](version-property-ado.md) d'un objet [Connection](connection-object-ado.md) pour afficher la version ADO actuelle. Il utilise aussi plusieurs propriétés dynamiques pour afficher :

  - le nom et la version du SGBD,

  - la version d'OLE DB,

  - le nom et la version du fournisseur,

  - la version d'ODBC,

  - le nom et la version du pilote ODBC.

<!-- end list -->

```vb 
 
'BeginVersionVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim strVersionInfo As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 strVersionInfo = "ADO Version: " & Cnxn.Version & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Name: " & Cnxn.Properties("DBMS Name") & vbCr 
 strVersionInfo = strVersionInfo & "DBMS Version: " & Cnxn.Properties("DBMS Version") & vbCr 
 strVersionInfo = strVersionInfo & "OLE DB Version: " & Cnxn.Properties("OLE DB Version") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Name: " & Cnxn.Properties("Provider Name") & vbCr 
 strVersionInfo = strVersionInfo & "Provider Version: " & Cnxn.Properties("Provider Version") & vbCr 
 
 MsgBox strVersionInfo 
 
 ' clean up 
 Cnxn.Close 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndVersionVB 
```

