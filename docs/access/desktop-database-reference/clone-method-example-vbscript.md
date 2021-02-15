---
title: Clone, méthode – Exemple (VBScript)
TOCTitle: Clone method example (VBScript)
ms:assetid: b9d49eb9-8da8-dfd2-1c59-35ac70969850
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249893(v=office.15)
ms:contentKeyID: 48547357
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1fc3341f4ec662c17e2a7c274b1cc3af215c877c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296331"
---
# <a name="clone-method-example-vbscript"></a><span data-ttu-id="a5293-102">Clone, méthode – Exemple (VBScript)</span><span class="sxs-lookup"><span data-stu-id="a5293-102">Clone method example (VBScript)</span></span>


<span data-ttu-id="a5293-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a5293-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a5293-104">Cet exemple utilise la méthode [Clone](clone-method-ado.md) pour créer des copies d'un objet [Recordset](recordset-object-ado.md) puis permet à l'utilisateur de positionner le pointeur d'enregistrement de chaque copie indépendamment des autres.</span><span class="sxs-lookup"><span data-stu-id="a5293-104">This example uses the [Clone](clone-method-ado.md) method to create copies of a [Recordset](recordset-object-ado.md) and then lets the user position the record pointer of each copy independently.</span></span>

<span data-ttu-id="a5293-p101">Utilisez l'exemple suivant dans une page ASP (Active Server Page). Cet exemple utilise la base de données Northwind (Les Comptoirs) distribuée avec Microsoft Access. Coupez le code suivant, collez-le dans le Bloc-notes ou dans un autre éditeur de texte, puis enregistrez-le sous le nom **CloneVBS.asp**. Vous pouvez afficher le résultat dans un navigateur client.</span><span class="sxs-lookup"><span data-stu-id="a5293-p101">Use the following example in an Active Server Page (ASP). This example uses the Northwind database distributed with Microsoft Access. Cut and paste the following code to Notepad or another text editor and save it as **CloneVBS.asp**. You can view the result in any client browser.</span></span>

<span data-ttu-id="a5293-109">Pour exercer cet exemple, modifiez la ligne RsCustomerList.Source = « Customers » en RsCustomerList.Source = « Products » pour compter une table plus grande.</span><span class="sxs-lookup"><span data-stu-id="a5293-109">To exercise the example, change the line RsCustomerList.Source = "Customers" to to RsCustomerList.Source = "Products" to count a larger table.</span></span>

```vb 
 
<!-- BeginCloneVBS --> 
<% Language = VBScript %> 
<%' use this meta tag instead of adovbs.inc%> 
<!--METADATA TYPE="typelib" uuid="00000205-0000-0010-8000-00AA006D2EA4" --> 
<HTML> 
<HEAD> 
<TITLE>ADO Clone Method</TITLE> 
</HEAD> 
 
<BODY> 
 
<H1 align="center">ADO Clone Method</H1> 
<HR> 
<% ' to integrate/test this code replace the  
   ' Data Source value in the Connection string%> 
<%  
    ' connection and recordset variables 
    Dim Cnxn, strCnxn 
    Dim rsCustomers, strSQLCustomers 
    Dim rsFirst, rsLast, rsCount 
    Dim rsClone 
    Dim CloneFirst, CloneLast, CloneCount 
 
    ' open connection 
    Set Cnxn = Server.CreateObject("ADODB.Connection") 
    strCnxn = "Provider='sqloledb';Data Source=" & _ 
            Request.ServerVariables("SERVER_NAME") & ";" & _ 
            "Integrated Security='SSPI';Initial Catalog='Northwind';" 
    Cnxn.Open strCnxn 
         
    ' create and open Recordset using object refs 
    Set rsCustomers = Server.CreateObject("ADODB.Recordset") 
    strSQLCustomers = "Customers" 
     
    rsCustomers.ActiveConnection = Cnxn 
    rsCustomers.CursorLocation = adUseClient 
    rsCustomers.CursorType = adOpenKeyset 
    rsCustomers.LockType = adLockOptimistic 
    rsCustomers.Source = strSQLCustomers 
    rsCustomers.Open 
 
    rsCustomers.MoveFirst 
    rsCount = rsCustomers.RecordCount 
    rsFirst = rsCustomers("CompanyName") 
    rsCustomers.MoveLast 
    rsLast = rsCustomers("CompanyName") 
 
    ' create clone 
    Set rsClone = rsCustomers.Clone 
    rsClone.MoveFirst 
    CloneCount = rsClone.RecordCount 
    CloneFirst = rsClone("CompanyName") 
    rsClone.MoveLast 
    CloneLast = rsClone("CompanyName") 
%> 
 
<!-- Display Results --> 
<H3>There Are <%=rsCount%> Records in the original recordset</H3> 
<H3>The first record is <%=rsFirst%> and the last record is <%=rsLast%></H3> 
<BR><HR> 
<H3>There Are <%=CloneCount%> Records in the original recordset</H3> 
<H3>The first record is <%=CloneFirst%> and the last record is <%=CloneLast%></H3> 
<BR><HR> 
<H4>Location of OLEDB Database</H4> 
 
<% 
    ' Show location of DSN data source 
    Response.Write(Cnxn) 
 
    ' Clean up 
    If rsCustomers.State = adStateOpen then 
       rsCustomers.Close 
    End If 
    If rsClone.State = adStateOpen then 
       rsClone.Close 
    End If 
    If Cnxn.State = adStateOpen then 
       Cnxn.Close 
    End If 
    Set rsCustomers = Nothing 
    Set rsClone = Nothing 
    Set Cnxn = Nothing 
%> 
</BODY> 
</HTML> 
<!-- EndCloneVBS --> 
 
```

