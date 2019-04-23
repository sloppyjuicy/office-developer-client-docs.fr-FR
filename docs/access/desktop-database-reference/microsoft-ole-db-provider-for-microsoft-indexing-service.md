---
title: Fournisseur Microsoft OLE DB pour le service d'indexation Microsoft
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba27bfdf6cc1317b441e626c61784e2c50b589f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288917"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Fournisseur Microsoft OLE DB pour le service d’indexation Microsoft


**S’applique à** : Access 2013, Office 2013

Le fournisseur Microsoft OLE DB pour le service d'indexation Microsoft fournit un accès par programmation en lecture seule au système de fichiers et aux données Web indexées par le service d'indexation Microsoft. Les applications ADO peuvent émettre des requêtes SQL pour extraire du contenu et des informations sur les propriétés des fichiers.

Le fournisseur est libre de thread et utilise Unicode.

## <a name="connection-string-parameters"></a>Paramètres de la chaîne de connexion

Pour vous connecter à ce fournisseur, définissez l’argument **Provider=** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :

```vb 
 
MSIDXS 
```

La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.

## <a name="typical-connection-string"></a>Chaîne de connexion classique

Voici une chaîne de connexion classique pour ce fournisseur :

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

La chaîne est composée des mots clé suivants :

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
<td><p><strong>Provider</strong></p></td>
<td><p>Spécifie le fournisseur OLE DB pour le service d'indexation Microsoft. Ce mot clé est généralement le seul spécifié dans la chaîne de connexion.</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>Spécifie le nom du catalogue du service d'indexation. Si ce mot clé n'est pas spécifié, le catalogue système par défaut est utilisé.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>Spécifie un nombre unique 32 bits (par exemple, 1033) qui indique les préférences relatives à la langue de l'utilisateur. Ces préférences décrivent le format de la date et de l'heure, l'ordre alphabétique utilisé pour trier les éléments, le mode de comparaison des chaînes, et ainsi de suite. Si ce mot clé n'est pas spécifié, l'identificateur des paramètres régionaux par défaut est utilisé.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Texte de la commande

La syntaxe des requêtes SQL du service d'indexation est constituée d'extensions de l'instruction SQL-92 **SELECT** et des clauses **FROM** et **WHERE** associées. Les résultats de la requête sont renvoyés via des ensembles de lignes OLE DB, qui peuvent être utilisés par ADO et traités comme des objets [Recordset](recordset-object-ado.md).

Vous pouvez rechercher des mots ou des phrases exacts ou utiliser des caractères génériques pour rechercher un modèle ou le radical d'un mot. La logique de recherche peut être basée sur des décisions booléennes, des termes pondérés ou la proximité d'autres mots. Vous pouvez également effectuer une recherche en « texte libre » : les correspondances trouvées seront dans ce cas basées non plus sur des mots exacts mais sur la signification.

Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**).

## <a name="recordset-behavior"></a>Comportement des jeux d'enregistrements

Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet **Recordset** ouvert avec ce fournisseur. Seul le type de curseur statique (**adOpenStatic**) est disponible.

Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.

Disponibilité des propriétés ADO standard d'un **Recordset** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriété</p></th>
<th><p>Disponibilité</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Signet</a>*</p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>Toujours <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Toujours <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>Toujours <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions,</a></p></td>
<td><p>Non disponible</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>en lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>en lecture seule</p></td>
</tr>
</tbody>
</table>


\*Les signets doivent être activés sur le fournisseur pour que cette fonctionnalité existe sur le **Recordset**.

Disponibilité des méthodes ADO standard d'un **Recordset** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Méthode</p></th>
<th><p>Possibles?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">Méthodes</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Actualiser</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Compatible</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">Mettre à jour</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Non</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

Pour obtenir des détails spécifiques d’implémentation et des informations fonctionnelles sur le fournisseur Microsoft OLE DB pour le service d’indexation Microsoft, consultez le guide Microsoft OLE DB Programmer’s Reference (en anglais).

