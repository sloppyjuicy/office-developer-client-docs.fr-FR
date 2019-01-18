---
title: 'Chapitre 12 : Didacticiel de Remote Data Service (RDS)'
TOCTitle: 'Chapter 12: RDS tutorial'
ms:assetid: fa44a5e8-e4df-dfdd-d7a1-a870ec3cabdd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250277(v=office.15)
ms:contentKeyID: 48548837
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aca77ac08688e643327bdbf229ab6c1dec40d109
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704804"
---
# <a name="chapter-12-remote-data-service-rds-tutorial"></a><span data-ttu-id="5abdd-102">Chapitre 12 : Didacticiel de Remote Data Service (RDS)</span><span class="sxs-lookup"><span data-stu-id="5abdd-102">Chapter 12: Remote Data Service (RDS) tutorial</span></span>

<span data-ttu-id="5abdd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5abdd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5abdd-104">Ce didacticiel illustre l'utilisation du modèle de programmation RDS pour interroger et mettre à jour une source de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-104">This tutorial illustrates using the RDS programming model to query and update a data source.</span></span> <span data-ttu-id="5abdd-105">Dans un premier temps, il décrit les étapes à suivre pour accomplir cette tâche.</span><span class="sxs-lookup"><span data-stu-id="5abdd-105">First, it describes the steps necessary to accomplish this task.</span></span> <span data-ttu-id="5abdd-106">Ensuite, le didacticiel est répété dans Microsoft Visual Basic Scripting Edition et Microsoft Visual J ++, visionnez ADO pour Windows Foundation Classes (ADO/WFC).</span><span class="sxs-lookup"><span data-stu-id="5abdd-106">Then the tutorial is repeated in Microsoft Visual Basic Scripting Edition and Microsoft Visual J++, featuring ADO for Windows Foundation Classes (ADO/WFC).</span></span>

<span data-ttu-id="5abdd-107">Ce didacticiel est codé dans différents langages pour deux raisons :</span><span class="sxs-lookup"><span data-stu-id="5abdd-107">This tutorial is coded in different languages for two reasons:</span></span>

- <span data-ttu-id="5abdd-p102">La documentation portant sur RDS part du principe que le lecteur code en Visual Basic. Si cette documentation s'avère utile pour les programmeurs qui codent en Visual Basic, elle l'est moins pour les programmeurs qui utilisent d'autres langages.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p102">The documentation for RDS assumes the reader codes in Visual Basic. This makes the documentation convenient for Visual Basic programmers, but less useful for programmers who use other languages.</span></span>

- <span data-ttu-id="5abdd-110">Si vous avez un doute concernant une fonctionnalité RDS déterminée et que vous possédez certaines connaissances dans un autre langage, vous pouvez éventuellement résoudre votre problème en examinant cette même fonction exprimée dans un autre langage.</span><span class="sxs-lookup"><span data-stu-id="5abdd-110">If you are uncertain about a particular RDS feature and you know a little of another language, you might be able to resolve your question by looking for the same feature expressed in another language.</span></span>

<span data-ttu-id="5abdd-p103">Ce didacticiel est basé sur le modèle de programmation RDS. Chaque étape du modèle de programmation y est abordée, avec en outre une illustration de chacune de ces étapes par un fragment de code Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p103">This tutorial is based on the RDS programming model. It discusses each step of the programming model individually. In addition, it illustrates each step with a fragment of Visual Basic code.</span></span>

<span data-ttu-id="5abdd-p104">L'exemple de code est reproduit dans les autres langages avec un minimum de détails. Chaque étape figurant dans le didacticiel d'un langage de programmation donné s'accompagne d'une mention de l'étape correspondante dans le modèle de programmation et le didacticiel descriptif. Servez-vous du numéro de l'étape pour accéder aux détails correspondants dans le didacticiel descriptif.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p104">The code example is repeated in other languages with minimal discussion. Each step in a given programming language tutorial is marked with the corresponding step in the programming model and descriptive tutorial. Use the number of the step to refer to the discussion in the descriptive tutorial.</span></span>

<span data-ttu-id="5abdd-p105">Le modèle de programmation RDS est indiqué ci-dessous. Référez-vous-y à mesure que vous avancez dans le didacticiel.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p105">The RDS programming model is stated below. Use it as a roadmap as you proceed through the tutorial.</span></span>

### <a name="rds-programming-model-with-objects"></a><span data-ttu-id="5abdd-119">Modèle de programmation RDS avec des objets</span><span class="sxs-lookup"><span data-stu-id="5abdd-119">RDS programming model with objects</span></span>

- <span data-ttu-id="5abdd-120">Spécifiez le programme à appeler sur le serveur et obtenir un moyen (proxy) d'y faire référence à partir du client.</span><span class="sxs-lookup"><span data-stu-id="5abdd-120">Specify the program to be invoked on the server, and obtain a way (proxy) to refer to it from the client.</span></span>

- <span data-ttu-id="5abdd-p106">Appelez le programme serveur. Transmettez les paramètres au programme serveur qui identifie la source de données et la commande à émettre.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p106">Invoke the server program. Pass parameters to the server program that identifies the data source and the command to issue.</span></span>

- <span data-ttu-id="5abdd-p107">Le programme serveur obtient un objet [Recordset](recordset-object-ado.md) auprès de la source de données, généralement en utilisant ADO. L'objet **Recordset** peut éventuellement être traité sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p107">The server program obtains a [Recordset](recordset-object-ado.md) object from the data source, typically by using ADO. Optionally, the **Recordset** object is processed on the server.</span></span>

- <span data-ttu-id="5abdd-125">Le programme serveur retourne l'objet **Recordset** final à l'application cliente.</span><span class="sxs-lookup"><span data-stu-id="5abdd-125">The server program returns the final **Recordset** object to the client application.</span></span>

- <span data-ttu-id="5abdd-126">Au niveau du client, l'objet **Recordset** est éventuellement placé dans un format facilement exploitable par des contrôles visuels.</span><span class="sxs-lookup"><span data-stu-id="5abdd-126">On the client, the **Recordset** object is optionally put into a form that can be easily used by visual controls.</span></span>

- <span data-ttu-id="5abdd-127">Les modifications apportées à l'objet **Recordset** sont renvoyées au serveur et utilisées pour la mise à jour de la source de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-127">Changes to the **Recordset** object are sent back to the server and used to update the data source.</span></span>

## <a name="step-1-specify-a-server-program"></a><span data-ttu-id="5abdd-128">Étape 1 : Spécifier un programme serveur</span><span class="sxs-lookup"><span data-stu-id="5abdd-128">Step 1: Specify a server program</span></span>

<span data-ttu-id="5abdd-p108">Dans la plupart des cas, utilisez la méthode [CreateObject](createobject-method-rds.md) de l’objet [RDS.DataSpace](dataspace-object-rds.md) pour spécifier le programme serveur par défaut, [RDSServer.DataFactory](datafactory-object-rdsserver.md), ou votre propre programme serveur personnalisé (objet métier). Un programme serveur est instancié sur le serveur et une référence à ce programme (ou *proxy*) est retournée.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p108">In the most general case, use the [RDS.DataSpace](dataspace-object-rds.md) object [CreateObject](createobject-method-rds.md) method to specify the default server program, [RDSServer.DataFactory](datafactory-object-rdsserver.md), or your own custom server program (business object). A server program is instantiated on the server, and a reference to the server program, or *proxy*, is returned.</span></span>

<span data-ttu-id="5abdd-131">Ce didacticiel utilise le programme serveur par défaut :</span><span class="sxs-lookup"><span data-stu-id="5abdd-131">This tutorial uses the default server program:</span></span>

```vb 
 
Sub RDSTutorial1() 
 Dim DS as New RDS.DataSpace 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
... 
``` 

## <a name="step-2-invoke-the-server-program"></a><span data-ttu-id="5abdd-132">Étape 2 : Appeler le programme serveur</span><span class="sxs-lookup"><span data-stu-id="5abdd-132">Step 2: Invoke the server program</span></span> 

<span data-ttu-id="5abdd-p109">Lorsque vous appelez une méthode sur le *proxy* client, c'est le programme serveur qui exécute cette méthode. Au cours de cette étape, vous allez exécuter une requête sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p109">When you invoke a method on the client *proxy*, the actual program on the server executes the method. In this step, you'll execute a query on the server.</span></span>

### <a name="part-a"></a><span data-ttu-id="5abdd-135">Partie A</span><span class="sxs-lookup"><span data-stu-id="5abdd-135">Part A</span></span>

<span data-ttu-id="5abdd-136">Si vous n’utilisiez [RDSServer.DataFactory](datafactory-object-rdsserver.md) dans ce didacticiel, le moyen le plus pratique pour effectuer cette étape consisterait à utiliser le [RDS. DataControl](datacontrol-object-rds.md) objet.</span><span class="sxs-lookup"><span data-stu-id="5abdd-136">If you weren't using [RDSServer.DataFactory](datafactory-object-rdsserver.md) in this tutorial, the most convenient way to perform this step would be to use the [RDS.DataControl](datacontrol-object-rds.md) object.</span></span> <span data-ttu-id="5abdd-137">**RDS.DataControl** combine l'étape précédente de création d'un proxy, et celle-ci, qui consiste à émettre une requête.</span><span class="sxs-lookup"><span data-stu-id="5abdd-137">The **RDS.DataControl** combines the previous step of creating a proxy, with this step, issuing the query.</span></span>

1. <span data-ttu-id="5abdd-138">Définir le **RDS. DataControl** propriété [Server](server-property-rds.md) pour identifier où le programme serveur doit être instancié.</span><span class="sxs-lookup"><span data-stu-id="5abdd-138">Set the **RDS.DataControl** object [Server](server-property-rds.md) property to identify where the server program should be instantiated.</span></span>

2. <span data-ttu-id="5abdd-139">Définir la propriété [Connect](connect-property-rds.md) pour spécifier la chaîne de connexion pour accéder à la source de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-139">Set the [Connect](connect-property-rds.md) property to specify the connect string to access the data source.</span></span>

3. <span data-ttu-id="5abdd-140">Définissez la propriété [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) pour spécifier le texte de commande de requête.</span><span class="sxs-lookup"><span data-stu-id="5abdd-140">Set the [SQL](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/sql-property-ado) property to specify the query command text.</span></span> 

4. <span data-ttu-id="5abdd-141">Problème de la méthode [Refresh](refresh-method-rds.md) pour forcer le programme serveur à se connecter à la source de données, récupérer les lignes spécifiées par la requête et retourner un objet **Recordset** au client.</span><span class="sxs-lookup"><span data-stu-id="5abdd-141">Issue the [Refresh](refresh-method-rds.md) method to cause the server program to connect to the data source, retrieve rows specified by the query, and return a **Recordset** object to the client.</span></span>

<span data-ttu-id="5abdd-142">Ce didacticiel n'utilise pas l'objet **RDS.DataControl**, mais, si c'était le cas, le code ressemblerait à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5abdd-142">This tutorial does not use the **RDS.DataControl**, but this is how it would look if it did:</span></span>

```vb 
 
Sub RDSTutorial2A() 
 Dim DC as New RDS.DataControl 
 DC.Server = "https://yourServer" 
 DC.Connect = "DSN=Pubs" 
 DC.SQL = "SELECT * FROM Authors" 
 DC.Refresh 
... 
```

<br/>

<span data-ttu-id="5abdd-143">De même, le didacticiel n'appelle pas RDS avec les objets ADO, mais voici comment se présenterait le code dans le cas contraire :</span><span class="sxs-lookup"><span data-stu-id="5abdd-143">Nor does the tutorial invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
"Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
```

### <a name="part-b"></a><span data-ttu-id="5abdd-144">Partie B</span><span class="sxs-lookup"><span data-stu-id="5abdd-144">Part B</span></span>

<span data-ttu-id="5abdd-145">La méthode générale d’effectuer cette étape consiste à appeler la méthode [Query](query-method-rds.md) de l’objet **RDSServer.DataFactory** .</span><span class="sxs-lookup"><span data-stu-id="5abdd-145">The general method of performing this step is to invoke the **RDSServer.DataFactory** object [Query](query-method-rds.md) method.</span></span> <span data-ttu-id="5abdd-146">Cette méthode prend une chaîne de connexion, utilisée pour établir la connexion à une source de données, et un texte de commande, pour spécifier les lignes à retourner par la source de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-146">That method takes a connect string, which is used to connect to a data source, and a command text, which is used to specify the rows to be returned from the data source.</span></span>

<span data-ttu-id="5abdd-147">Ce didacticiel utilise la méthode **Query** de l'objet **DataFactory**:</span><span class="sxs-lookup"><span data-stu-id="5abdd-147">This tutorial uses the **DataFactory** object **Query** method:</span></span>

```vb 
 
Sub RDSTutorial2B() 
 Dim DS as New RDS.DataSpace 
 Dim DF 
 Dim RS as ADODB.Recordset 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-3-server-obtains-a-recordset"></a><span data-ttu-id="5abdd-148">Étape 3 : Le serveur obtient un objet Recordset</span><span class="sxs-lookup"><span data-stu-id="5abdd-148">Step 3: Server obtains a Recordset</span></span> 

<span data-ttu-id="5abdd-p112">Le programme serveur utilise la chaîne de connexion et le texte de commande pour interroger la source de données et obtenir les lignes souhaitées. ADO est généralement utilisé pour récupérer cet objet **Recordset** même s'il est possible d'utiliser d'autres interfaces d'accès aux données Microsoft, comme OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p112">The server program uses the connect string and command text to query the data source for the desired rows. ADO is typically used to retrieve this **Recordset**, although other Microsoft data access interfaces, such as OLE DB, could be used.</span></span>

<span data-ttu-id="5abdd-151">Un programme serveur personnalisé peut ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="5abdd-151">A custom server program might look like this:</span></span>

```vb 
 
Public Function ServerProgram(cn as String, qry as String) as Object 
Dim rs as New ADODB.Recordset 
 rs.CursorLocation = adUseClient 
 rs.Open qry, cn 
 rs.ActiveConnection = Nothing 
 Set ServerProgram = rs 
End Function 
```

## <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="5abdd-152">Étape 4 : Le serveur retourne l’objet Recordset</span><span class="sxs-lookup"><span data-stu-id="5abdd-152">Step 4: Server returns the Recordset</span></span> 

<span data-ttu-id="5abdd-p113">RDS convertit l'objet **Recordset** récupéré dans un format qui peut être renvoyé au client (autrement dit, il *marshale* l'objet **Recordset**). La forme exacte de la conversion et son mode d'envoi varient selon que le serveur réside sur Internet ou sur un intranet, sur un réseau local ou qu'il corresponde à une bibliothèque de liaison dynamique. Toutefois, ce détail n'est pas crucial ; l'important est que RDS renvoie l'objet **Recordset** au client.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p113">RDS converts the retrieved **Recordset** object to a form that can be sent back to the client (that is, it *marshals* the **Recordset**). The exact form of the conversion and how it is sent depends on whether the server is on the Internet or an intranet, a local area network, or is a dynamic-link library. However, this detail is not critical; all that matters is that RDS sends the **Recordset** back to the client.</span></span>

<span data-ttu-id="5abdd-156">Côté client, un objet **Recordset** est retourné et affecté à une variable locale.</span><span class="sxs-lookup"><span data-stu-id="5abdd-156">On the client side, a **Recordset** object is returned and assigned to a local variable.</span></span>

```vb 
 
Sub RDSTutorial4() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query("DSN=Pubs", "SELECT * FROM Authors") 
... 
```

## <a name="step-5-datacontrol-is-made-usable"></a><span data-ttu-id="5abdd-157">Étape 5 : L’objet DataControl est rendu utilisable</span><span class="sxs-lookup"><span data-stu-id="5abdd-157">Step 5: DataControl is made usable</span></span> 

<span data-ttu-id="5abdd-p114">L'objet **Recordset** retourné est disponible et peut être utilisé. Vous pouvez l'examiner, le parcourir ou le modifier comme n'importe quel autre objet **Recordset**. L'utilisation que vous pouvez faire de cet objet **Recordset** dépend de votre environnement. Visual Basic et Visual C++ intègrent des contrôles visuels qu'un objet **Recordset** peut utiliser directement ou indirectement à l'aide d'un contrôle d'activation de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-p114">The returned **Recordset** object is available for use. You can examine, navigate, or edit it as you would any other **Recordset**. What you can do with the **Recordset** depends on your environment. Visual Basic and Visual C++ have visual controls that can use a **Recordset** directly or indirectly with the aid of an enabling data control.</span></span>

<span data-ttu-id="5abdd-162">Par exemple, si vous affichez une page Web dans Internet Explorer, vous souhaitez afficher les données de l’objet **Recordset** dans un contrôle visuel.</span><span class="sxs-lookup"><span data-stu-id="5abdd-162">For example, if you are displaying a webpage in Internet Explorer, you might want to display the **Recordset** object data in a visual control.</span></span> <span data-ttu-id="5abdd-163">Les contrôles visuels d’une page Web ne peut pas accéder à un objet **Recordset** directement.</span><span class="sxs-lookup"><span data-stu-id="5abdd-163">Visual controls on a webpage cannot access a **Recordset** object directly.</span></span> <span data-ttu-id="5abdd-164">Cependant, ils peuvent accéder à l’objet **Recordset** par le biais de la [RDS. DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5abdd-164">However, they can access the **Recordset** object through the [RDS.DataControl](datacontrol-object-rds.md).</span></span> <span data-ttu-id="5abdd-165">**RDS. DataControl** utilisable par un contrôle visuel lorsque sa propriété [SourceRecordset](recordset-sourcerecordset-properties-rds.md) est définie à l’objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5abdd-165">The **RDS.DataControl** becomes usable by a visual control when its [SourceRecordset](recordset-sourcerecordset-properties-rds.md) property is set to the **Recordset** object.</span></span>

<span data-ttu-id="5abdd-166">Le paramètre **DATASRC** de l'objet de contrôle visuel doit être défini sur **RDS.DataControl**, et sa propriété **DATAFLD** sur un champ (colonne) de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="5abdd-166">The visual control object must have its **DATASRC** parameter set to the **RDS.DataControl**, and its **DATAFLD** property set to a **Recordset** object field (column).</span></span>

<span data-ttu-id="5abdd-167">Dans ce didacticiel, définissez la propriété **SourceRecordset**:</span><span class="sxs-lookup"><span data-stu-id="5abdd-167">In this tutorial, set the **SourceRecordset** property:</span></span>

```vb 
 
Sub RDSTutorial5() 
 Dim DS as New RDS.DataSpace 
 Dim RS as ADODB.Recordset 
 Dim DC as New RDS.DataControl 
 Dim DF as Object 
 Set DF = DS.CreateObject("RDSServer.DataFactory", "https://yourServer") 
 Set RS = DF.Query ("DSN=Pubs", "SELECT * FROM Authors") 
 DC.SourceRecordset = RS ' Visual controls can now bind to DC. 
... 
```

## <a name="step-6-changes-are-sent-to-the-server"></a><span data-ttu-id="5abdd-168">Étape 6 : Les modifications sont envoyées au serveur</span><span class="sxs-lookup"><span data-stu-id="5abdd-168">Step 6: Changes are sent to the server</span></span>

<span data-ttu-id="5abdd-169">Si l'objet **Recordset** est modifié, les modifications correspondantes (p. ex., lignes ajoutées, modifiées ou supprimées) peuvent être renvoyées au serveur.</span><span class="sxs-lookup"><span data-stu-id="5abdd-169">If the **Recordset** object is edited, any changes (that is, rows that are added, changed, or deleted) can be sent back to the server.</span></span>

<span data-ttu-id="5abdd-170">[!REMARQUE] Le comportement par défaut de RDS peut être appelé implicitement avec les objets ADO et le fournisseur d'accès à distance Microsoft OLE DB.</span><span class="sxs-lookup"><span data-stu-id="5abdd-170">The default behavior of RDS can be invoked implicitly with ADO objects and the Microsoft OLE DB Remoting Provider.</span></span> <span data-ttu-id="5abdd-171">Les requêtes peuvent retourner des **jeux d’enregistrements**et modifié **jeux d’enregistrements** peuvent mettre à jour la source de données.</span><span class="sxs-lookup"><span data-stu-id="5abdd-171">Queries can return **Recordsets**, and edited **Recordsets** can update the data source.</span></span> <span data-ttu-id="5abdd-172">Ce didacticiel n'appelle pas RDS avec les objets ADO, mais, si c'était le cas, voici comment se présenterait le code :</span><span class="sxs-lookup"><span data-stu-id="5abdd-172">This tutorial does not invoke RDS with ADO objects, but this is how it would look if it did:</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
rs.Open "SELECT * FROM Authors","Provider=MS Remote;Data Source=Pubs;" & _ 
 "Remote Server=https://yourServer;Remote Provider=SQLOLEDB;" 
... ' Edit the Recordset. 
rs.UpdateBatch ' The equivalent of SubmitChanges. 
... 
```

### <a name="part-a"></a><span data-ttu-id="5abdd-173">Partie A</span><span class="sxs-lookup"><span data-stu-id="5abdd-173">Part A</span></span>

<span data-ttu-id="5abdd-174">Supposons dans cet exemple que vous avez utilisé uniquement la [RDS. DataControl](datacontrol-object-rds.md) et qu’un objet **Recordset** est maintenant associé à la **RDS. DataControl**.</span><span class="sxs-lookup"><span data-stu-id="5abdd-174">Assume for this case that you have only used the [RDS.DataControl](datacontrol-object-rds.md) and that a **Recordset** object is now associated with the **RDS.DataControl**.</span></span> <span data-ttu-id="5abdd-175">La méthode [SubmitChanges](submitchanges-method-rds.md) met à jour la source de données en fonction des modifications apportées à l'objet **Recordset** si les propriétés [Server](server-property-rds.md) et [Connect](connect-property-rds.md) sont toujours définies.</span><span class="sxs-lookup"><span data-stu-id="5abdd-175">The [SubmitChanges](submitchanges-method-rds.md) method updates the data source with any changes to the **Recordset** object if the [Server](server-property-rds.md) and [Connect](connect-property-rds.md) properties are still set.</span></span>

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

### <a name="part-b"></a><span data-ttu-id="5abdd-176">Partie B</span><span class="sxs-lookup"><span data-stu-id="5abdd-176">Part B</span></span>

<span data-ttu-id="5abdd-177">Vous pouvez également vous pourriez mettre à jour le serveur avec l’objet [RDSServer.DataFactory](datafactory-object-rdsserver.md) , définissant une connexion et un objet **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="5abdd-177">Alternatively, you could update the server with the [RDSServer.DataFactory](datafactory-object-rdsserver.md) object, specifying a connection and a **Recordset** object.</span></span>

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


## <a name="appendix-a-rds-tutorial-vbscript"></a><span data-ttu-id="5abdd-178">Annexe a : didacticiel RDS (VBScript)</span><span class="sxs-lookup"><span data-stu-id="5abdd-178">Appendix A: RDS tutorial (VBScript)</span></span>

<span data-ttu-id="5abdd-179">Il s’agit du didacticiel RDS, écrit en Microsoft Visual Basic Scripting Edition.</span><span class="sxs-lookup"><span data-stu-id="5abdd-179">This is the RDS tutorial, written in Microsoft Visual Basic Scripting Edition.</span></span> <span data-ttu-id="5abdd-180">Pour obtenir une description de l’objectif de ce didacticiel, voir l’introduction de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="5abdd-180">For a description of the purpose of this tutorial, see the introduction to this topic.</span></span>

<span data-ttu-id="5abdd-181">Dans ce didacticiel, [RDS. DataControl](datacontrol-object-rds.md) et [RDS. DataSpace](dataspace-object-rds.md) sont créés au moment du design ; Autrement dit, ils sont définis avec des balises object.</span><span class="sxs-lookup"><span data-stu-id="5abdd-181">In this tutorial, [RDS.DataControl](datacontrol-object-rds.md) and [RDS.DataSpace](dataspace-object-rds.md) are created at design time; that is, they are defined with object tags.</span></span> <span data-ttu-id="5abdd-182">Il est également possible de les créer au moment de l'exécution à l'aide de la méthode **Server.CreateObject**.</span><span class="sxs-lookup"><span data-stu-id="5abdd-182">Alternatively, they could be created at run time with the **Server.CreateObject** method.</span></span> 

<span data-ttu-id="5abdd-183">Par exemple, l'objet **RDS.DataControl** peut être créé de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="5abdd-183">For example, the **RDS.DataControl** object could be created like this:</span></span>

```vb
    Set DC = Server.CreateObject("RDS.DataControl") 
     <!-- RDS.DataControl --> 
     <OBJECT 
     ID="DC1" CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E33"> 
     </OBJECT> 
     
     <!-- RDS.DataSpace --> 
     <OBJECT 
     ID="DS1" WIDTH=1 HEIGHT=1 
     CLASSID="CLSID:BD96C556-65A3-11D0-983A-00C04FC29E36"> 
     </OBJECT> 
     
     <SCRIPT LANGUAGE="VBScript"> 
     
     Sub RDSTutorial() 
     Dim DF1 
```

### <a name="step-1-specify-a-server-program"></a><span data-ttu-id="5abdd-184">Étape 1 : Spécifier un programme serveur</span><span class="sxs-lookup"><span data-stu-id="5abdd-184">Step 1: Specify a server program</span></span>

<span data-ttu-id="5abdd-185">VBScript peut détecter le nom du serveur web IIS qu'exécute en accédant à la méthode VBScript **Request.ServerVariables** disponible pour les Pages ASP :</span><span class="sxs-lookup"><span data-stu-id="5abdd-185">VBScript can discover the name of the IIS web server it is running on by accessing the VBScript **Request.ServerVariables** method available to Active Server Pages:</span></span>

```vb 
 
"https://<%=Request.ServerVariables("SERVER_NAME")%>" 
```

<span data-ttu-id="5abdd-186">Toutefois, dans ce didacticiel, utilisez le serveur fictif « yourServer ».</span><span class="sxs-lookup"><span data-stu-id="5abdd-186">However, for this tutorial, use the imaginary server, "yourServer."</span></span>

> [!NOTE]
> <span data-ttu-id="5abdd-p120">[!REMARQUE] Soyez attentif au type de données des arguments **ByRef**. VBScript ne vous autorisant pas à spécifier le type de variable, vous devez toujours transmettre un type Variant. Si vous utilisez HTTP, RDS vous autorise à transmettre un type Variant à une méthode qui n'attend pas ce type de données si vous l'appelez avec la méthode **CreateObject** de l'objet [RDS.DataSpace](createobject-method-rds.md). Si vous utilisez DCOM ou un serveur in-process, faites en sorte que les types de paramètres côté client et côté serveur correspondent sans quoi vous obtiendrez une erreur « Incompatibilité de type ».</span><span class="sxs-lookup"><span data-stu-id="5abdd-p120">Pay attention to the data type of **ByRef** arguments. VBScript does not let you specify the variable type, so you must always pass a Variant. When using HTTP, RDS will allow you to pass a Variant to a method that expects a non-Variant if you invoke it with the **RDS.DataSpace** object [CreateObject](createobject-method-rds.md) method. When using DCOM or an in-process server, match the parameter types on the client and server sides or you will receive a "Type Mismatch" error.</span></span>

```vb
 
Set DF1 = DS1.CreateObject("RDSServer.DataFactory", "https://yourServer") 
```

### <a name="step-2-part-a-invoke-the-server-program-with-rdsdatacontrol"></a><span data-ttu-id="5abdd-191">Étape 2, composant a : appeler le programme serveur avec RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="5abdd-191">Step 2, Part A: Invoke the server program with RDS.DataControl</span></span>

<span data-ttu-id="5abdd-192">Cet exemple est simplement un commentaire illustrant le comportement par défaut de l'objet **RDS.DataControl**, qui consiste à exécuter la requête spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5abdd-192">This example is merely a comment demonstrating that the default behavior of the **RDS.DataControl** is to perform the specified query.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial2A() 
 Dim RS 
 DC1.Refresh 
 Set RS = DC1.Recordset 
... 
```

<span data-ttu-id="5abdd-193">Passez à l’étape suivante.</span><span class="sxs-lookup"><span data-stu-id="5abdd-193">Skip to the following step.</span></span>

### <a name="step-4-server-returns-the-recordset"></a><span data-ttu-id="5abdd-194">Étape 4 : Le serveur retourne l’objet Recordset</span><span class="sxs-lookup"><span data-stu-id="5abdd-194">Step 4: Server returns the Recordset</span></span>

```vb
 
Set RS = DF1.Query("DSN=Pubs;", "SELECT * FROM Authors") 
```

### <a name="step-5-datacontrol-is-made-usable-by-visual-controls"></a><span data-ttu-id="5abdd-195">Étape 5 : DataControl est rendu utilisable par les contrôles visuels</span><span class="sxs-lookup"><span data-stu-id="5abdd-195">Step 5: DataControl is made usable by visual controls</span></span>

```vb
 
' Assign the returned recordset to the DataControl. 
 
DC1.SourceRecordset = RS 
```

### <a name="step-6-part-a-changes-are-sent-to-the-server-with-rdsdatacontrol"></a><span data-ttu-id="5abdd-196">Étape 6, composant r : les modifications sont envoyées au serveur avec RDS. DataControl</span><span class="sxs-lookup"><span data-stu-id="5abdd-196">Step 6, Part A: Changes are sent to the server with RDS.DataControl</span></span>

<span data-ttu-id="5abdd-197">Cet exemple est simplement un commentaire illustrant la façon dont **RDS.DataControl** effectue les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="5abdd-197">This example is merely a comment demonstrating how the **RDS.DataControl** performs updates.</span></span>

```vb
 
<OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DC1"> 
 <PARAM NAME="SQL" VALUE="SELECT * FROM Authors"> 
 <PARAM NAME="Connect" VALUE="DSN=Pubs;"> 
 <PARAM NAME="Server" VALUE="https://yourServer/"> 
</OBJECT> 
... 
<SCRIPT LANGUAGE="VBScript"> 
 
Sub RDSTutorial6A() 
Dim RS 
DC1.Refresh 
... 
Set RS = DC1.Recordset 
' Edit the Recordset object... 
' The SERVER and CONNECT properties are already set from Step 2A. 
Set DC1.SourceRecordset = RS 
... 
DC1.SubmitChanges 
```

### <a name="step-6-part-b-changes-are-sent-to-the-server-with-rdsserverdatafactory"></a><span data-ttu-id="5abdd-198">Étape 6, composant b : les modifications sont envoyées au serveur avec RDSServer.DataFactory</span><span class="sxs-lookup"><span data-stu-id="5abdd-198">Step 6, Part B: Changes are sent to the server with RDSServer.DataFactory</span></span>

```vb
 
DF.SubmitChanges"DSN=Pubs", RS 
 
End Sub 
</SCRIPT> 
</BODY> 
</HTML> 
```

## <a name="appendix-b-rds-tutorial-visual-j"></a><span data-ttu-id="5abdd-199">Annexe b : didacticiel RDS (Visual J ++)</span><span class="sxs-lookup"><span data-stu-id="5abdd-199">Appendix B: RDS tutorial (Visual J++)</span></span>

<span data-ttu-id="5abdd-p121">ADO/WFC ne suit pas intégralement le modèle d'objet RDS en cela qu'il n'implémente pas l'objet [RDS.DataControl](datacontrol-object-rds.md). ADO/WFC implémente uniquement la classe côté client[RDS.DataSpace](dataspace-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5abdd-p121">ADO/WFC does not completely follow the RDS object model in that it does not implement the [RDS.DataControl](datacontrol-object-rds.md) object. ADO/WFC only implements the client-side class, [RDS.DataSpace](dataspace-object-rds.md).</span></span>

<span data-ttu-id="5abdd-p122">La classe **DataSpace** implémente une seule méthode, [CreateObject](createobject-method-rds.md), qui retourne un objet [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax). La classe **DataSpace** implémente également la propriété [InternetTimeout](internettimeout-property-rds.md).</span><span class="sxs-lookup"><span data-stu-id="5abdd-p122">The **DataSpace** class implements one method, [CreateObject](createobject-method-rds.md), which returns an [ObjectProxy](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/objectproxy-ado-wfc-syntax) object. The **DataSpace** class also implements the [InternetTimeout](internettimeout-property-rds.md) property.</span></span>

<span data-ttu-id="5abdd-204">La classe **ObjectProxy** implémente une seule méthode, call, qui peut appeler n'importe quel objet métier côté serveur.</span><span class="sxs-lookup"><span data-stu-id="5abdd-204">The **ObjectProxy** class implements one method, call, which can invoke any server-side business object.</span></span>

```java 
 
import com.ms.wfc.data.*; 
public class RDSTutorial 
{ 
 public void tutorial() 
 { 
// Step 1: Specify a server program. 
 ObjectProxy obj = 
 DataSpace.createObject( 
 "RDSServer.DataFactory", 
 "https://YourServer"); 
 
// Step 2: Server returns a Recordset. 
 Recordset rs = (Recordset) obj.call( 
 "Query", 
 new Object[] {"DSN=Pubs;", "SELECT * FROM Authors"}); 
 
// Step 3: Changes are sent to the server. 
 ... // Edit Recordset. 
 obj.call( 
 "SubmitChanges", 
 new Object[] {"DSN=Pubs;", rs}); 
 return; 
 } 
} 
```



