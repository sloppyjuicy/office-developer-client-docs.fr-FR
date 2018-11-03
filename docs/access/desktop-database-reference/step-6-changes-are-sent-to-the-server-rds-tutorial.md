---
title: 'Étape 6 : les modifications sont envoyées au serveur (didacticiel RDS)'
TOCTitle: 'Step 6: Changes are Sent to the Server (RDS Tutorial)'
ms:assetid: c5915d89-77b6-bb3f-a962-49378160751f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249965(v=office.15)
ms:contentKeyID: 48547611
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c8677428c32c70bc11b9eef6f168b09c72592a0b
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944248"
---
# <a name="step-6-changes-are-sent-to-the-server-rds-tutorial"></a>Étape 6 : Les modifications sont envoyées au serveur (didacticiel RDS)


**S’applique à**: Access 2013, Office 2013

Si l'objet **Recordset** est modifié, les modifications correspondantes (p. ex., lignes ajoutées, modifiées ou supprimées) peuvent être renvoyées au serveur.


> [!NOTE]
> <P>Le comportement par défaut de RDS peut être appelé implicitement avec les objets ADO et le fournisseur d'accès à distance Microsoft OLE DB. Les requêtes peuvent retourner des objets <STRONG>Recordset</STRONG> et les objets <STRONG>Recordset</STRONG> modifiés peuvent mettre à jour la source de données. Ce didacticiel n'appelle pas RDS avec les objets ADO, mais, si c'était le cas, voici comment se présenterait le code :</P>



```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

**Partie A** 

Supposons dans cet exemple que vous avez utilisé uniquement la [RDS. DataControl](datacontrol-object-rds.md) et qu’un objet **Recordset** est maintenant associé à la **RDS. DataControl**. La méthode [SubmitChanges](submitchanges-method-rds.md) met à jour la source de données en fonction des modifications apportées à l'objet **Recordset** si les propriétés [Server](server-property-rds.md) et [Connect](connect-property-rds.md) sont toujours définies.

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

**Partie B** 

Vous pouvez également vous pourriez mettre à jour le serveur avec l’objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) , définissant une connexion et un objet **Recordset** .

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

**Fin du didacticiel.**

