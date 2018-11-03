---
title: 'Étape 2 : appeler le programme serveur (didacticiel RDS)'
TOCTitle: 'Step 2: Invoke the Server Program (RDS Tutorial)'
ms:assetid: 45429faa-c1e2-d448-a5b4-b2d77cb94377
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249211(v=office.15)
ms:contentKeyID: 48544549
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d3264c58434bf7af6ae4e75c249a7009f39b7d4
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25947230"
---
# <a name="step-2-invoke-the-server-program-rds-tutorial"></a><span data-ttu-id="ff5b1-102">Étape 2 : Appeler le programme serveur (didacticiel RDS)</span><span class="sxs-lookup"><span data-stu-id="ff5b1-102">Step 2: Invoke the server program (RDS Tutorial)</span></span>

<span data-ttu-id="ff5b1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff5b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff5b1-p101">Lorsque vous appelez une méthode sur le *proxy* client, c'est le programme serveur qui exécute cette méthode. Au cours de cette étape, vous allez exécuter une requête sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-p101">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

<span data-ttu-id="ff5b1-106">**Partie A** Si vous n’utilisiez [RDSServer.DataFactory](datafactory-object-rdsserver.md) dans ce didacticiel, le moyen le plus pratique pour effectuer cette étape consisterait à utiliser le [RDS. DataControl](datacontrol-object-rds.md) objet.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-106">**Part A**If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="ff5b1-107">**RDS.DataControl** combine l'étape précédente de création d'un proxy, et celle-ci, qui consiste à émettre une requête.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-107">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

<span data-ttu-id="ff5b1-p103">Définissez la propriété **Server** de l'objet [RDS.DataControl](server-property-rds.md) pour déterminer l'emplacement au niveau duquel le programme serveur doit être instancié, la propriété [Connect](connect-property-rds.md) pour spécifier la chaîne de connexion permettant d'accéder à la source de données et la propriété [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) pour spécifier le texte de la commande de requête. Exécutez ensuite la méthode [Refresh](refresh-method-rds.md) pour forcer le programme serveur à se connecter à la source de données, récupérer les lignes spécifiées par la requête et retourner un objet **Recordset** au client.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-p103">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated; the [Connect](connect-property-rds.md) property to specify the connect string to access the data source; and the [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property to specify the query command text. Then issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="ff5b1-110">Ce didacticiel n'utilise pas l'objet **RDS.DataControl**, mais, si c'était le cas, le code ressemblerait à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="ff5b1-110">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<span data-ttu-id="ff5b1-111">De même, le didacticiel n'appelle pas RDS avec les objets ADO, mais voici comment se présenterait le code dans le cas contraire :</span><span class="sxs-lookup"><span data-stu-id="ff5b1-111">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

<span data-ttu-id="ff5b1-112">**Partie B** La méthode générale d’effectuer cette étape consiste à appeler la méthode [Query](query-method-rds.md) de l’objet **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="ff5b1-112">**Part B**The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="ff5b1-113">Cette méthode prend une chaîne de connexion, utilisée pour établir la connexion à une source de données, et un texte de commande, pour spécifier les lignes à retourner par la source de données.</span><span class="sxs-lookup"><span data-stu-id="ff5b1-113">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="ff5b1-114">Ce didacticiel utilise la méthode **Query** de l'objet **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="ff5b1-114">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

