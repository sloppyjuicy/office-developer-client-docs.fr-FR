---
title: 'Étape 2 : appeler le programme serveur (didacticiel RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edd9f8561e6275e3b8eb33e86be745345d7c797a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472118"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a>Étape 2 : appeler le programme serveur (didacticiel RDS)


**S’applique à**: Access 2013 | Office 2013

Lorsque vous appelez une méthode sur le *proxy* client, c'est le programme serveur qui exécute cette méthode. Au cours de cette étape, vous allez exécuter une requête sur le serveur.

**Partie A** Si vous n’utilisiez [RDSServer.DataFactory](datafactory-object-rdsserver.md) dans ce didacticiel, le moyen le plus pratique pour effectuer cette étape consisterait à utiliser le [RDS. DataControl](datacontrol-object-rds.md) objet. **RDS.DataControl** combine l'étape précédente de création d'un proxy, et celle-ci, qui consiste à émettre une requête.

Définissez la propriété **Server** de l'objet [RDS.DataControl](server-property-rds.md) pour déterminer l'emplacement au niveau duquel le programme serveur doit être instancié, la propriété [Connect](connect-property-rds.md) pour spécifier la chaîne de connexion permettant d'accéder à la source de données et la propriété [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) pour spécifier le texte de la commande de requête. Exécutez ensuite la méthode [Refresh](refresh-method-rds.md) pour forcer le programme serveur à se connecter à la source de données, récupérer les lignes spécifiées par la requête et retourner un objet **Recordset** au client.

Ce didacticiel n'utilise pas l'objet **RDS.DataControl**, mais, si c'était le cas, le code ressemblerait à ce qui suit :

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

De même, le didacticiel n'appelle pas RDS avec les objets ADO, mais voici comment se présenterait le code dans le cas contraire :

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

**Partie B** La méthode générale d’effectuer cette étape consiste à appeler la méthode [Query](query-method-rds.md) de l’objet **RDSServer.DataFactory** . Cette méthode prend une chaîne de connexion, utilisée pour établir la connexion à une source de données, et un texte de commande, pour spécifier les lignes à retourner par la source de données.

Ce didacticiel utilise la méthode **Query** de l'objet **DataFactory**:

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

