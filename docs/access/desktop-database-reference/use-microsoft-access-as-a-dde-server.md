---
title: Utilisation de Microsoft Access en tant que serveur DDE
TOCTitle: Use Microsoft Access as a DDE Server
description: Microsoft Access prend en charge l'échange dynamique de données (DDE) à la fois comme application de destination (client) et comme application source (serveur).
ms:assetid: a3e82bf7-94b5-8eec-86bc-2d5387d66738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821067(v=office.15)
ms:contentKeyID: 48546801
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5186349
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0e22eb03571d51f28344f6d41fdcaa47321f67af
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870918"
---
# <a name="use-microsoft-access-as-a-dde-server"></a><span data-ttu-id="21356-103">Utilisation de Microsoft Access en tant que serveur DDE</span><span class="sxs-lookup"><span data-stu-id="21356-103">Use Microsoft Access as a DDE server</span></span>

<span data-ttu-id="21356-104">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21356-104">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="21356-p101">Microsoft Access prend en charge l'échange dynamique de données (DDE) à la fois comme application de destination (client) et comme application source (serveur). Par exemple, une application telle que Microsoft Word, représentant le client, peut utiliser l'échange dynamique de données pour demander des données à une base de données Microsoft Access, représentant le serveur.</span><span class="sxs-lookup"><span data-stu-id="21356-p101">Microsoft Access supports dynamic data exchange (DDE) as either a destination (client) application or a source (server) application. For example, an application such as Microsoft Word, acting as a client, can request data through DDE from a Microsoft Access database that's acting as a server.</span></span>

> [!TIP]
> <span data-ttu-id="21356-107">[!CONSEIL] Si vous souhaitez manipuler des objets Microsoft Access à partir d'une autre application, il est peut-être préférable de recourir à l'automation.</span><span class="sxs-lookup"><span data-stu-id="21356-107">If you need to manipulate Microsoft Access objects from another application, you may want to consider using Automation.</span></span>

<span data-ttu-id="21356-108">Une conversation DDE entre un client et un serveur est établie sur un sujet spécifique.</span><span class="sxs-lookup"><span data-stu-id="21356-108">A DDE conversation between a client and server is established on a particular topic.</span></span> <span data-ttu-id="21356-109">Ce sujet est soit un fichier de données qui utilise le format reconnu par l'application serveur, soit le sujet System qui fournit les informations relatives à l'application serveur elle-même.</span><span class="sxs-lookup"><span data-stu-id="21356-109">A topic can be either a data file in the format supported by the server application, or it can be the System topic, which supplies information about the server application itself.</span></span> <span data-ttu-id="21356-110">Une fois une conversation créée sur un sujet particulier, seulement un élément de données associé à cette rubrique peut être transféré.</span><span class="sxs-lookup"><span data-stu-id="21356-110">After a conversation has begun on a particular topic, only a data item associated with that topic can be transferred.</span></span>

<span data-ttu-id="21356-p103">Par exemple, supposez que Microsoft Word pour Windows est en cours d'exécution et que vous souhaitez insérer des données d'une base de données Microsoft Access particulière dans un document. Vous entamez une conversation DDE avec Microsoft Access en ouvrant un canal DDE à l'aide de la fonction **DDEInitiate** et en spécifiant le nom du fichier de base de données comme sujet. Vous pouvez alors transférer des données de cette base de données vers Microsoft Word à travers ce canal.</span><span class="sxs-lookup"><span data-stu-id="21356-p103">For example, suppose you are running Microsoft Word and want to insert data from a particular Microsoft Access database into a document. You begin a DDE conversation with Microsoft Access by opening a DDE channel with the **DDEInitiate** function and specifying the database file name as the topic. You can then transfer data from that database to Microsoft Word through that channel.</span></span>

<span data-ttu-id="21356-114">En tant que serveur DDE, Microsoft Access reconnaît les sujets suivants :</span><span class="sxs-lookup"><span data-stu-id="21356-114">As a DDE server, Microsoft Access supports the following topics:</span></span>

- <span data-ttu-id="21356-115">Le sujet System</span><span class="sxs-lookup"><span data-stu-id="21356-115">The System topic</span></span>

- <span data-ttu-id="21356-116">Le nom d'une base de données (sujet *base-de-données*)</span><span class="sxs-lookup"><span data-stu-id="21356-116">The name of a database (*database* topic)</span></span>

- <span data-ttu-id="21356-117">Le nom d'une table (sujet *nom-table*)</span><span class="sxs-lookup"><span data-stu-id="21356-117">The name of a table (*tablename* topic)</span></span>

- <span data-ttu-id="21356-118">Le nom d'une requête (sujet *nom-requête*)</span><span class="sxs-lookup"><span data-stu-id="21356-118">The name of a query (*queryname* topic)</span></span>

- <span data-ttu-id="21356-119">Une instruction Microsoft Access SQL (sujet *chaîne-sql*)</span><span class="sxs-lookup"><span data-stu-id="21356-119">A Microsoft Access SQL string (*sqlstring* topic)</span></span>

<span data-ttu-id="21356-120">Une fois que vous avez créé une conversation DDE, vous pouvez utiliser l’instruction **DDEExecute** pour envoyer une commande à partir du client à l’application serveur.</span><span class="sxs-lookup"><span data-stu-id="21356-120">After you've established a DDE conversation, you can use the **DDEExecute** statement to send a command from the client to the server application.</span></span> <span data-ttu-id="21356-121">Lorsqu'il est utilisé comme serveur DDE, Microsoft Access reconnaît, comme commande valide, n'importe lequel des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="21356-121">When used as a DDE server, Microsoft Access recognizes any of the following as a valid command:</span></span>

- <span data-ttu-id="21356-122">Le nom d'une macro dans la base de données en cours.</span><span class="sxs-lookup"><span data-stu-id="21356-122">The name of a macro in the current database.</span></span>

- <span data-ttu-id="21356-123">N'importe quelle action que vous pouvez exécuter en Visual Basic au moyen d'une des méthodes de l'objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="21356-123">Any action that you can carry out in Visual Basic by using one of the methods of the **DoCmd** object.</span></span>

- <span data-ttu-id="21356-p105">Les actions OuvrirBase et FermerBase, qui ne sont utilisées que pour l'échange dynamique de données (pour savoir comment utiliser ces actions, voyez l'exemple plus loin sous cette rubrique).</span><span class="sxs-lookup"><span data-stu-id="21356-p105">The OpenDatabase and CloseDatabase actions, which are used only for DDE operations. (For an example of how to use these actions, see the example later in this topic.)</span></span>

> [!NOTE]
> <span data-ttu-id="21356-p106">[!REMARQUE] Lorsque vous spécifiez une action de macro comme instruction **DDEExecute**, l'action et les arguments éventuels suivent la syntaxe de **DoCmd** et doivent être entourés de crochets ([ ]). Toutefois, les applications qui prennent en charge DDE ne reconnaissent pas les constantes intrinsèques dans les opérations DDE. De même, les arguments de type chaîne de caractères doivent être entourés de guillemets doubles (" ") si la chaîne renferme une virgule. Dans tous les autres cas, les guillemets doubles sont superflus.</span><span class="sxs-lookup"><span data-stu-id="21356-p106">When you specify a macro action as a **DDEExecute** statement, the action and any arguments follow the **DoCmd** object syntax and must be enclosed in brackets ([ ]). However, applications that support DDE don't recognize intrinsic constants in DDE operations. Also, string arguments must be enclosed in quotation marks (" ") if the string contains a comma. Otherwise, quotation marks aren't required.</span></span>

<span data-ttu-id="21356-130">L'application client peut utiliser la fonction **DDERequest** pour demander des données textuelles à l'application serveur sur un canal DDE ouvert.</span><span class="sxs-lookup"><span data-stu-id="21356-130">The client application can use the **DDERequest** function to request text data from the server application over an open DDE channel.</span></span> <span data-ttu-id="21356-131">Elle peut également utiliser l'instruction **DDEPoke** pour envoyer des données à l'application serveur.</span><span class="sxs-lookup"><span data-stu-id="21356-131">Or the client can use the **DDEPoke** statement to send data to the server application.</span></span> <span data-ttu-id="21356-132">Une fois le transfert de données terminée, le client peut utiliser l’instruction **DDETerminate** pour fermer le canal DDE, ou l’instruction **DDETerminateAll** pour fermer tous les canaux ouverts.</span><span class="sxs-lookup"><span data-stu-id="21356-132">After the data transfer is complete, the client can use the **DDETerminate** statement to close the DDE channel, or the **DDETerminateAll** statement to close all open channels.</span></span>

> [!NOTE]
> <span data-ttu-id="21356-133">[!REMARQUE] Lorsque la réception de données par votre application client à travers un canal DDE est terminée, il est préférable de fermer ce canal afin de ne pas épuiser la mémoire et les ressources du système.</span><span class="sxs-lookup"><span data-stu-id="21356-133">When your client application has finished receiving data over a DDE channel, it should close that channel to conserve memory resources.</span></span>

<span data-ttu-id="21356-p108">L'exemple suivant montre comment créer avec Visual Basic une procédure Microsoft Word qui utilise Microsoft Access comme serveur DDE (pour que cet exemple fonctionne, Microsoft Access doit être actif) :</span><span class="sxs-lookup"><span data-stu-id="21356-p108">The following example demonstrates how to create a Microsoft Word procedure with Visual Basic that uses Microsoft Access as a DDE server. (For this example to work, Microsoft Access must be running.)</span></span>

```vb
    Sub AccessDDE() 
        Dim intChan1 As Integer, intChan2 As Integer 
        Dim strQueryData As String 
     
        ' Use System topic to open Northwind sample database. 
        ' Database must be open before using other DDE topics. 
        intChan1 = DDEInitiate("MSAccess", "System") 
        ' You may need to change this path to point to actual location 
        ' of Northwind sample database. 
        DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]" 
     
        ' Get all data from Ten Most Expensive Products query. 
        intChan2 = DDEInitiate("MSAccess", "Northwind.mdb;" _ 
            & "QUERY Ten Most Expensive Products") 
        strQueryData = DDERequest(intChan2, "All") 
        DDETerminate intChan2 
     
        ' Close database. 
        DDEExecute intChan1, "[CloseDatabase]" 
        DDETerminate intChan1 
     
        ' Print retrieved data to Debug Window. 
        Debug.Print strQueryData 
    End Sub
```

<br/>

<span data-ttu-id="21356-136">Les sections suivantes vous informent sur les sujets DDE valides pris en charge par Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="21356-136">The following sections provide information about the valid DDE topics supported by Microsoft Access.</span></span>

## <a name="the-system-topic"></a><span data-ttu-id="21356-137">Le sujet System</span><span class="sxs-lookup"><span data-stu-id="21356-137">The System topic</span></span>

<span data-ttu-id="21356-138">Le sujet System est une rubrique standard pour toutes les applications basées sur Windows de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="21356-138">The System topic is a standard topic for all Microsoft Windows–based applications.</span></span> <span data-ttu-id="21356-139">Fournit des informations sur les autres rubriques pris en charge par l’application.</span><span class="sxs-lookup"><span data-stu-id="21356-139">It supplies information about the other topics supported by the application.</span></span> <span data-ttu-id="21356-140">Pour accéder à ces informations, votre code doit d’abord appeler la fonction **DDEInitiate** avec l’argument *sujet* , puis exécuter l’instruction **DDERequest** utilisant une des suivantes pour l’argument *élément* .</span><span class="sxs-lookup"><span data-stu-id="21356-140">To access this information, your code must first call the **DDEInitiate** function with the *topic* argument, and then execute the **DDERequest** statement with one of the following supplied for the *item* argument.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21356-141">Élément</span><span class="sxs-lookup"><span data-stu-id="21356-141">Item</span></span></p></th>
<th><p><span data-ttu-id="21356-142">Renvoie</span><span class="sxs-lookup"><span data-stu-id="21356-142">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21356-143">SysItems</span><span class="sxs-lookup"><span data-stu-id="21356-143">SysItems</span></span></p></td>
<td><p><span data-ttu-id="21356-144">Une liste d'éléments pris en charge par le sujet System dans Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="21356-144">A list of items supported by the System topic in Microsoft Access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-145">Formats</span><span class="sxs-lookup"><span data-stu-id="21356-145">Formats</span></span></p></td>
<td><p><span data-ttu-id="21356-146">Une liste des formats que Microsoft Access peut copier dans le Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="21356-146">A list of the formats Microsoft Access can copy onto the Clipboard.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-147">Status</span><span class="sxs-lookup"><span data-stu-id="21356-147">Status</span></span></p></td>
<td><p><span data-ttu-id="21356-148">&quot;Occupé (e)&quot; ou &quot;prêt&quot;.</span><span class="sxs-lookup"><span data-stu-id="21356-148">&quot;Busy&quot; or &quot;Ready&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-149">Topics</span><span class="sxs-lookup"><span data-stu-id="21356-149">Topics</span></span></p></td>
<td><p><span data-ttu-id="21356-150">Une liste de toutes les bases de données ouvertes.</span><span class="sxs-lookup"><span data-stu-id="21356-150">A list of all open databases.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="21356-151">L'exemple suivant montre comment utiliser les fonctions **DDEInitiate** et **DDERequest** avec le sujet System :</span><span class="sxs-lookup"><span data-stu-id="21356-151">The following example demonstrates the use of the **DDEInitiate** and **DDERequest** functions with the System topic:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with Microsoft Access. 
    Dim intChan1 As Integer, strResults As String 
    intChan1 = DDEInitiate("MSAccess", "System") 
    ' Request list of topics supported by System topic. 
    strResults = DDERequest(intChan1, "SysItems") 
    ' Run OpenDatabase action to open Northwind.mdb. 
    ' You may need to change this path to point to actual location 
    ' of Northwind sample database. 
    DDEExecute intChan1, "[OpenDatabase C:\Access\Samples\Northwind.mdb]"
```

## <a name="the-database-topic"></a><span data-ttu-id="21356-152">La rubrique de la base de données</span><span class="sxs-lookup"><span data-stu-id="21356-152">The database topic</span></span>

<span data-ttu-id="21356-153">La rubrique de la *base de données* est le nom de fichier d’une base de données.</span><span class="sxs-lookup"><span data-stu-id="21356-153">The *database* topic is the file name of an existing database.</span></span> <span data-ttu-id="21356-154">Vous pouvez taper uniquement le nom de base (Les Comptoirs) ou son chemin d’accès et extension .mdb (c :\\Access\\exemples\\Northwind.mdb).</span><span class="sxs-lookup"><span data-stu-id="21356-154">You can type either just the base name (Northwind), or its path and .mdb extension (C:\\Access\\Samples\\Northwind.mdb).</span></span> <span data-ttu-id="21356-155">Une fois que vous avez engagé une conversation DDE avec la base de données, vous pouvez demander une liste des objets contenus dans celle-ci.</span><span class="sxs-lookup"><span data-stu-id="21356-155">After you start a DDE conversation with the database, you can request a list of the objects in that database.</span></span>

> [!NOTE]
> <span data-ttu-id="21356-156">[!REMARQUE] Vous ne pouvez pas recourir à l'échange dynamique de données (DDE) pour interroger le fichier d'information du groupe de travail.</span><span class="sxs-lookup"><span data-stu-id="21356-156">You can't use DDE to query the Microsoft Access workgroup information file.</span></span>

<span data-ttu-id="21356-157">Le sujet *base-de-données* prend en charge les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="21356-157">The *database* topic supports the following items.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21356-158">Élément</span><span class="sxs-lookup"><span data-stu-id="21356-158">Item</span></span></p></th>
<th><p><span data-ttu-id="21356-159">Renvoie</span><span class="sxs-lookup"><span data-stu-id="21356-159">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21356-160">TableList</span><span class="sxs-lookup"><span data-stu-id="21356-160">TableList</span></span></p></td>
<td><p><span data-ttu-id="21356-161">Une liste de tables</span><span class="sxs-lookup"><span data-stu-id="21356-161">A list of tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-162">QueryList</span><span class="sxs-lookup"><span data-stu-id="21356-162">QueryList</span></span></p></td>
<td><p><span data-ttu-id="21356-163">Une liste de requêtes</span><span class="sxs-lookup"><span data-stu-id="21356-163">A list of queries</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-164">FormList</span><span class="sxs-lookup"><span data-stu-id="21356-164">FormList</span></span></p></td>
<td><p><span data-ttu-id="21356-165">Une liste de formulaires</span><span class="sxs-lookup"><span data-stu-id="21356-165">A list of forms</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-166">ReportList</span><span class="sxs-lookup"><span data-stu-id="21356-166">ReportList</span></span></p></td>
<td><p><span data-ttu-id="21356-167">Une liste de rapports</span><span class="sxs-lookup"><span data-stu-id="21356-167">A list of reports</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-168">MacroList</span><span class="sxs-lookup"><span data-stu-id="21356-168">MacroList</span></span></p></td>
<td><p><span data-ttu-id="21356-169">Une liste de macros</span><span class="sxs-lookup"><span data-stu-id="21356-169">A list of macros</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-170">ModuleList</span><span class="sxs-lookup"><span data-stu-id="21356-170">ModuleList</span></span></p></td>
<td><p><span data-ttu-id="21356-171">Une liste de modules</span><span class="sxs-lookup"><span data-stu-id="21356-171">A list of modules</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-172">ViewList</span><span class="sxs-lookup"><span data-stu-id="21356-172">ViewList</span></span></p></td>
<td><p><span data-ttu-id="21356-173">Une liste d'affichages.</span><span class="sxs-lookup"><span data-stu-id="21356-173">A list of views</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-174">StoredProcedureList</span><span class="sxs-lookup"><span data-stu-id="21356-174">StoredProcedureList</span></span></p></td>
<td><p><span data-ttu-id="21356-175">Une liste de procédures enregistrées.</span><span class="sxs-lookup"><span data-stu-id="21356-175">A list of stored procedures</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-176">DatabaseDiagramList</span><span class="sxs-lookup"><span data-stu-id="21356-176">DatabaseDiagramList</span></span></p></td>
<td><p><span data-ttu-id="21356-177">Une liste de schémas de base de données.</span><span class="sxs-lookup"><span data-stu-id="21356-177">A list of database diagrams</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="21356-178">L'exemple suivant montre comment ouvrir le formulaire Employés de la base de données Les comptoirs à l'aide d'une procédure Visual Basic :</span><span class="sxs-lookup"><span data-stu-id="21356-178">The following example shows how you can open the Employees form in the Northwind sample database from a Visual Basic procedure:</span></span>

```vb
    ' In Visual Basic, initiate DDE conversation with 
    ' Northwind sample database. 
    ' Make sure database is open. 
    intChan2 = DDEInitiate("MSAccess", "Northwind") 
    ' Request list of forms in Northwind sample database. 
    strResponse = DDERequest(intChan2, "FormList") 
    ' Run OpenForm action and arguments to open Employees form. 
    DDEExecute intChan2, "[OpenForm Employees,0,,,1,0]"
```

## <a name="the-table-topic"></a><span data-ttu-id="21356-179">La rubrique de la TABLE</span><span class="sxs-lookup"><span data-stu-id="21356-179">The TABLE topic</span></span>

<span data-ttu-id="21356-180">Ces sujets utilisent la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="21356-180">These topics use the following syntax:</span></span>

<span data-ttu-id="21356-181">_databasename_ ; **Tableau** _TableName_</span><span class="sxs-lookup"><span data-stu-id="21356-181">_databasename_ ; **TABLE** _tablename_</span></span>

<span data-ttu-id="21356-182">_databasename_ ; **Requête** _nom-requête_</span><span class="sxs-lookup"><span data-stu-id="21356-182">_databasename_ ; **QUERY** _queryname_</span></span>

<span data-ttu-id="21356-183">_databasename_ ; **SQL** [ _chaîne-SQL_ ]</span><span class="sxs-lookup"><span data-stu-id="21356-183">_databasename_ ; **SQL** [ _sqlstring_ ]</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21356-184">Élément</span><span class="sxs-lookup"><span data-stu-id="21356-184">Part</span></span></p></th>
<th><p><span data-ttu-id="21356-185">Description</span><span class="sxs-lookup"><span data-stu-id="21356-185">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21356-186"><em>nombase</em></span><span class="sxs-lookup"><span data-stu-id="21356-186"><em>databasename</em></span></span></p></td>
<td><p><span data-ttu-id="21356-p111">Le nom de la base de données contenant la table ou la requête à laquelle s'applique l'instruction SQL, suivi d'un point-virgule (;). Le nom de la base de données peut se présenter sous la forme la plus simple (Comptoir) ou sous la forme du nom complet avec chemin d'accès et extension .mdb (C:\Access\Samples\Comptoir.mdb).</span><span class="sxs-lookup"><span data-stu-id="21356-p111">The name of the database that the table or query is in or that the SQL statement applies to, followed by a semicolon (;). The database name can be just the base name (Northwind) or its full path and .mdb extension (C:\Access\Samples\Northwind.mdb).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-189"><em>nomtable</em></span><span class="sxs-lookup"><span data-stu-id="21356-189"><em>tablename</em></span></span></p></td>
<td><p><span data-ttu-id="21356-190">Le nom d'une table existante.</span><span class="sxs-lookup"><span data-stu-id="21356-190">The name of an existing table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-191"><em>nomrequête</em></span><span class="sxs-lookup"><span data-stu-id="21356-191"><em>queryname</em></span></span></p></td>
<td><p><span data-ttu-id="21356-192">Le nom d'une requête existante.</span><span class="sxs-lookup"><span data-stu-id="21356-192">The name of an existing query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-193"><em>chaîne-sql</em></span><span class="sxs-lookup"><span data-stu-id="21356-193"><em>sqlstring</em></span></span></p></td>
<td><p><span data-ttu-id="21356-194">Une instruction SQL valide jusqu'à 256 caractères et se terminant par un point-virgule.</span><span class="sxs-lookup"><span data-stu-id="21356-194">A valid SQL statement up to 256 characters long, ending with a semicolon.</span></span> <span data-ttu-id="21356-195">Pour échanger plus de 256 caractères, omettez cet argument et à la place de plusieurs instructions <strong>DDEPoke</strong> successives pour créer une instruction SQL.</span><span class="sxs-lookup"><span data-stu-id="21356-195">To exchange more than 256 characters, omit this argument and instead use successive <strong>DDEPoke</strong> statements to build an SQL statement.</span></span> <span data-ttu-id="21356-196">Par exemple, le code Visual Basic suivant crée une instruction SQL au moyen de <strong>DDEPoke</strong>, puis demande le résultat de la requête.</span><span class="sxs-lookup"><span data-stu-id="21356-196">For example, the following Visual Basic code uses the <strong>DDEPoke</strong> statement to build an SQL statement and then request the results of the query.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="21356-197">Le tableau ci-dessous énumère les éléments valides pour les sujets TABLE *nom-table*, QUERY *nom-requête* et SQL *chaîne-sql*.</span><span class="sxs-lookup"><span data-stu-id="21356-197">The following table lists the valid items for the TABLE *tablename*, QUERY *queryname*, and SQL *sqlstring* topics.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21356-198">Élément</span><span class="sxs-lookup"><span data-stu-id="21356-198">Item</span></span></p></th>
<th><p><span data-ttu-id="21356-199">Renvoie</span><span class="sxs-lookup"><span data-stu-id="21356-199">Returns</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21356-200">Tous</span><span class="sxs-lookup"><span data-stu-id="21356-200">All</span></span></p></td>
<td><p><span data-ttu-id="21356-201">Toutes les données contenues dans la table, y compris les noms de champs.</span><span class="sxs-lookup"><span data-stu-id="21356-201">All the data in the table, including field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-202">Données</span><span class="sxs-lookup"><span data-stu-id="21356-202">Data</span></span></p></td>
<td><p><span data-ttu-id="21356-203">Toutes les lignes de données, sans les noms de champs.</span><span class="sxs-lookup"><span data-stu-id="21356-203">All rows of data, without field names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-204">FieldNames</span><span class="sxs-lookup"><span data-stu-id="21356-204">FieldNames</span></span></p></td>
<td><p><span data-ttu-id="21356-205">Une liste d'une seule ligne reprenant les noms de champs.</span><span class="sxs-lookup"><span data-stu-id="21356-205">A single-row list of field names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-206">FieldNames ; T</span><span class="sxs-lookup"><span data-stu-id="21356-206">FieldNames;T</span></span></p></td>
<td><p><span data-ttu-id="21356-207">Une liste de deux lignes reprenant les noms de champs (première ligne) et leurs types de données (seconde ligne).</span><span class="sxs-lookup"><span data-stu-id="21356-207">A two-row list of field names (first row) and their data types (second row).</span></span></p>
<p><span data-ttu-id="21356-208">Voici les valeurs renvoyées :</span><span class="sxs-lookup"><span data-stu-id="21356-208">These are the values returned:</span></span></p>
<p><span data-ttu-id="21356-209">Valeur</span><span class="sxs-lookup"><span data-stu-id="21356-209">Value</span></span></p>
<p><ul>
<li><span data-ttu-id="21356-210">0</span><span class="sxs-lookup"><span data-stu-id="21356-210">0</span></span></li>
<li><span data-ttu-id="21356-211">1</span><span class="sxs-lookup"><span data-stu-id="21356-211">1</span></span></li>
<li><span data-ttu-id="21356-212">2</span><span class="sxs-lookup"><span data-stu-id="21356-212">2</span></span></li>
<li><span data-ttu-id="21356-213">3</span><span class="sxs-lookup"><span data-stu-id="21356-213">3</span></span></li>
<li><span data-ttu-id="21356-214">4</span><span class="sxs-lookup"><span data-stu-id="21356-214">4</span></span></li>
<li><span data-ttu-id="21356-215">5</span><span class="sxs-lookup"><span data-stu-id="21356-215">5</span></span></li>
<li><span data-ttu-id="21356-216">6</span><span class="sxs-lookup"><span data-stu-id="21356-216">6</span></span></li>
<li><span data-ttu-id="21356-217">7</span><span class="sxs-lookup"><span data-stu-id="21356-217">7</span></span></li>
<li><span data-ttu-id="21356-218">8</span><span class="sxs-lookup"><span data-stu-id="21356-218">8</span></span></li>
<li><span data-ttu-id="21356-219">9</span><span class="sxs-lookup"><span data-stu-id="21356-219">9</span></span></li>
<li><span data-ttu-id="21356-220">10</span><span class="sxs-lookup"><span data-stu-id="21356-220">10</span></span></li>
<li><span data-ttu-id="21356-221">11</span><span class="sxs-lookup"><span data-stu-id="21356-221">11</span></span></li>
<li><span data-ttu-id="21356-222">12</span><span class="sxs-lookup"><span data-stu-id="21356-222">12</span></span></li>
</ul>
</p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-223">NextRow</span><span class="sxs-lookup"><span data-stu-id="21356-223">NextRow</span></span></p></td>
<td><p><span data-ttu-id="21356-p113">Les données contenues dans la ligne suivante de la table ou de la requête. Lorsque vous ouvrez un canal, NextRow retourne les données dans la première ligne. Si la ligne en cours est le dernier enregistrement et si vous exécutez NextRow, l'appel échoue.</span><span class="sxs-lookup"><span data-stu-id="21356-p113">The data in the next row in the table or query. When you open a channel, NextRow returns the data in the first row. If the current row is the last record and you run NextRow, the request fails.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-227">PrevRow</span><span class="sxs-lookup"><span data-stu-id="21356-227">PrevRow</span></span></p></td>
<td><p><span data-ttu-id="21356-p114">Les données contenues dans la ligne précédente de la table ou de la requête. Si PrevRow est le premier appel sur un nouveau canal, les données contenues dans la dernière ligne de la table ou de la requête sont retournées. Si le premier enregistrement est la ligne en cours, l'appel PrevRow échoue..</span><span class="sxs-lookup"><span data-stu-id="21356-p114">The data in the previous row in the table or query. If PrevRow is the first request on a new channel, the data in the last row of the table or query is returned. If the first record is the current row, the request for PrevRow fails.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-231">FirstRow</span><span class="sxs-lookup"><span data-stu-id="21356-231">FirstRow</span></span></p></td>
<td><p><span data-ttu-id="21356-232">Les données contenues dans la première ligne de la table ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="21356-232">The data in the first row of the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-233">LastRow</span><span class="sxs-lookup"><span data-stu-id="21356-233">LastRow</span></span></p></td>
<td><p><span data-ttu-id="21356-234">Les données contenues dans la dernière ligne de la table ou de la requête.</span><span class="sxs-lookup"><span data-stu-id="21356-234">The data in the last row of the table or query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-235">FieldCount</span><span class="sxs-lookup"><span data-stu-id="21356-235">FieldCount</span></span></p></td>
<td><p><span data-ttu-id="21356-236">Le nombre de champs dans la table ou la requête.</span><span class="sxs-lookup"><span data-stu-id="21356-236">The number of fields in the table or query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21356-237">SQLText</span><span class="sxs-lookup"><span data-stu-id="21356-237">SQLText</span></span></p></td>
<td><p><span data-ttu-id="21356-238">Une instruction SQL qui représente la table ou requête.</span><span class="sxs-lookup"><span data-stu-id="21356-238">An SQL statement representing the table or query.</span></span> <span data-ttu-id="21356-239">Pour les tables, cet élément retourne une instruction SQL dans le formulaire &quot;sélectionnez `*` de <em>table</em>; &quot;.</span><span class="sxs-lookup"><span data-stu-id="21356-239">For tables, this item returns an SQL statement in the form &quot;SELECT `*` FROM <em>table</em>;&quot;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21356-240">SQLText;<em>n</em></span><span class="sxs-lookup"><span data-stu-id="21356-240">SQLText;<em>n</em></span></span></p></td>
<td><p><span data-ttu-id="21356-241">Une instruction SQL, <em>n</em>-de segments, qui représente la table ou requête, où <em>n</em> est un entier jusqu'à 256 caractères.</span><span class="sxs-lookup"><span data-stu-id="21356-241">An SQL statement, in <em>n</em>-character chunks, representing the table or query, where <em>n</em> is an integer up to 256.</span></span> <span data-ttu-id="21356-242">Par exemple, supposons qu’une requête est représentée par l’instruction SQL suivante : l’élément &quot;SQLText ; 7&quot; retourne les segments ci-dessous délimité par des tabulations : l’élément &quot;SQLText ; 7&quot; renvoie les segments délimité par des tabulations suivantes :</span><span class="sxs-lookup"><span data-stu-id="21356-242">For example, suppose a query is represented by the following SQL statement: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks: The item &quot;SQLText;7&quot; returns the following tab-delimited chunks:</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="21356-243">L'exemple suivant montre comment utiliser l'échange dynamique de données (DDE) dans une procédure Visual Basic pour demander des données d'une table de la base de données exemple Comptoirs et insérer ces données dans un fichier texte :</span><span class="sxs-lookup"><span data-stu-id="21356-243">The following example shows how you can use DDE in a Visual Basic procedure to request data from a table in the Northwind sample database and insert that data into a text file:</span></span>

```vb
    Sub NorthwindDDE 
        Dim intChan1 As Integer, intChan2 As Integer, intChan3 As Integer 
        Dim strResp1 As Variant, strResp2 As Variant, strResp3 As Variant 
     
        ' In a Visual Basic module, get data from Categories table, 
        ' Catalog query, and Orders table in Northwind.mdb. 
        ' Make sure database is open first. 
        intChan1 = DDEInitiate("MSAccess", "Northwind;TABLE Shippers") 
        intChan2 = DDEInitiate("MSAccess", "Northwind;QUERY Catalog") 
        intChan3 = DDEInitiate("MSAccess", "Northwind;SQL SELECT * " _ 
            & "FROM Orders " _ 
            & "WHERE OrderID > 10050;") 
     
        strResp1 = DDERequest(intChan1, "All") 
        strResp2 = DDERequest(intChan2, "FieldNames;T") 
        strResp3 = DDERequest(intChan3, "FieldNames;T") 
        DDETerminate intChan1 
        DDETerminate intChan2 
        DDETerminate intChan3 
     
        ' Insert data into text file. 
        Open "C:\DATA.TXT" For Append As #1 
        Print #1, strResp1 
        Print #1, strResp2 
        Print #1, strResp3 
        Close #1 
    End Sub
```
