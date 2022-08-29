---
title: Fournisseur Microsoft OLE DB d'accès à distance (fournisseur de service ADO)
TOCTitle: Microsoft OLE DB Remoting Provider (ADO Service Provider)
ms:assetid: f39bd83d-8c2c-302e-16e3-0fae50f89fbc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250238(v=office.15)
ms:contentKeyID: 48548673
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ab6e02da05ee47f6e296f7a300b82ed6406029ba
ms.sourcegitcommit: 7c1e7389b18d4f067a69b992ac6c876b5e0441b3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2022
ms.locfileid: "67365830"
---
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Fournisseur d’accès à distance Microsoft OLE DB (fournisseur de services ADO)

**S’applique à** : Access 2013, Office 2013

Le fournisseur Microsoft OLE DB d'accès à distance permet à l'utilisateur local d'un ordinateur client d'appeler des fournisseurs de données sur un ordinateur distant. Spécifiez les paramètres du fournisseur de données pour l'ordinateur distant comme vous le feriez si vous étiez un utilisateur local de cet ordinateur. Spécifiez ensuite les paramètres utilisés par le fournisseur d'accès à distance pour accéder à l'ordinateur distant. Vous accéderez ainsi à l'ordinateur distant comme si vous étiez un utilisateur local.

## <a name="provider-keyword"></a>Mot clé du fournisseur

Pour appeler le fournisseur Microsoft OLE DB d'accès à distance, spécifiez le mot clé et la valeur suivants dans la chaîne de connexion. (Vous remarquerez que le nom du fournisseur contient un espace.)

```sql 
 
"Provider=MS Remote" 
```

## <a name="additional-keywords"></a>Mots clé supplémentaires

Lorsque ce fournisseur de services est appelé, les mots clés supplémentaires suivants sont pertinents.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Mot clé</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Data Source</strong></p></td>
<td><p>Spécifie le nom de la source de données distante. Il est transmis au fournisseur OLE DB d'accès à distance pour le traitement. Ce mot clé est équivalent à la propriété <a href="connect-property-rds.md">Connect</a> de l’objet <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Propriétés dynamiques

Lorsque ce fournisseur de services est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de la propriété dynamique</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>DFMode</strong></p></td>
<td><p>Indique le mode DataFactory. Chaîne qui spécifie la version souhaitée de l’objet <a href="datafactory-object-rdsserver.md">DataFactory</a> sur le serveur. Définissez cette propriété avant d’ouvrir une connexion pour demander une version particulière du <strong>DataFactory</strong>. Si la version souhaitée n’est pas disponible, une tentative d’utilisation d’une version précédente est effectuée. S’il n’existe pas de version précédente, une erreur est générée. Si la valeur de <strong>DFMode</strong> est inférieure à la version disponible, une erreur est générée. Cette propriété passe en lecture seule une fois la connexion établie. Les valeurs valides sont les valeurs de chaîne suivantes :</p>
<p></p>
<ul>
<li><p>&quot;25&quot; — Version 2.5 (par défaut)</p></li>
<li><p>&quot;21&quot; — Version 2.1</p></li>
<li><p>&quot;20&quot; — Version 2.0</p></li>
<li><p>&quot;15&quot; — Version 1.5</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Command Properties</strong></p></td>
<td><p>Indique les valeurs qui seront ajoutées à la chaîne de propriétés de commande (ensemble de lignes) envoyées au serveur par le fournisseur MS d'accès à distance.

La valeur par défaut pour cette chaîne est vt_empty.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Current DFMode</strong></p></td>
<td><p>Indique le numéro de version réel du <strong>DataFactory</strong> sur le serveur. Consultez cette propriété pour vérifier si la version demandée dans la propriété <strong>DFMode</strong> a été respectée. Les valeurs valides sont les entiers longs suivants :</p>
<p></p>
<ul>
<li><p>25 — Version 2.5 (valeur par défaut)</p></li>
<li><p>21 — Version 2.1</p></li>
<li><p>20 — Version 2.0</p></li>
<li><p>15 — Version 1.5</p></li>
</ul>
<p></p>
<p>L’ajout &quot;de DFMode=20;&quot; à votre chaîne de connexion lors de l’utilisation du fournisseur <strong>MSRemote</strong> peut améliorer les performances de votre serveur lors de la mise à jour des données. Avec ce paramètre, l'objet <strong>RDSServer.DataFactory</strong> utilise moins de ressources au niveau du serveur. Toutefois, les fonctions suivantes ne sont pas disponibles dans cette configuration :</p>
<p></p>
<ul>
<li><p>utilisation de requêtes paramétrées ;</p></li>
<li><p>obtention d'informations de paramètres et de colonnes avant l'appel de la méthode <strong>Execute</strong>;</p></li>
<li><p>affectation de la valeur <strong>True</strong> à <strong>Transact Updates</strong>;</p></li>
<li><p>obtention de l'état des lignes ;</p></li>
<li><p>appel de la méthode <strong>Resync</strong> ;</p></li>
<li><p>actualisation (explicite ou automatique) via la propriété <strong>Update Resync</strong> ;</p></li>
<li><p>définition des propriétés <strong>Command</strong> ou <strong>Recordset</strong> ;</p></li>
<li><p>Utilisation d'<strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Handler</strong></p></td>
<td><p>Indique le nom d’un programme de personnalisation côté serveur (ou gestionnaire) qui étend les fonctionnalités de <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a> et tous les paramètres utilisés par le gestionnaire<em>,</em> tous séparés par des virgules (&quot;,&quot;). Valeur <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Indique le délai d'attente maximum en millisecondes pour qu'une requête effectue un aller-retour au serveur. (La valeur par défaut est de 5 minutes).</p></td>
</tr>
<tr class="even">
<td><p><strong>Remote Provider</strong></p></td>
<td><p>Indique le nom du fournisseur de données à utiliser sur le serveur distant.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Remote Server</strong></p></td>
<td><p>Indique le nom du serveur et le protocole de communication à utiliser pour cette connexion. Cette propriété équivaut à la propriété <a href="server-property-rds.md">Server</a> de l’objet <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Transact Updates</strong></p></td>
<td><p>Le fait de définir cette valeur sur True indique que lorsque la méthode <a href="updatebatch-method-ado.md">UpdateBatch</a> est exécutée sur le serveur, cette opération s’effectue dans une transaction. La valeur par défaut de cette propriété dynamique booléenne est False.</p></td>
</tr>
</tbody>
</table>


Vous pouvez aussi définir des propriétés dynamiques en écriture en spécifiant leurs noms en tant que mots clé dans la chaîne de connexion. Par exemple définissez la propriété dynamique **Internet Timeout** sur cinq secondes en spécifiant :

```sql 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MS Remote;Internet Timeout=5000" 
```

Vous pouvez également définir ou extraire une propriété dynamique en spécifiant son nom en tant qu'index de la propriété **Properties**. Par exemple, vous pouvez obtenir et imprimer la valeur actuelle de la propriété dynamique **Internet Timeout**, puis définir une nouvelle valeur de la façon suivante :

```sql 
 
Debug.Print cn.Properties("Internet Timeout") 
cn.Properties("Internet Timeout") = 5000 
```

## <a name="remarks"></a>Remarques

Dans ADO 2.0, le fournisseur OLE DB d’accès à distance ne pouvait être spécifié que dans le paramètre *ActiveConnection* de la méthode **Open** de l’objet [Recordset](recordset-object-ado.md). À partir d’ADO 2.1, le fournisseur peut également être spécifié dans le paramètre *ConnectionString* de la méthode **Open** de l’objet [Connection](connection-object-ado.md).

L’équivalent de la propriété [SQL](/office/vba/access/concepts/miscellaneous/sql-property-ado) de l’objet **RDS.DataControl** n’est pas disponible. On utilise à la place l’argument *Source* de la méthode **Open** de l’objet [Recordset](recordset-object-ado.md).

Le fait de spécifier « ...;Remote Provider=MS Remote;... » génère un scénario à quatre niveaux. Les scénarios de plus de trois niveaux n'ont pas été testés et ne sont en principe pas nécessaires.

## <a name="example"></a>Exemple

Cet exemple adresse une requête à la table **authors** de la base de données **pubs** sur un serveur appelé *YourServer*. Les noms de la source de données et du serveur distants sont fournis dans la méthode [Open](open-method-ado-connection.md) de l’objet [Connection](connection-object-ado.md) ; la requête SQL est spécifiée dans la méthode [Open](open-method-ado-recordset.md) de l’objet [Recordset](recordset-object-ado.md). Un objet **Recordset** est renvoyé, modifié et utilisé pour mettre à jour la source de données.

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

