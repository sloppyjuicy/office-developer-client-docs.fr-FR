---
title: Nouveautés d'ADO (ActiveX Data Objects)
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302610"
---
# <a name="whats-new-in-ado"></a>Nouveautés dans ADO

**S’applique à** : Access 2013, Office 2013 
 
La version ADO 2.5 propose les nouvelles fonctionnalités suivantes ainsi qu'une documentation enrichie. Cette liste englobe ADO, ADO MD et ADOX.

## <a name="new-features"></a>Fonctionnalités nouvelles

- **[Enregistrements et flux](chapter-10-records-and-streams.md)**

  Cette version d'ADO présente l'objet [Record](record-object-ado.md) , qui peut représenter et gérer des éléments tels que les répertoires et les fichiers d'un système de fichiers, ainsi que les dossiers et les messages d'un système de messagerie. L'objet **Record** peut également représenter une ligne d'un [Recordset](recordset-object-ado.md), bien que les objets **Record** et **Recordset** aient des méthodes et des propriétés différentes.

  Le nouvel objet [Stream](stream-object-ado.md) fournit les moyens de lire, d'écrire et de gérer le flux binaire d'octets ou de texte qui compose un flux de message ou de fichier.

- **[Utilisation des URL](absolute-and-relative-urls.md)**

  Cette version introduit également l'utilisation d'URL (Uniform Resource Locators) à la place des chaînes de connexion et du texte de commande pour nommer des objets de magasin de données. Ces URL peuvent être employées avec les objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec les nouveaux objets **Record** et **Stream**.

  La nouvelle version d’ADO prend également en charge des fournisseurs OLE DB qui identifient leurs propres schémas d’URL. Par exemple, le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md)*,* qui accède au système de fichiers Windows 2000, identifie le schéma HTTP existant.

- **[Champs spéciaux pour les fournisseurs de sources de documents](records-and-provider-supplied-fields.md)**

  Une classe spéciale de fournisseurs, appelée fournisseurs de *source de documents*, gère des dossiers et des documents. Lorsqu'un objet **Record** représente un document ou lorsqu'un objet **Recordset** représente un dossier de documents, le fournisseur de source de documents remplit ces objets d'un ensemble de champs unique qui décrit les caractéristiques du document. Ces champs constituent un objet **Record** ou **Recordset**de *ressources* .

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
<td><p><a href="charset-property-ado.md">Caractères</a></p></td>
<td><p>Indique dans quel jeu de caractères le contenu d'un objet <strong>Stream</strong> de texte doit être traduit.</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">ÉTHOXY</a></p></td>
<td><p>Indique si la position actuelle correspond à la fin du flux.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Indique quel caractère binaire utiliser comme séparateur de ligne dans des objets <strong>Stream</strong> de texte.</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Indique les autorisations disponibles pour modifier les données d'un objet <strong>Connection</strong>, <strong>Record</strong> ou <strong>Stream</strong>.</p></td>
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
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></p></td>
<td><p>Indique la taille du flux en nombre d'octets.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p>Indique l'entité représentée par l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>Indique, pour tous les objets applicables, si l'état de l'objet est ouvert ou fermé. Indique, pour tous les objets applicables exécutant une méthode asynchrone, si l'état actuel de l'objet est « en cours de connexion », « en cours d'exécution » ou « en cours d'extraction ».</p></td>
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
<td><p>Copie un fichier ou un répertoire, ainsi que son contenu à un autre emplacement.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Copie le nombre spécifié de caractères ou d'octets (selon le <strong>type</strong>) dans l' <strong></strong> <strong>objet</strong> Stream vers un autre objet <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Supprime un fichier ou un répertoire avec tous ses sous-répertoires.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Comptabilité</a></p></td>
<td><p>Force le contenu de l'objet <strong>Stream</strong> encore présent dans la mémoire tampon ADO dans l'objet sous-jacent auquel cet objet <strong>Stream</strong> est associé.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Retourne un objet <strong>Recordset</strong> dont les lignes représentent les fichiers et sous-répertoires du répertoire représenté par cet objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
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
<td><p>Ouvre un objet <strong>Stream</strong> afin de manipuler des flux de données binaires ou de texte.</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Lit le nombre spécifié d'octets d'un objet <strong>Stream</strong> binaire.</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Lit le nombre spécifié de caractères d'un objet <strong>Stream</strong> de texte.</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Enregistre le contenu binaire d'un objet <strong>Stream</strong> dans un fichier.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Définit la position qui correspond à la fin du flux.</p></td>
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


## <a name="new-and-enhanced-documentation"></a>Documentation nouvelle et améliorée

- **[Rubriques d'exemples de code](ado-code-examples.md)**

  Les exemples ont été développés pour contenir des exemples de code écrits en Microsoft Visual C++ et Microsoft Visual J++. Vous pouvez copier et coller ces exemples dans votre éditeur.

- **[Rubriques relatives aux fournisseurs](appendix-a-providers.md)**

  Une nouvelle rubrique, qui explique comment utiliser ADO avec le [fournisseur OLE DB pour la publication Internet](microsoft-ole-db-provider-for-internet-publishing.md), a été ajoutée.

- **[Programmation avec ADO](appendix-c-programming-with-ado.md)**

  Cette nouvelle section contient des conseils et des astuces pour l'utilisation d'ADO avec différents langages de programmation. Il contient les index de syntaxe existants pour les extensions Visual C++ pour ADO et ADO/WFC, ainsi que de nouvelles informations propres aux développeurs qui utilisent Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++ ou Microsoft Visual J++.

