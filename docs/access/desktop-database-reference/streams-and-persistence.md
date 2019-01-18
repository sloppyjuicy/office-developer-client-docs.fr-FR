---
title: Flux et persistance
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5a6f49368def305964119edcb06b5bcc80c278d2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709305"
---
# <a name="streams-and-persistence"></a>Flux et persistance


**S’applique à**: Access 2013, Office 2013

La méthode [Save](save-method-ado.md) de l’objet [Recordset](recordset-object-ado.md) stocke, ou *persiste*, un objet **Recordset** dans un fichier. La méthode [Open](open-method-ado-recordset.md) restaure, quant à elle, l’objet **Recordset** à partir de ce fichier.

Avec ADO 2.5, les méthodes **Save** et **Open** peuvent également persister un objet **Recordset** dans un objet [Stream](stream-object-ado.md). Cette fonctionnalité est particulièrement utile si vous utilisez RDS (Remote Data Service) et ASP (Active Server Pages).

Pour plus d'informations sur la façon d'utiliser la persistance seule sur les pages ASP, consultez la documentation ASP récente.

Ci-dessous sont présentés quelques scénarios qui montrent comment utiliser les objets **Stream** et la persistance.

## <a name="scenario-1"></a>Scénario 1

Ce scénario enregistre simplement un objet **Recordset** dans un fichier, puis dans un objet **Stream**. Il ouvre ensuite le flux persistant dans un autre objet **Recordset**.

```vb 
 
Dim rs1 As ADODB.Recordset 
Dim rs2 As ADODB.Recordset 
Dim stm As ADODB.Stream 
 
Set rs1 = New ADODB.Recordset 
Set rs2 = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
rs1.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""", adopenStatic, adLockReadOnly, adCmdText 
rs1.Save "c:\myfolder\mysubfolder\myrs.xml", adPersistXML 
rs1.Save stm, adPersistXML 
rs2.Open stm 
```

## <a name="scenario-2"></a>Scénario 2

Ce scénario rend un objet **Recordset** persistant dans un objet **Stream** au format XML. Il lit ensuite l'objet **Stream** dans une chaîne que vous pouvez consulter, manipuler et afficher.

```vb 
 
Dim rs As ADODB.Recordset 
Dim stm As ADODB.Stream 
Dim strRst As String 
 
Set rs = New ADODB.Recordset 
Set stm = New ADODB.Stream 
 
' Open, save, and close the recordset. 
rs.Open "SELECT * FROM Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
rs.Save stm, adPersistXML 
rs.Close 
Set rs = nothing 
 
' Put saved Recordset into a string variable. 
strRst = stm.ReadText(adReadAll) 
 
' Examine, manipulate, or display the XML data. 
... 
```

## <a name="scenario-3"></a>Scénario 3

Cet exemple de code montre comment le code ASP persiste un objet **Recordset** au format XML directement dans l'objet **Response**:

```vb 
 
... 
<% 
response.ContentType = "text/xml" 
 
' Create and open a Recordset. 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select * from Customers", "Provider=sqloledb;" & _ 
 "Data Source=MyServer;Initial Catalog=Northwind;" & _ 
 "Integrated Security=SSPI;""" 
 
' Save Recordset directly into output stream. 
rs.Save Response, adPersistXML 
 
' Close Recordset. 
rs.Close 
Set rs = nothing 
%> 
... 
```

## <a name="scenario-4"></a>Scénario 4

Dans ce scénario, le code ASP écrit le contenu de l'objet **Recordset** au format ADTG sur le client. Le [service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) peut utiliser ces données pour créer un objet **Recordset** déconnecté.

Une nouvelle propriété de l'objet [DataControl](datacontrol-object-rds.md) RDS, [URL](url-property-rds.md), pointe vers la page .asp qui génère l'objet **Recordset**. En d'autres termes, il est possible d'obtenir un objet **Recordset** sans que RDS fasse appel à l'objet [DataFactory](datafactory-object-rdsserver.md) côté serveur ou que l'utilisateur crée un objet métier. Cela simplifie considérablement le modèle de programmation RDS.

Code côté serveur, appelé https://server/directory/recordset.asp: :

```vb 
 
<% 
Dim rs 
Set rs = Server.CreateObject("ADODB.Recordset") 
rs.Open "select au_fname, au_lname, phone from Authors", ""& _ 
 "Provider=sqloledb;Data Source=MyServer;" & _ 
 "Initial Catalog=Pubs;Integrated Security=SSPI;" 
response.ContentType = "multipart/mixed" 
rs.Save response, adPersistADTG 
%> 
```

Code côté client :

```html 
 
<HTML> 
<HEAD> 
<TITLE>RDS Query Page</TITLE> 
</HEAD> 
<body> 
<CENTER> 
<H1>Remote Data Service 2.5</H1> 
<TABLE DATASRC="#DC1"> 
 <TR> 
 <TD><SPAN DATAFLD="au_fname"></SPAN></TD> 
 <TD><SPAN DATAFLD="au_lname"></SPAN></TD> 
 <TD><SPAN DATAFLD="phone"></SPAN></TD> 
 </TR> 
</TABLE> 

<BR> 
 
<OBJECT classid="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
 ID=DC1 HEIGHT=1 WIDTH = 1> 
 <PARAM NAME="URL" VALUE="https://server/directory/recordset.asp"> 
</OBJECT> 
 
</SCRIPT> 
</BODY> 
</HTML> 
```

Les développeurs peuvent également utiliser l'objet **Recordset** sur le client :

```vb
... 
function GetRs() 
 { 
 rs = CreateObject("ADODB.Recordset"); 
 rs.Open "https://server/directory/recordset.asp" 
 DC1.SourceRecordset = rs; 
 } 
... 
```

