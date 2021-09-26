---
title: Open et Close, méthodes – Exemple (VBScript)
TOCTitle: Open and Close methods example (VBScript)
ms:assetid: 7b9d9443-9693-8738-7c93-52f9efc895ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249513(v=office.15)
ms:contentKeyID: 48545816
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ca39bacafea3f8100a35e98a56af2cf4bd959257
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622157"
---
# <a name="open-and-close-methods-example-vbscript"></a>Open et Close, méthodes – Exemple (VBScript)


**S’applique à** : Access 2013, Office 2013

Cet exemple utilise les méthodes [Open](open-method-ado-recordset.md) et [Close](close-method-ado.md) sur des objets [Recordset](recordset-object-ado.md) et [Connection](connection-object-ado.md) qui ont été ouverts.

Utilisez l'exemple suivant dans une page ASP (Active Server Page). Utilisez **Rechercher** pour localiser le fichier Adovbs.inc et placez-le dans le répertoire que vous avez l'intention d'utiliser. Coupez et collez le code suivant dans le Bloc-notes ou un autre éditeur de texte et enregistrez-le sous **OpenVBS.asp**. Vous pouvez consulter le résultat dans n'importe quel navigateur.

```vb 
 
<!-- BeginOpenVBS --> 
<%@ Language=VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<META name="VI60_DefaultClientScript"  content=VBScript> 
<META NAME="GENERATOR" Content="Microsoft Visual Studio 6.0"> 
<title>ADO Open Method</title> 
<STYLE> 
<!-- 
BODY { 
   font-family: 'Verdana','Arial','Helvetica',sans-serif; 
   BACKGROUND-COLOR:white; 
   COLOR:black; 
    } 
.thead { 
   background-color: #008080;  
   font-family: 'Verdana','Arial','Helvetica',sans-serif;  
   font-size: x-small; 
   color: white; 
   } 
.thead2 { 
   background-color: #800000;  
   font-family: 'Verdana','Arial','Helvetica',sans-serif;  
   font-size: x-small; 
   color: white; 
   } 
.tbody {  
   text-align: center; 
   background-color: #f7efde; 
   font-family: 'Verdana','Arial','Helvetica',sans-serif;  
   font-size: x-small; 
    } 
--> 
</STYLE> 
</HEAD> 
 
<BODY> 
<H3>ADO Open Method</H3> 
 
<TABLE WIDTH=600 BORDER=0> 
<TR> 
<TD VALIGN=TOP COLSPAN=3> 
<FONT SIZE=2> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim rsProducts, strSQLProducts 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
 
    Cnxn.Open strCnxn 
         
    ' create and open first Recordset using Connection - execute 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "SELECT CompanyName, ContactName, City FROM Customers" 
    Set rsCustomers = Cnxn.Execute(strSQLCustomers)  
 
    ' create and open second Recordset using recordset - open 
    Set rsProducts = Server.CreateObject("ADODB.Recordset") 
    strSQLProducts = "SELECT ProductName, UnitPrice FROM Products" 
    rsProducts.Open strSQLProducts, Cnxn, adOpenDynamic, adLockPessimistic, adCmdText 
    %> 
 
    <TABLE COLSPAN=8 CELLPADDING=5 BORDER=0> 
    <!-- BEGIN column header row for Customer Table--> 
    <TR CLASS=thead> 
       <TD>Company Name</TD> 
       <TD>Contact Name</TD> 
       <TD>City</TD> 
    </TR> 
 
    <!--Display ADO Data from Customer Table--> 
    <% Do Until rsCustomers.EOF %> 
    <TR CLASS=tbody> 
      <TD> <%=rsCustomers("CompanyName")%> </TD> 
      <TD> <%=rsCustomers("ContactName")%></TD> 
      <TD> <%=rsCustomers("City")%> </TD> 
    </TR>  
    <%rsCustomers.MoveNext  
    Loop  
    %> 
    </TABLE> 
 
    <HR> 
 
    <TABLE COLSPAN=8 CELLPADDING=5 BORDER=0> 
    <!-- BEGIN column header row for Product List Table--> 
 
    <TR CLASS=thead2> 
       <TD>Product Name</TD> 
       <TD>Unit Price</TD> 
    </TR> 
    <!-- Display ADO Data Product List--> 
    <% Do Until rsProducts.EOF %> 
      <TR CLASS=tbody>   
      <TD> <%=rsProducts("ProductName")%> </TD> 
      <TD> <%=rsProducts("UnitPrice")%> </TD> 
      </TR> 
      <!--  Next Row = Record --> 
    <%rsProducts.MoveNext  
    Loop  
 
    ' clean up 
    If rsProducts.State = adStateOpen then 
        rsProducts.Close 
    End If 
    If rsCustomers.State = adStateOpen then 
        rsCustomers.Close 
    End If 
    If Cnxn.State = adStateOpen then 
        Cnxn.Close 
    End If 
    Set rsProducts = Nothing 
    Set rsCustomers = Nothing 
    Set Cnxn = Nothing 
 
    %> 
    </TABLE> 
 
</BODY> 
</HTML> 
<!-- EndOpenVBS --> 
```

