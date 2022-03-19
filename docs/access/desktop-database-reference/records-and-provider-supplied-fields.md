---
title: Enregistrements et champs fournis par le fournisseur
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 98251127149e3272cb669e75437d753fc442a112
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63628132"
---
# <a name="records-and-provider-supplied-fields"></a>Enregistrements et champs fournis par le fournisseur

**S’applique à** : Access 2013, Office 2013

Lorsqu'un objet [Record](record-object-ado.md) est ouvert, sa source peut être la ligne active d'un objet [Recordset](recordset-object-ado.md) ouvert, une URL absolue ou une URL relative à un objet [Connection](connection-object-ado.md) ouvert.

Si l'objet **Record** est ouvert depuis un objet **Recordset**, la collection **Fields** de l'objet [Record](fields-collection-ado.md) contiendra tous les champs provenant de l'objet **Recordset** ainsi que tous les champs ajoutés par le fournisseur sous-jacent.

Le fournisseur peut insérer d'autres champs utilisés comme caractéristiques supplémentaires de l'objet **Record**. Par conséquent, un objet **Record** peut comporter des champs uniques, non présents dans l'objet **Recordset** ou tout objet **Record** dérivé d'une autre ligne de l'objet **Recordset**.

Par exemple, toutes les lignes d’un **recordset** dérivé d’une source de données de messagerie peuvent avoir des colonnes telles que De, À et Objet. Un objet **Record** dérivé de cet objet **Recordset** comportera les mêmes champs. Cependant, l'objet **Record** peut également comporter d'autres champs uniques et spécifiques au message représenté par cet objet **Record**, Pièce jointe et CC, par exemple.

Bien que l'objet **Record** et la ligne active de l'objet **Recordset** comportent les mêmes champs, ceux-ci diffèrent, car les objets **Record** et **Recordset** possèdent des méthodes et des propriétés différentes.

Un champ commun aux objets **Record** et **Recordset** peut être modifié indifféremment dans l'un ou l'autre objet. Cependant, le champ ne peut pas être supprimé de l'objet **Record** même si le fournisseur sous-jacent accepte une valeur de champ null.

Une fois que l'objet **Record** est ouvert, vous pouvez ajouter des champs par programme. Vous pouvez également supprimer ceux que vous avez ajoutés, mais vous ne pouvez pas supprimer les champs de l'objet **Recordset** initial.

Vous pouvez également ouvrir l'objet **Record** directement à partir d'une URL. Dans ce cas, les champs ajoutés à l'objet **Record** dépendent du fournisseur sous-jacent. Actuellement, la plupart des fournisseurs ajoutent un ensemble de champs qui décrivent l'entité représentée par l'objet **Record**. Si l'entité est constituée d'un flux d'octets, par exemple un fichier simple, un objet [Stream](stream-object-ado.md) peut généralement être ouvert depuis l'objet **Record**.

## <a name="special-fields-for-document-source-providers"></a>Champs spéciaux destinés aux fournisseurs de source de documents

Une classe spéciale de fournisseurs, appelée *fournisseurs de sources de documents*, gère les dossiers et les documents. Lorsqu'un objet **Record** représente un document ou qu'un objet **Recordset** représente un dossier de documents, le fournisseur de la source des documents remplit ces objets avec un jeu unique de champs qui décrivent les caractéristiques du document plutôt que le document en lui-même. En général, un champ contient une référence à l'objet **Stream** qui représente le document.

Ces champs constituent un objet **Record** ou **Recordset** de ressources et sont répertoriés pour les fournisseurs spécifiques qui les prennent en charge à l' [Annexe A : Fournisseurs](appendix-a-providers.md).

Deux constantes indexent la collection **Fields** d'un objet **Record** ou **Recordset** de ressources pour extraire une paire de champs fréquemment utilisés. La propriété **Value** de l'objet [Field](value-property-ado.md) retourne le contenu demandé.

  - Le champ accédé avec la constante **adDefaultStream** contient un flux par défaut associé à l'objet **Record** ou **Recordset**. Le fournisseur affecte un flux par défaut à un objet.

  - Le champ accédé avec la constante **adRecordURL** contient l'URL absolue qui identifie le document.

Un fournisseur de sources de documents ne prend pas en charge la collection [Properties](properties-collection-ado.md) des objets **Record** et **Field**. Le contenu de la collection **Properties** a une valeur null pour de tels objets.

Un fournisseur de sources de documents peut ajouter une propriété spécifique au fournisseur, comme la propriété **Datasource Type** qui permet de l'identifier. Pour plus d'informations sur la façon de déterminer le type de fournisseur, consultez la documentation de celui-ci.

## <a name="resource-recordset-columns"></a>Colonnes d'un objet Recordset de ressources

Un *objet Recordset de ressources* comporte les colonnes suivantes.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom de colonne</p></th>
<th><p>Type</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RESOURCE_PARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>En lecture seule. Indique l'URL de la ressource.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_PARENTNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>En lecture seule. Indique l'URL absolue de l'enregistrement parent.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ABSOLUTEPARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>En lecture seule. Indique l'URL absolue de la ressource, qui est la concaténation de PARENTNAME et PARSENAME.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISHIDDEN</p></td>
<td><p>AdBoolean</p></td>
<td><p>True si la ressource est cachée. Aucune ligne n'est retournée sauf si la commande qui crée le jeu de lignes sélectionne de façon explicite les lignes dont la propriété RESOURCE_ISHIDDEN a la valeur True.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISREADONLY</p></td>
<td><p>AdBoolean</p></td>
<td><p>True si la ressource est en lecture seule. Tente d'ouvrir cette ressource avec DBBINDFLAG_WRITE et échoue avec DB_E_READONLY. Cette propriété peut être modifiée même si la ressource n'a été ouverte qu'en lecture.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTTYPE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indique l'utilisation probable du document, par exemple, un dossier d'avocat. Cela peut correspondre au modèle Office utilisé pour créer le document.&quot;&quot;</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CONTENTCLASS</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indique le type MIME du document, indiquant le format tel que texte &quot;/html&quot;.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTLANGUAGE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>Indique la langue dans laquelle le contenu est stocké.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CREATIONTIME</p></td>
<td><p>adFileTime</p></td>
<td><p>En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format de temps universel (UTC, Coordinated Universal Time).</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_LASTACCESSTIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format UTC. Les membres FILETIME sont au nombre de zéro si le fournisseur ne prend pas en charge ce membre de temps.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_LASTWRITETIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>En lecture seule. Indique une structure FILETIME contenant l'heure à laquelle la ressource a été créée. L'heure est au format UTC. Les membres FILETIME sont au nombre de zéro si le fournisseur ne prend pas en charge ce membre de temps.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_STREAMSIZE</p></td>
<td><p>asUnsignedBigInt</p></td>
<td><p>En lecture seule. Indique la taille (en octets) du flux par défaut de la ressource.</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISCOLLECTION</p></td>
<td><p>AdBoolean</p></td>
<td><p>En lecture seule. True si la ressource est une collection, telle qu'un répertoire. False si la ressource est un fichier simple.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISSTRUCTUREDDOCUMENT</p></td>
<td><p>AdBoolean</p></td>
<td><p>True si la ressource est un document structuré. False si la ressource n'est pas un document structuré. Il peut s'agir d'une collection ou d'un fichier simple.</p></td>
</tr>
<tr class="odd">
<td><p>DEFAULT_DOCUMENT</p></td>
<td><p>AdVarWChar</p></td>
<td><p>En lecture seule. Indique que cette ressource contient une URL pointant vers le document simple par défaut d'un dossier ou un document structuré. Utilisé si le flux par défaut est requis par une ressource. Pour les fichiers simples, cette propriété est vide.</p></td>
</tr>
<tr class="even">
<td><p>CHAPTERED_CHILDREN</p></td>
<td><p>AdChapter</p></td>
<td><p>En lecture seule. Facultative. Indique le chapitre du jeu de lignes contenant les enfants de la ressource. (Le <em>fournisseur Microsoft OLE DB pour la publication Internet</em> ne prend pas en charge cette colonne.)</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_DISPLAYNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>En lecture seule. Indique le nom complet de la ressource.</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISROOT</p></td>
<td><p>AdBoolean</p></td>
<td><p>En lecture seule. True si la ressource est la racine d'une collection ou d'un document structuré.</p></td>
</tr>
</tbody>
</table>

