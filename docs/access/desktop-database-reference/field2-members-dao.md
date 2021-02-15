---
title: Field2 members (DAO)
TOCTitle: Field2 Members
ms:assetid: 27829bbc-8b4e-c7eb-f29b-bcbef341f9fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191913(v=office.15)
ms:contentKeyID: 48543839
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf3deac487f1e114bea2a69d5423a210a51a5944
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292796"
---
# <a name="field2-members-dao"></a>Field2 members (DAO)


**S’applique à** : Access 2013, Office 2013

Un objet Field2 représente une colonne de données avec un type de données communes et un ensemble commun de propriétés.

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
<td><p><strong><a href="field2-appendchunk-method-dao.md">AppendChunk</a></strong></p></td>
<td><p>Ajoute des données issues d'une expression de chaîne à un objet <strong>Field2</strong> de type mémo ou binaire long dans un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Crée un objet utilisateur <strong><a href="property-object-dao.md">Property</a></strong> (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-getchunk-method-dao.md">GetChunk</a></strong></p></td>
<td><p>Renvoie l’ensemble ou une partie du contenu d’un objet <strong>Memo</strong> ou <strong>Long BinaryField2</strong> dans la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d’un <strong><a href="recordset-object-dao.md">objet Recordset.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-loadfromfile-method-dao.md">LoadFromFile</a></strong></p></td>
<td><p>Charge le fichier de disque désigné.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-savetofile-method-dao.md">SaveToFile</a></strong></p></td>
<td><p>Enregistre la pièce jointe sur le disque.</p></td>
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
<td><p><strong><a href="field2-allowzerolength-property-dao.md">AllowZeroLength</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si une chaîne de longueur nulle () est un paramètre valide pour la propriété Value de l’objet Field2 avec un type de données Texte ou Mémo (espaces de travail &quot; &quot; Microsoft Access uniquement). <strong><a href="field-value-property-dao.md"></a></strong> <strong></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-appendonly-property-dao.md">AppendOnly</a></strong></p></td>
<td><p>Obtient ou définit une valeur <strong>Boolean</strong> qui indique si le champ est paramétré pour placer lse valeurs à la fin du contenu existant du champ au fur et à mesure qu'elles sont ajoutées. En lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-attributes-property-dao.md">Attributs</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique une ou plusieurs caractéristiques d'un objet <strong>Field2</strong>. Type de données <strong>Long</strong> en lecture/écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Renvoie une valeur qui spécifie la séquence de l'ordre de tri du texte pour la comparaison ou le tri de chaînes de caractères (espaces de travail Microsoft Access uniquement). Valeur <strong>Long</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-complextype-property-dao.md">ComplexType</a></strong></p></td>
<td><p>Renvoie un objet <strong><a href="complextype-object-dao.md">ComplexType</a></strong> qui représente un champ à plusieurs valeurs. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-dataupdatable-property-dao.md">DataUpdatable</a></strong></p></td>
<td><p>Renvoie une donnée indiquant si la donnée du champ représenté par un objet <strong>Field2</strong> peut être mise à jour.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-defaultvalue-property-dao.md">DefaultValue</a></strong></p></td>
<td><p>Définit ou renvoie la valeur par défaut d'un objet <strong>Field2</strong>. Pour un objet <strong>Field2</strong> pas encore ajouté à la collection <strong><a href="fields-collection-dao.md">Fields</a></strong>, cette propriété est en lecture-écriture (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-expression-property-dao.md">Expression</a></strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-fieldsize-property-dao.md">FieldSize</a></strong></p></td>
<td><p>Renvoie le nombre d'octets utilisés dans la base de données (plutôt que la mémoire) d'un objet <strong>Field2</strong> de type Mémo ou Binaire long de la collection <strong><a href="fields-collection-dao.md">Fields</a></strong> d'un objet <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-foreignname-property-dao.md">ForeignName</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie le nom de l'objet <strong>Field2</strong> d'une table étrangère correspondant à un champ d'une table primaire d'une relation (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-iscomplex-property-dao.md">IsComplex</a></strong></p></td>
<td><p>Renvoie une valeur <strong>Boolean</strong> qui indique si le champ défini est un type de données à plusieurs valeurs. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-name-property-dao.md">Name</a></strong></p></td>
<td><p>Renvoie ou définit le nom de l'objet spécifié. Type <strong>String</strong> en lecture-écriture si l'objet n'a pas été ajouté à une collection. Type <strong>String</strong> en lecture seule si l'objet a été ajouté à une collection.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-ordinalposition-property-dao.md">OrdinalPosition</a></strong></p></td>
<td><p>Définit ou renvoie la position relative d’un <strong>objet Field2</strong> dans une collection <strong><a href="fields-collection-dao.md">Fields.</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-originalvalue-property-dao.md">OriginalValue</a></strong></p></td>
<td><p>Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Renvoie la valeur d'un objet <strong>Field2</strong> de la base de données qui existait au moment du lancement de la dernière mise à jour en lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-properties-property-dao.md">Propriétés</a></strong></p></td>
<td><p>Renvoie la collection <strong><a href="properties-collection-dao.md">Properties</a></strong> de l'objet spécifié. En lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-required-property-dao.md">Obligatoire</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique si un objet <strong>Field2</strong> requiert une valeur non nulle.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-size-property-dao.md">Taille</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique la taille maximale, en octets, d'un objet <strong>Field2</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-sourcefield-property-dao.md">SourceField</a></strong></p></td>
<td><p>Renvoie une valeur indiquant le nom du champ duquel provient les données d'un objet <strong>Field2</strong>. Données de type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-sourcetable-property-dao.md">SourceTable</a></strong></p></td>
<td><p>Renvoie une valeur indiquant le nom de la table de laquelle provient les données d'un objet <strong>Field2</strong>. Données de type <strong>String</strong> en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-type-property-dao.md">Type</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. <strong>Entier</strong> en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validateonset-property-dao.md">ValidateOnSet</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie si la valeur d'un objet <strong>Field2</strong> est immédiatement validée ou non lorsque la propriété <strong>Value</strong> de l'objet est définie (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui valide les données d'un champ lorsque ce dernier est modifié ou ajouté à une table (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet <strong>Field2</strong> ne respecte par la règle de validation spécifiée par le paramètre de propriété <strong>ValidationRule</strong> (espaces de travail Microsoft Access uniquement). Valeur <strong>String</strong> en lecture-écriture.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="field2-value-property-dao.md">Valeur</a></strong></p></td>
<td><p>Définit ou renvoie la valeur d'un objet. Type de données <strong>Variant</strong> en lecture/écriture.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="field2-visiblevalue-property-dao.md">VisibleValue</a></strong></p></td>
<td><p>Une des <strong><a href="workspacetypeenum-enumeration-dao.md">valeurs WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p>
<p>Renvoie une valeur actuellement dans la base de données qui est plus récente que la propriété <strong>OriginalValue</strong> suite à un conflit de mise à jour en lot (espaces de travail ODBCDirect uniquement).</p></td>
</tr>
</tbody>
</table>

