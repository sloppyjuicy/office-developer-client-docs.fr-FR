---
title: Fournisseur Microsoft OLE DB d'accès à distance (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 907686e0dcd1be8ef24747d9ff655a7ff0f7f91f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470949"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a><span data-ttu-id="911dc-102">Fournisseur Microsoft OLE DB d'accès à distance (fournisseur de service ADO)</span><span class="sxs-lookup"><span data-stu-id="911dc-102">Microsoft OLE DB Remoting Provider (ADO Service Provider)</span></span>

<span data-ttu-id="911dc-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="911dc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="911dc-p101">Le fournisseur Microsoft OLE DB d'accès à distance permet à l'utilisateur local d'un ordinateur client d'appeler des fournisseurs de données sur un ordinateur distant. Spécifiez les paramètres du fournisseur de données pour l'ordinateur distant comme vous le feriez si vous étiez un utilisateur local de cet ordinateur. Spécifiez ensuite les paramètres utilisés par le fournisseur d'accès à distance pour accéder à l'ordinateur distant. Vous accéderez ainsi à l'ordinateur distant comme si vous étiez un utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="911dc-p101">The Microsoft OLE DB Remoting Provider enables a local user on a client machine to invoke data providers on a remote machine. Specify the data provider parameters for the remote machine as you would if you were a local user on the remote machine. Then specify the parameters used by the Remoting Provider to access the remote machine. The resulting effect is that you will access the remote machine as if you were a local user.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="911dc-108">Mot clé du fournisseur</span><span class="sxs-lookup"><span data-stu-id="911dc-108">Provider Keyword</span></span>

<span data-ttu-id="911dc-p102">Pour appeler le fournisseur Microsoft OLE DB d'accès à distance, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion. (Vous remarquerez que le nom du fournisseur contient un espace.)</span><span class="sxs-lookup"><span data-stu-id="911dc-p102">To invoke the OLE DB Remoting Provider, specify the following keyword and value in the connection string. (Note the blank space in the provider name.)</span></span>

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a><span data-ttu-id="911dc-111">Mots clé supplémentaires</span><span class="sxs-lookup"><span data-stu-id="911dc-111">Additional Keywords</span></span>

<span data-ttu-id="911dc-112">Lorsque ce fournisseur de services est appelé, les mots clés supplémentaires suivants sont pertinents.</span><span class="sxs-lookup"><span data-stu-id="911dc-112">When this service provider is invoked, the following additional keywords are relevant.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="911dc-113">Mot clé</span><span class="sxs-lookup"><span data-stu-id="911dc-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="911dc-114">Description</span><span class="sxs-lookup"><span data-stu-id="911dc-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="911dc-115"><strong>Data Source</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-115"><strong>Data Source</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-116">Spécifie le nom de la source de données à distance.</span><span class="sxs-lookup"><span data-stu-id="911dc-116">Specifies the name of the remote data source.</span></span> <span data-ttu-id="911dc-117">Il est passé pour le fournisseur OLE DB d’accès à distance pour le traitement.</span><span class="sxs-lookup"><span data-stu-id="911dc-117">It is passed to the OLE DB Remoting Provider for processing.</span></span> <span data-ttu-id="911dc-118">Ce mot clé est équivalent à la propriété <a href="connect-property-rds.md">Connect</a> de l’objet <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="911dc-118">This keyword is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object's <a href="connect-property-rds.md">Connect</a> property.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a><span data-ttu-id="911dc-119">Propriétés dynamiques</span><span class="sxs-lookup"><span data-stu-id="911dc-119">Dynamic Properties</span></span>

<span data-ttu-id="911dc-120">Lorsque ce fournisseur de services est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md).</span><span class="sxs-lookup"><span data-stu-id="911dc-120">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="911dc-121">Nom de la propriété dynamique</span><span class="sxs-lookup"><span data-stu-id="911dc-121">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="911dc-122">Description</span><span class="sxs-lookup"><span data-stu-id="911dc-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="911dc-123"><strong>DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-123"><strong>DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-124">Indique le Mode DataFactory.</span><span class="sxs-lookup"><span data-stu-id="911dc-124">Indicates the DataFactory Mode.</span></span> <span data-ttu-id="911dc-125">Chaîne qui spécifie la version souhaitée de l’objet <a href="datafactory-object-rdsserver.md">DataFactory</a> sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="911dc-125">A string that specifies the desired version of the <a href="datafactory-object-rdsserver.md">DataFactory</a> object on the server.</span></span> <span data-ttu-id="911dc-126">Définir cette propriété avant d’ouvrir une connexion pour demander une version spécifique de l' <strong>objet DataFactory</strong>.</span><span class="sxs-lookup"><span data-stu-id="911dc-126">Set this property before opening a connection to request a particular version of the <strong>DataFactory</strong>.</span></span> <span data-ttu-id="911dc-127">Si la version demandée n’est pas disponible, s’être tenté d’utiliser la version précédente.</span><span class="sxs-lookup"><span data-stu-id="911dc-127">If the requested version is not available, an attempt will be made to use the preceding version.</span></span> <span data-ttu-id="911dc-128">S’il n’existe aucune version précédente, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="911dc-128">If there is no preceding version, an error will occur.</span></span> <span data-ttu-id="911dc-129">Si la <strong>valeur de DFMode</strong> est inférieure à la version disponible, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="911dc-129">If <strong>DFMode</strong> is less than the available version, an error will occur.</span></span> <span data-ttu-id="911dc-130">Cette propriété est en lecture seule après qu’une connexion est établie.</span><span class="sxs-lookup"><span data-stu-id="911dc-130">This property is read-only after a connection is made.</span></span> <span data-ttu-id="911dc-131">Les valeurs valides sont les valeurs de chaîne suivantes :</span><span class="sxs-lookup"><span data-stu-id="911dc-131">Can be one of the following valid string values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="911dc-132">&quot;25&quot; — version 2.5 (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="911dc-132">&quot;25&quot; — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="911dc-133">&quot;21&quot; — version 2.1</span><span class="sxs-lookup"><span data-stu-id="911dc-133">&quot;21&quot; — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="911dc-134">&quot;20&quot; — version 2.0</span><span class="sxs-lookup"><span data-stu-id="911dc-134">&quot;20&quot; — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="911dc-135">&quot;15&quot; — version 1.5</span><span class="sxs-lookup"><span data-stu-id="911dc-135">&quot;15&quot; — Version 1.5</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911dc-136"><strong>Command Properties</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-136"><strong>Command Properties</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-p105">Indique les valeurs qui seront ajoutées à la chaîne de propriétés de commande (ensemble de lignes) envoyées au serveur par le fournisseur MS d'accès à distance.

La valeur par défaut pour cette chaîne est vt_empty.</span><span class="sxs-lookup"><span data-stu-id="911dc-p105">Indicates values that will be added to the string of command (rowset) properties sent to the server by the MS Remote provider. The default value for this string is vt_empty.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="911dc-139"><strong>Current DFMode</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-139"><strong>Current DFMode</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-140">Indique le numéro de version réel du <strong>DataFactory</strong> sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="911dc-140">Indicates the actual version number of the <strong>DataFactory</strong> on the server.</span></span> <span data-ttu-id="911dc-141">Vérifier cette propriété pour vérifier si la version demandée dans la propriété <strong>DFMode</strong> a été respectée.</span><span class="sxs-lookup"><span data-stu-id="911dc-141">Check this property to see if the version requested in the <strong>DFMode</strong> property was honored.</span></span> <span data-ttu-id="911dc-142">Les valeurs valides sont les entiers longs suivants :</span><span class="sxs-lookup"><span data-stu-id="911dc-142">Can be one of the following valid Long integer values:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="911dc-143">25 — Version 2.5 (valeur par défaut)</span><span class="sxs-lookup"><span data-stu-id="911dc-143">25 — Version 2.5 (Default)</span></span></p></li>
<li><p><span data-ttu-id="911dc-144">21 — Version 2.1</span><span class="sxs-lookup"><span data-stu-id="911dc-144">21 — Version 2.1</span></span></p></li>
<li><p><span data-ttu-id="911dc-145">20 — Version 2.0</span><span class="sxs-lookup"><span data-stu-id="911dc-145">20 — Version 2.0</span></span></p></li>
<li><p><span data-ttu-id="911dc-146">15 — Version 1.5</span><span class="sxs-lookup"><span data-stu-id="911dc-146">15 — Version 1.5</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="911dc-147">Ajout de &quot;DFMode = 20 ; &quot; à votre connexion de chaîne lorsque vous utilisez le fournisseur <strong>MSRemote, vous</strong> peut améliorer les performances de votre serveur lors de la mise à jour des données.</span><span class="sxs-lookup"><span data-stu-id="911dc-147">Adding &quot;DFMode=20;&quot; to your connection string when using the <strong>MSRemote</strong> provider can improve your server's performance when updating data.</span></span> <span data-ttu-id="911dc-148">Avec ce paramètre, l'objet <strong>RDSServer.DataFactory</strong> utilise moins de ressources au niveau du serveur.</span><span class="sxs-lookup"><span data-stu-id="911dc-148">With this setting, the <strong>RDSServer.DataFactory</strong> object on the server uses a less resource-intensive mode.</span></span> <span data-ttu-id="911dc-149">Toutefois, les fonctions suivantes ne sont pas disponibles dans cette configuration :</span><span class="sxs-lookup"><span data-stu-id="911dc-149">However, the following features are not available in this configuration:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="911dc-150">utilisation de requêtes paramétrées ;</span><span class="sxs-lookup"><span data-stu-id="911dc-150">Using parameterized queries.</span></span></p></li>
<li><p><span data-ttu-id="911dc-151">obtention d'informations de paramètres et de colonnes avant l'appel de la méthode <strong>Execute</strong>;</span><span class="sxs-lookup"><span data-stu-id="911dc-151">Getting parameter or column information before calling the <strong>Execute</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="911dc-152">affectation de la valeur <strong>True</strong> à <strong>Transact Updates</strong>;</span><span class="sxs-lookup"><span data-stu-id="911dc-152">Setting <strong>Transact Updates</strong> to <strong>True</strong>.</span></span></p></li>
<li><p><span data-ttu-id="911dc-153">obtention de l'état des lignes ;</span><span class="sxs-lookup"><span data-stu-id="911dc-153">Getting row status.</span></span></p></li>
<li><p><span data-ttu-id="911dc-154">appel de la méthode <strong>Resync</strong> ;</span><span class="sxs-lookup"><span data-stu-id="911dc-154">Calling the <strong>Resync</strong> method.</span></span></p></li>
<li><p><span data-ttu-id="911dc-155">actualisation (explicite ou automatique) via la propriété <strong>Update Resync</strong> ;</span><span class="sxs-lookup"><span data-stu-id="911dc-155">Refreshing (explicitly or automatically) via the <strong>Update Resync</strong> property.</span></span></p></li>
<li><p><span data-ttu-id="911dc-156">définition des propriétés <strong>Command</strong> ou <strong>Recordset</strong> ;</span><span class="sxs-lookup"><span data-stu-id="911dc-156">Setting <strong>Command</strong> or <strong>Recordset</strong> properties.</span></span></p></li>
<li><p><span data-ttu-id="911dc-157">utilisation d' <strong>adCmdTableDirect</strong>.</span><span class="sxs-lookup"><span data-stu-id="911dc-157">Using <strong>adCmdTableDirect</strong>.</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911dc-158"><strong>Gestionnaire</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-158"><strong>Handler</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-159">Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend les fonctionnalités de <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>et tous les paramètres utilisés par le gestionnaire<em>,</em> tous les séparées par des virgules (&quot;,&quot;).</span><span class="sxs-lookup"><span data-stu-id="911dc-159">Indicates the name of a server-side customization program (or handler) that extends the functionality of the <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>, and any parameters used by the handler<em>,</em> all separated by commas (&quot;,&quot;).</span></span> <span data-ttu-id="911dc-160">Valeur de type <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="911dc-160">A <strong>String</strong> value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="911dc-161"><strong>Internet Timeout</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-161"><strong>Internet Timeout</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-p109">Indique le délai d'attente maximum en millisecondes pour qu'une requête effectue un aller-retour au serveur.

(La valeur par défaut est de 5 minutes).</span><span class="sxs-lookup"><span data-stu-id="911dc-p109">Indicates the maximum number of milliseconds to wait for a request to travel to and from the server. (The default is 5 minutes.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911dc-164"><strong>Remote Provider</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-164"><strong>Remote Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-165">Indique le nom du fournisseur de données à utiliser sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="911dc-165">Indicates the name of the data provider to be used on the remote server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="911dc-166"><strong>Remote Server</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-166"><strong>Remote Server</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-p110">Indique le nom du serveur et le protocole de communication à utiliser pour cette connexion. Cette propriété équivaut à la propriété <a href="server-property-rds.md">Server</a> de l’objet <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</span><span class="sxs-lookup"><span data-stu-id="911dc-p110">Indicates the server name and communication protocol to be used by this connection. This property is equivalent to the <a href="datacontrol-object-rds.md">RDS.DataControl</a> object <a href="server-property-rds.md">Server</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="911dc-169"><strong>Transact Updates</strong></span><span class="sxs-lookup"><span data-stu-id="911dc-169"><strong>Transact Updates</strong></span></span></p></td>
<td><p><span data-ttu-id="911dc-p111">Le fait de définir cette valeur sur True indique que lorsque la méthode <a href="updatebatch-method-ado.md">UpdateBatch</a> est exécutée sur le serveur, cette opération s’effectue dans une transaction. La valeur par défaut de cette propriété dynamique booléenne est False.</span><span class="sxs-lookup"><span data-stu-id="911dc-p111">When set to True, this value indicates that when <a href="updatebatch-method-ado.md">UpdateBatch</a> is performed on the server, it will be done inside a transaction. The default value for this Boolean dynamic property is False.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="911dc-p112">Vous pouvez aussi définir des propriétés dynamiques en écriture en spécifiant leurs noms en tant que mots clé dans la chaîne de connexion. Par exemple définissez la propriété dynamique **Internet Timeout** sur cinq secondes en spécifiant :</span><span class="sxs-lookup"><span data-stu-id="911dc-p112">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, set the **Internet Timeout** dynamic property to five seconds by specifying:</span></span>

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

<span data-ttu-id="911dc-p113">Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu'index de la propriété **Properties**. Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique **Internet Timeout**, puis définir une nouvelle valeur de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="911dc-p113">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** property. For example, get and print the current value of the **Internet Timeout** dynamic property, and then set a new value, like this:</span></span>

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a><span data-ttu-id="911dc-176">Remarques</span><span class="sxs-lookup"><span data-stu-id="911dc-176">Remarks</span></span>

<span data-ttu-id="911dc-177">Dans ADO 2.0, le fournisseur OLE DB d’accès à distance ne pouvait être spécifié dans le paramètre *ActiveConnection* de la méthode **Open** de l’objet [Recordset](recordset-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="911dc-177">In ADO 2.0, the OLE DB Remoting Provider could only be specified in the *ActiveConnection* parameter of the [Recordset](recordset-object-ado.md) object **Open** method.</span></span> <span data-ttu-id="911dc-178">À partir d’ADO 2.1, le fournisseur peut également être spécifié dans le paramètre *ConnectionString* de la méthode **Open** de l’objet [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="911dc-178">Starting with ADO 2.1, the provider may also be specified in the *ConnectionString* parameter of the [Connection](connection-object-ado.md) object **Open** method.</span></span>

<span data-ttu-id="911dc-179">L'équivalent de la propriété **SQL** de l'objet [RDS.DataControl](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) n'est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="911dc-179">The equivalent of the **RDS.DataControl** object [SQL](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) property is not available.</span></span> <span data-ttu-id="911dc-180">L’argument *Source de* la méthode **Open** d’objet [Recordset](recordset-object-ado.md) est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="911dc-180">The [Recordset](recordset-object-ado.md) object **Open** method *Source* argument is used instead.</span></span>

<span data-ttu-id="911dc-181">Le fait de spécifier « ...;Remote Provider=MS Remote;... » génère un scénario à quatre niveaux. Les scénarios de plus de trois niveaux n'ont pas été testés et ne sont en principe pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="911dc-181">Specifying "...;Remote Provider=MS Remote;..." would create a four-tier scenario.Scenarios beyond three tiers have not been tested and should not be needed.</span></span>

## <a name="example"></a><span data-ttu-id="911dc-182">Exemple</span><span class="sxs-lookup"><span data-stu-id="911dc-182">Example</span></span>

<span data-ttu-id="911dc-p116">Cet exemple adresse une requête à la table **authors** de la base de données **pubs** sur un serveur appelé *YourServer*. Les noms de la source de données et du serveur distants sont fournis dans la méthode [Open](open-method-ado-connection.md) de l’objet [Connection](connection-object-ado.md) ; la requête SQL est spécifiée dans la méthode [Open](open-method-ado-recordset.md) de l’objet [Recordset](recordset-object-ado.md). Un objet **Recordset** est renvoyé, modifié et utilisé pour mettre à jour la source de données.</span><span class="sxs-lookup"><span data-stu-id="911dc-p116">This example performs a query on the **authors** table of the **pubs** database on a server named, *YourServer*. The names of the remote data source and remote server are provided in the [Connection](connection-object-ado.md) object [Open](open-method-ado-connection.md) method, and the SQL query is specified in the [Recordset](recordset-object-ado.md) object [Open](open-method-ado-recordset.md) method. A **Recordset** object is returned, edited, and used to update the data source.</span></span>

```vb 
 
Dim rs as New ADODB.Recordset 
Dim cn as New ADODB.Connection 
cn.Open  "Provider=MS Remote;Data Source=pubs;" & _ 
         "Remote Server=https://YourServer" 
rs.Open "SELECT * FROM authors", cn 
...                'Edit the recordset 
rs.UpdateBatch     'Equivalent of RDS SubmitChanges 
... 
```

