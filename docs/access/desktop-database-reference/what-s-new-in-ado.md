---
title: Quelles sont les nouveautés dans ActiveX Data Objects (ADO)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 232af159c669968c9c3b4d3d65acbc181f958689
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998902"
---
# <a name="whats-new-in-ado"></a>Nouveautés dans ADO

**S’applique à**: Access 2013, Office 2013 
 
La version ADO 2.5 propose les nouvelles fonctionnalités suivantes ainsi qu'une documentation enrichie. Cette liste englobe ADO, ADO MD et ADOX.

## <a name="new-features"></a>Nouvelles fonctionnalités

- **[Enregistrements et flux](chapter-10-records-and-streams.md)**

  Cette version d’ADO introduit l’objet [Record](record-object-ado.md) , qui peut représenter et gérer des éléments comme les répertoires et fichiers d’un système de fichiers et dossiers et messages d’un système de messagerie. L'objet **Record** peut également représenter une ligne d'un [Recordset](recordset-object-ado.md), bien que les objets **Record** et **Recordset** aient des méthodes et des propriétés différentes.

  Le nouvel objet [Stream](stream-object-ado.md) fournit les moyens de lire, d'écrire et de gérer le flux binaire d'octets ou de texte qui compose un flux de message ou de fichier.

- **[Utilisation d’URL](absolute-and-relative-urls.md)**

  Cette version introduit également l'utilisation d'URL (Uniform Resource Locators) à la place des chaînes de connexion et du texte de commande pour nommer des objets de magasin de données. Ces URL peuvent être employées avec les objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec les nouveaux objets **Record** et **Stream**.

  La nouvelle version d’ADO prend également en charge des fournisseurs OLE DB qui identifient leurs propres schémas d’URL. Par exemple, le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)*,* qui accède au système de fichiers Windows 2000, identifie le schéma HTTP existant.

- **[Champs spéciaux pour les fournisseurs de sources de documents](records-and-provider-supplied-fields.md)**

  Une classe spéciale de fournisseurs, appelée fournisseurs de *sources de documents* , gérer les documents et dossiers. Lorsqu'un objet **Record** représente un document ou lorsqu'un objet **Recordset** représente un dossier de documents, le fournisseur de source de documents remplit ces objets d'un ensemble de champs unique qui décrit les caractéristiques du document. Ces champs constituent une *ressource* **Record** ou **Recordset**.

## <a name="new-reference-topics"></a>Nouvelles rubriques de référence

### <a name="properties"></a>Propriétés

Les nouvelles propriétés suivantes sont fournies dans cette version.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Propriété</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Jeu de caractères</a></p></td>
<td><p>Indique dans quel jeu de caractères le contenu d'un objet <strong>Stream</strong> de texte doit être traduit.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Indique si la position actuelle est à la fin du flux.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets <strong>Stream</strong> textuels.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Indique les autorisations disponibles pour la modification des données d'un objet <strong>Connection</strong>, <strong>Enregistrement</strong> ou <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Indique la chaîne d'URL absolue qui pointe vers l'objet <strong>Record</strong> parent de l'objet <strong>Record</strong> actif.</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Indique la position actuelle dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Indique le type de l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Taille</a></p></td>
<td><p>Indique la taille du flux en nombre d'octets.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Indique l'entité représentée par l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé. Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">Type</a></p></td>
<td><p>Indique le type des données contenues dans l'objet <strong>Stream</strong> (binaire ou texte).</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Méthodes

Les nouvelles méthodes suivantes sont fournies dans cette version.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Méthode</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Copie un fichier ou un répertoire, avec tout son contenu, dans un autre emplacement.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copie le nombre spécifié de caractères ou d’octets (selon le <strong>Type</strong>) dans <strong>l’objet</strong> <strong>flux de données</strong> à un autre objet <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Vider</a></p></td>
<td><p>Force le contenu de l'objet <strong>Stream</strong> encore présent dans la mémoire tampon ADO dans l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">La méthode LoadFromFile</a></p></td>
<td><p>Charge le contenu d'un fichier existant dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Déplace un fichier ou un répertoire, avec tout son contenu, vers un autre emplacement.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">Open</a></p></td>
<td><p>Ouvre un objet <strong>Record</strong> existant ou crée un fichier ou un répertoire.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open</a></p></td>
<td><p>Ouvre un objet <strong>Stream</strong> pour manipuler des flux de données binaires ou de texte.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lit un nombre spécifié d'octets dans un objet <strong>Stream</strong> binaire.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lit un nombre spécifié de caractères dans un objet <strong>Stream</strong> de texte.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">Méthode SaveToFile</a></p></td>
<td><p>Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Définit la position qui représente la fin du flux.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Saute une ligne complète lors de la lecture d'un objet <strong>Stream</strong> de texte.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Écrit des données binaires dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Écrit une chaîne de texte spécifiée dans un objet <strong>Stream</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>Nouvelle documentation et documentation enrichie

- **[Rubriques d’exemples de code](ado-code-examples.md)**

  Les exemples ont été développées pour contenir les exemples de code écrits en Microsoft Visual C++ et Microsoft Visual J ++. Vous pouvez copier et coller ces exemples dans votre éditeur.

- **[Rubriques de fournisseur](appendix-a-providers.md)**

  Une nouvelle rubrique, qui explique comment utiliser ADO avec le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), a été ajoutée.

- **[Programmation avec ADO](appendix-c-programming-with-ado.md)**

  Cette nouvelle section contient des conseils et des astuces pour l'utilisation d'ADO avec différents langages de programmation. Il contient les index existants de la syntaxe pour les Extensions Visual C++ pour ADO et ADO/WFC, ainsi que des informations pour les développeurs utilisant Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, ou Microsoft Visual J ++.

