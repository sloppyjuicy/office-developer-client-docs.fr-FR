---
title: Fournisseur Microsoft OLE DB pour le service Microsoft Active Directory
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7ea95d40d10823de22b7496615a4fddb3e2860c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593963"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Fournisseur Microsoft OLE DB pour Microsoft Active Directory Service

**S’applique à** : Access 2013, Office 2013

Le fournisseur ADSI (Microsoft Active Directory Service Interfaces) permet à ADO de se connecter à des services d'annuaire hétérogènes via ADSI. Les applications ADO bénéficient ainsi d'un accès en lecture seule aux services d'annuaire de Microsoft Windows NT 4.0 et de Microsoft Windows 2000, ainsi qu'aux services d'annuaire Novell ou compatibles avec LDAP. ADSI est basé sur un modèle de fournisseur ; par conséquent, si un nouveau fournisseur donne accès à un autre annuaire, l'application ADO pourra y accéder de façon transparente. Le fournisseur ADSI est libre de thread et utilise Unicode.

## <a name="connection-string-parameters"></a>Paramètres de la chaîne de connexion

Pour vous connecter à ce fournisseur, définissez l’argument **Provider** de la propriété [ConnectionString](connectionstring-property-ado.md) sur :

```vb 
 
ADSDSOObject 
```

La lecture de la propriété [Provider](provider-property-ado.md) renverra également cette chaîne.

## <a name="typical-connection-string"></a>Chaîne de connexion classique

Voici une chaîne de connexion classique pour ce fournisseur :

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
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
<td><p>Spécifie le fournisseur OLE DB pour le service Microsoft Active Directory.</p></td>
</tr>
<tr class="even">
<td><p><strong>User ID</strong></p></td>
<td><p>Spécifie le nom de l'utilisateur. Si ce mot clé n'est pas spécifié, les paramètres de connexion actuels sont utilisés.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Spécifie le mot de passe de l'utilisateur. Si ce mot clé n'est pas spécifié, les paramètres de connexion actuels sont utilisés.</p></td>
</tr>
</tbody>
</table>


**Texte de la commande**

Dans la syntaxe suivante, une chaîne de texte de commande en quatre parties est reconnue par le fournisseur :

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Root</em></p></td>
<td><p>Indique l'objet <strong>ADsPath</strong> à partir duquel lancer la recherche (c'est-à-dire la racine de la recherche).</p></td>
</tr>
<tr class="even">
<td><p><em>Filtre</em></p></td>
<td><p>Indique le filtre de recherche au format RFC 1960.</p></td>
</tr>
<tr class="odd">
<td><p><em>Attributs</em></p></td>
<td><p>Indique une liste délimitée par des virgules d'attributs à renvoyer.</p></td>
</tr>
<tr class="even">
<td><p><em>Scope</em></p></td>
<td><p>Facultatif. <strong>Chaîne</strong> spécifiant l'étendue de la recherche. Il peut s’agit de l’une des opérations suivantes : Base — Rechercher uniquement l’objet de base (racine de la recherche).<br />
OneLevel : recherchez un seul niveau.<br />
Sous-arbre : recherchez l’intégralité de la sous-arbre.</p></td>
</tr>
</tbody>
</table>


Par exemple :

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

Le fournisseur prend aussi en charge SQL SELECT pour le texte de commande. Par exemple :

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

Le fournisseur n’accepte pas les appels de procédures stockées ni les noms de table simples (par exemple, la propriété [CommandType](commandtype-property-ado.md) sera toujours **adCmdText**). Pour obtenir une description plus complète des éléments du texte de commande, consultez la documentation ADSI.

## <a name="recordset-behavior"></a>Comportement des jeux d'enregistrements

Les tableaux suivants répertorient les fonctionnalités disponibles pour un objet [Recordset](recordset-object-ado.md) ouvert avec ce fournisseur. Seul le type de curseur statique (**adOpenStatic**) est disponible.

Pour obtenir des informations détaillées sur le comportement de l'objet **Recordset** en fonction de la configuration de votre fournisseur, exécutez la méthode [Supports](supports-method-ado.md) et passez en revue la collection [Properties](properties-collection-ado.md) du **Recordset** pour voir s'il existe des propriétés dynamiques spécifiques à ce fournisseur.

Disponibilité des propriétés ADO standard d'un **Recordset** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Property</p></th>
<th><p>Disponibilité</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>lecture/écriture</p></td>
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
<td><p>lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filtre</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Non disponible</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>lecture seule</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">État</a></p></td>
<td><p>lecture seule</p></td>
</tr>
</tbody>
</table>


Disponibilité des méthodes ADO standard d'un **Recordset** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Méthode</p></th>
<th><p>Disponible ?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>Non</p></td>
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
<td><p><a href="delete-method-ado-recordset.md">Supprimer</a></p></td>
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
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Ouvert</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Actualiser</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Prend en charge</a></p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Mise à jour</a></p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Non</p></td>
</tr>
</tbody>
</table>

