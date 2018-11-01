---
title: Flux et persistance
TOCTitle: Streams and Persistence
ms:assetid: 564fc098-52bf-77d7-9d48-75186483e3fe
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249289(v=office.15)
ms:contentKeyID: 48544949
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65fda92e28aab278fde4dafba4e94c576827370a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881747"
---
# <a name="streams-and-persistence"></a><span data-ttu-id="f35d7-102">Flux et persistance</span><span class="sxs-lookup"><span data-stu-id="f35d7-102">Streams and Persistence</span></span>


<span data-ttu-id="f35d7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f35d7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f35d7-104">La méthode [Save](save-method-ado.md) de l’objet [Recordset](recordset-object-ado.md) stocke, ou *persiste*, un objet **Recordset** dans un fichier. La méthode [Open](open-method-ado-recordset.md) restaure, quant à elle, l’objet **Recordset** à partir de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="f35d7-104">The [Recordset](recordset-object-ado.md) object [Save](save-method-ado.md) method stores, or *persists*, a **Recordset** in a file, and the [Open](open-method-ado-recordset.md) method restores the **Recordset** from that file.</span></span>

<span data-ttu-id="f35d7-p101">Avec ADO 2.5, les méthodes **Save** et **Open** peuvent également persister un objet **Recordset** dans un objet [Stream](stream-object-ado.md). Cette fonctionnalité est particulièrement utile si vous utilisez RDS (Remote Data Service) et ASP (Active Server Pages).</span><span class="sxs-lookup"><span data-stu-id="f35d7-p101">With ADO 2.5, the **Save** and **Open** methods can persist a **Recordset** to a [Stream](stream-object-ado.md) object as well. This feature is especially useful when working with Remote Data Service (RDS) and Active Server Pages (ASP).</span></span>

<span data-ttu-id="f35d7-107">Pour plus d'informations sur la façon d'utiliser la persistance seule sur les pages ASP, consultez la documentation ASP récente.</span><span class="sxs-lookup"><span data-stu-id="f35d7-107">For more information about how persistence can be used by itself on ASP pages, see the current ASP documentation.</span></span>

<span data-ttu-id="f35d7-108">Ci-dessous sont présentés quelques scénarios qui montrent comment utiliser les objets **Stream** et la persistance.</span><span class="sxs-lookup"><span data-stu-id="f35d7-108">The following are a few scenarios that show how **Stream** objects and persistence can be used.</span></span>

## <a name="scenario-1"></a><span data-ttu-id="f35d7-109">Scénario 1</span><span class="sxs-lookup"><span data-stu-id="f35d7-109">Scenario 1</span></span>

<span data-ttu-id="f35d7-p102">Ce scénario enregistre simplement un objet **Recordset** dans un fichier, puis dans un objet **Stream**. Il ouvre ensuite le flux persistant dans un autre objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="f35d7-p102">This scenario simply saves a **Recordset** to a file and then to a **Stream**. It then opens the persisted stream into another **Recordset**.</span></span>

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

## <a name="scenario-2"></a><span data-ttu-id="f35d7-112">Scénario 2</span><span class="sxs-lookup"><span data-stu-id="f35d7-112">Scenario 2</span></span>

<span data-ttu-id="f35d7-p103">Ce scénario rend un objet **Recordset** persistant dans un objet **Stream** au format XML. Il lit ensuite l'objet **Stream** dans une chaîne que vous pouvez consulter, manipuler et afficher.</span><span class="sxs-lookup"><span data-stu-id="f35d7-p103">This scenario persists a **Recordset** into a **Stream** in XML format. It then reads the **Stream** into a string that you can examine, manipulate, or display.</span></span>

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

## <a name="scenario-3"></a><span data-ttu-id="f35d7-115">Scénario 3</span><span class="sxs-lookup"><span data-stu-id="f35d7-115">Scenario 3</span></span>

<span data-ttu-id="f35d7-116">Cet exemple de code montre comment le code ASP persiste un objet **Recordset** au format XML directement dans l'objet **Response**:</span><span class="sxs-lookup"><span data-stu-id="f35d7-116">This example code shows ASP code persisting a **Recordset** as XML directly to the **Response** object:</span></span>

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

## <a name="scenario-4"></a><span data-ttu-id="f35d7-117">Scénario 4</span><span class="sxs-lookup"><span data-stu-id="f35d7-117">Scenario 4</span></span>

<span data-ttu-id="f35d7-p104">Dans ce scénario, le code ASP écrit le contenu de l'objet **Recordset** au format ADTG sur le client. Le [service de curseur Microsoft pour OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) peut utiliser ces données pour créer un objet **Recordset** déconnecté.</span><span class="sxs-lookup"><span data-stu-id="f35d7-p104">In this scenario, ASP code writes the contents of the **Recordset** in ADTG format to the client. The [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) can use this data to create a disconnected **Recordset**.</span></span>

<span data-ttu-id="f35d7-p105">Une nouvelle propriété de l'objet [DataControl](datacontrol-object-rds.md) RDS, [URL](url-property-rds.md), pointe vers la page .asp qui génère l'objet **Recordset**. En d'autres termes, il est possible d'obtenir un objet **Recordset** sans que RDS fasse appel à l'objet [DataFactory](datafactory-object-rdsserver.md) côté serveur ou que l'utilisateur crée un objet métier. Cela simplifie considérablement le modèle de programmation RDS.</span><span class="sxs-lookup"><span data-stu-id="f35d7-p105">A new property on the RDS [DataControl](datacontrol-object-rds.md), [URL](url-property-rds.md), points to the .asp page that generates the **Recordset**. This means a **Recordset** object can be obtained without RDS using the server-side [DataFactory](datafactory-object-rdsserver.md) object or the user writing a business object. This simplifies the RDS programming model significantly.</span></span>

<span data-ttu-id="f35d7-123">Code côté serveur, appelé https://server/directory/recordset.asp: :</span><span class="sxs-lookup"><span data-stu-id="f35d7-123">Server-side code, named https://server/directory/recordset.asp:</span></span>

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

<span data-ttu-id="f35d7-124">Code côté client :</span><span class="sxs-lookup"><span data-stu-id="f35d7-124">Client-side code:</span></span>

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

<span data-ttu-id="f35d7-125">Les développeurs peuvent également utiliser l'objet **Recordset** sur le client :</span><span class="sxs-lookup"><span data-stu-id="f35d7-125">Developers also have the option of using a **Recordset** object on the client:</span></span>

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

