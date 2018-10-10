---
title: 'Étape 6 : les modifications sont envoyées au serveur (didacticiel RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d26ca621ba7102dc0f9c6219ba3a16b28138770f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470563"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a><span data-ttu-id="0c2cf-102">Étape 6 : les modifications sont envoyées au serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="0c2cf-102">Step 6: Changes are Sent to the Server (RDS Tutorial)</span></span>


<span data-ttu-id="0c2cf-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0c2cf-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0c2cf-104">Si l'objet **Recordset** est modifié, les modifications correspondantes (p. ex., lignes ajoutées, modifiées ou supprimées) peuvent être renvoyées au serveur.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-104">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0c2cf-p101">Le comportement par défaut de RDS peut être appelé implicitement avec les objets ADO et le fournisseur d'accès à distance Microsoft OLE DB. Les requêtes peuvent retourner des objets <STRONG>Recordset</STRONG> et les objets <STRONG>Recordset</STRONG> modifiés peuvent mettre à jour la source de données. Ce didacticiel n'appelle pas RDS avec les objets ADO, mais, si c'était le cas, voici comment se présenterait le code :</span><span class="sxs-lookup"><span data-stu-id="0c2cf-p101">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider. Queries can return <STRONG>Recordset</STRONG>s, and edited <STRONG>Recordset</STRONG>s can update the data source. This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span></P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

<span data-ttu-id="0c2cf-108">**Partie A**</span><span class="sxs-lookup"><span data-stu-id="0c2cf-108">**Part A**</span></span> 

<span data-ttu-id="0c2cf-109">Supposons dans cet exemple que vous avez utilisé uniquement la [RDS. DataControl](datacontrol-object-rds.md) et qu’un objet **Recordset** est maintenant associé à la **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-109">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="0c2cf-110">La méthode [SubmitChanges](submitchanges-method-rds.md) met à jour la source de données en fonction des modifications apportées à l'objet **Recordset** si les propriétés [Server](server-property-rds.md) et [Connect](connect-property-rds.md) sont toujours définies.</span><span class="sxs-lookup"><span data-stu-id="0c2cf-110">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

```vb 
 
Sub RDSTutorial6A() 
Dim DC as New RDS.DataControl 
Dim RS as ADODB.Recordset 
DC.Server = "https://yourServer" 
DC.Connect = "DSN=Pubs" 
DC.SQL = "SELECT * FROM Authors" 
DC.Refresh 
... 
Set RS = DC.Recordset 
 ' Edit the Recordset. 
... 
DC.SubmitChanges 
... 
```

<span data-ttu-id="0c2cf-111">**Partie B**</span><span class="sxs-lookup"><span data-stu-id="0c2cf-111">**Part B**</span></span> 

<span data-ttu-id="0c2cf-112">Vous pouvez également vous pourriez mettre à jour le serveur avec l’objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) , définissant une connexion et un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="0c2cf-112">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

```vb 
 
Sub RDSTutorial6B() 
Dim DS As New RDS.DataSpace 
Dim RS As ADODB.Recordset 
Dim DC As New RDS.DataControl 
Dim DF As Object 
Dim blnStatus As Boolean 
Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
 ' Edit the Recordset. 
blnStatus = DF.SubmitChanges "DSN=Pubs", RS 
End Sub 
```

<span data-ttu-id="0c2cf-113">**Fin du didacticiel.**</span><span class="sxs-lookup"><span data-stu-id="0c2cf-113">**This is the end of the tutorial.**</span></span>

