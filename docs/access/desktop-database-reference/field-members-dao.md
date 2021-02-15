---
title: Field members (DAO)
TOCTitle: Field Members
ms:assetid: 4b6a587f-1fd0-37fb-db7d-75b587a8dc60
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193511(v=office.15)
ms:contentKeyID: 48544689
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1a0e448662384572163fca074e554a5e30be30a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293090"
---
# <a name="field-members-dao"></a>Field members (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet Field représente une colonne de données avec un type de données communes et un ensemble commun de propriétés.

## <a name="methods"></a>Méthodes

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Ajoute des données issues d'une expression de chaîne à un objet <strong><a href="field-object-dao.md">Field</a></strong> de type mémo ou binaire long dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Renvoie l’ensemble ou une partie du contenu d’un objet <strong>Memo</strong> ou <strong>Long Binary</strong> <strong><a href="field-object-dao.md">Field</a></strong> dans la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d’un <strong><a href="recordset-object-dao.md">objet Recordset.</a></strong></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriétés

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="field-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si une chaîne de longueur nulle () est un paramètre valide pour la propriété Value de l’objet Field avec un type de données Texte ou Mémo (espaces de travail &quot; &quot; Microsoft Access uniquement). <strong><a href="field-value-property-dao.md"></a></strong> <strong><a href="field-object-dao.md"></a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-attributes-property-dao.md">Attributs</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet <strong><a href="field-object-dao.md">Field</a></strong>. <strong>Long</strong> (en lecture/écriture).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Renvoie une valeur qui indique si les données du champ représenté par un objet <strong><a href="field-object-dao.md">Field</a></strong> peuvent être modifiées.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Définit ou renvoie la valeur par défaut d'un objet <strong><a href="field-object-dao.md">Field</a></strong>. Cette propriété est en lecture-écriture si l'objet <strong>Field</strong> n'est pas encore ajouté à la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie le nom de l'objet <strong><a href="field-object-dao.md">Field</a></strong> d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Définit ou renvoie la position relative d’un <strong><a href="field-object-dao.md">objet Field</a></strong> dans une collection <strong><a href="fields-collection-dao.md">Fields.</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Renvoie la valeur d'un objet <strong>Field</strong> de la base de données qui existait au moment du lancement de la dernière mise à jour en lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-required-property-dao.md">Obligatoire</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong><a href="field-object-dao.md">Field</a></strong> requiert une valeur non Null.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-fieldsize-property-dao.md">Taille</a></strong></p></td>
<td><p>Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong><a href="field-object-dao.md">Field</a></strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Renvoie une valeur spécifiant le nom du champ qui représente la source d'origine des données d'un objet <strong>Field</strong>. Type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet <strong>Field</strong>. Données de type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. <strong>Entier</strong> en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie si la valeur d'un objet <strong><a href="field-object-dao.md">Field</a></strong> est immédiatement validée quand la propriété <strong><a href="field-value-property-dao.md">Value</a></strong> de l'objet est définie (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui valide les données d'un champ lorsque ce dernier est modifié ou ajouté à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet <strong>Field</strong> n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field-value-property-dao.md">Valeur</a></strong></p></td>
<td><p>Définit ou renvoie la valeur d'un objet. Type de données <strong>Variant</strong> en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Renvoie une valeur actuellement dans la base de données qui est plus récente que la propriété <strong>OriginalValue</strong> suite à un conflit de mise à jour en lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
</tbody>
</table>

