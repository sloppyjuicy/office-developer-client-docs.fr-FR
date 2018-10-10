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
# <a name="microsoft-ole-db-remoting-provider-ado-service-provider"></a>Fournisseur Microsoft OLE DB d'accès à distance (fournisseur de service ADO)

**S’applique à**: Access 2013 | Office 2013

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
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Spécifie le nom de la source de données à distance. Il est passé pour le fournisseur OLE DB d’accès à distance pour le traitement. Ce mot clé est équivalent à la propriété <a href="connect-property-rds.md">Connect</a> de l’objet <a href="datacontrol-object-rds.md">RDS.DataControl</a>.</p></td>
</tr>
</tbody>
</table>


## <a name="dynamic-properties"></a>Propriétés dynamiques

Lorsque ce fournisseur de services est appelé, les propriétés dynamiques suivantes sont ajoutées à la collection [Properties](connection-object-ado.md) de l'objet [Connection](properties-collection-ado.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
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
<td><p>Indique le Mode DataFactory. Chaîne qui spécifie la version souhaitée de l’objet <a href="datafactory-object-rdsserver.md">DataFactory</a> sur le serveur. Définir cette propriété avant d’ouvrir une connexion pour demander une version spécifique de l' <strong>objet DataFactory</strong>. Si la version demandée n’est pas disponible, s’être tenté d’utiliser la version précédente. S’il n’existe aucune version précédente, une erreur se produit. Si la <strong>valeur de DFMode</strong> est inférieure à la version disponible, une erreur se produit. Cette propriété est en lecture seule après qu’une connexion est établie. Les valeurs valides sont les valeurs de chaîne suivantes :</p>
<p></p>
<ul>
<li><p>&quot;25&quot; — version 2.5 (valeur par défaut)</p></li>
<li><p>&quot;21&quot; — version 2.1</p></li>
<li><p>&quot;20&quot; — version 2.0</p></li>
<li><p>&quot;15&quot; — version 1.5</p></li>
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
<td><p>Indique le numéro de version réel du <strong>DataFactory</strong> sur le serveur. Vérifier cette propriété pour vérifier si la version demandée dans la propriété <strong>DFMode</strong> a été respectée. Les valeurs valides sont les entiers longs suivants :</p>
<p></p>
<ul>
<li><p>25 — Version 2.5 (valeur par défaut)</p></li>
<li><p>21 — Version 2.1</p></li>
<li><p>20 — Version 2.0</p></li>
<li><p>15 — Version 1.5</p></li>
</ul>
<p></p>
<p>Ajout de &quot;DFMode = 20 ; &quot; à votre connexion de chaîne lorsque vous utilisez le fournisseur <strong>MSRemote, vous</strong> peut améliorer les performances de votre serveur lors de la mise à jour des données. Avec ce paramètre, l'objet <strong>RDSServer.DataFactory</strong> utilise moins de ressources au niveau du serveur. Toutefois, les fonctions suivantes ne sont pas disponibles dans cette configuration :</p>
<p></p>
<ul>
<li><p>utilisation de requêtes paramétrées ;</p></li>
<li><p>obtention d'informations de paramètres et de colonnes avant l'appel de la méthode <strong>Execute</strong>;</p></li>
<li><p>affectation de la valeur <strong>True</strong> à <strong>Transact Updates</strong>;</p></li>
<li><p>obtention de l'état des lignes ;</p></li>
<li><p>appel de la méthode <strong>Resync</strong> ;</p></li>
<li><p>actualisation (explicite ou automatique) via la propriété <strong>Update Resync</strong> ;</p></li>
<li><p>définition des propriétés <strong>Command</strong> ou <strong>Recordset</strong> ;</p></li>
<li><p>utilisation d' <strong>adCmdTableDirect</strong>.</p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Gestionnaire</strong></p></td>
<td><p>Indique le nom d’un programme de personnalisation coté serveur (gestionnaire) qui étend les fonctionnalités de <a href="datafactory-object-rdsserver.md">RDSServer.DataFactory</a>et tous les paramètres utilisés par le gestionnaire<em>,</em> tous les séparées par des virgules (&quot;,&quot;). Valeur de type <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Internet Timeout</strong></p></td>
<td><p>Indique le délai d'attente maximum en millisecondes pour qu'une requête effectue un aller-retour au serveur.

(La valeur par défaut est de 5 minutes).</p></td>
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

Dans ADO 2.0, le fournisseur OLE DB d’accès à distance ne pouvait être spécifié dans le paramètre *ActiveConnection* de la méthode **Open** de l’objet [Recordset](recordset-object-ado.md) . À partir d’ADO 2.1, le fournisseur peut également être spécifié dans le paramètre *ConnectionString* de la méthode **Open** de l’objet [Connection](connection-object-ado.md) .

L'équivalent de la propriété **SQL** de l'objet [RDS.DataControl](https://msdn.microsoft.com/library/jj248989\(v=office.15\)) n'est pas disponible. L’argument *Source de* la méthode **Open** d’objet [Recordset](recordset-object-ado.md) est utilisé à la place.

Le fait de spécifier « ...;Remote Provider=MS Remote;... » génère un scénario à quatre niveaux. Les scénarios de plus de trois niveaux n'ont pas été testés et ne sont en principe pas nécessaires.

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

