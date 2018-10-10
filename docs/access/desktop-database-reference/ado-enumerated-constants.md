---
title: Constantes énumérées ADO
TOCTitle: ADO Enumerated Constants
ms:assetid: 7c983acd-8b38-dc3c-6704-46e649ebb7d6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249522(v=office.15)
ms:contentKeyID: 48545841
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ecefa3973d2995a69feb9abe82355aae7df63d1
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471727"
---
# <a name="ado-enumerated-constants"></a>Constantes énumérées ADO


**S’applique à**: Access 2013 | Office 2013

Pour faciliter le débogage, les énumérations ADO comportent une valeur pour chaque constante. Cependant, cette valeur est fournie uniquement à titre indicatif et peut changer d'une version d'ADO à une autre. Votre code doit dépendre uniquement du nom et non de la valeur réelle de chaque constante énumérée.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="adcprop-asyncthreadpriority-enum.md">ADCPROP_ASYNCTHREADPRIORITY_ENUM</a></p></td>
<td><p>Pour un objet <strong>Recordset</strong> RDS, spécifie la priorité d'exécution du thème asynchrone qui recherche des données.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-autorecalc-enum.md">ADCPROP_AUTORECALC_ENUM</a></p></td>
<td><p>Indique quand le fournisseur <strong>MSDataShape</strong> recalcule les colonnes regroupées et calculées dans un <strong>jeu d’enregistrements</strong>hiérarchique.</p></td>
</tr>
<tr class="odd">
<td><p><a href="adcprop-updatecriteria-enum.md">ADCPROP_UPDATECRITERIA_ENUM</a></p></td>
<td><p>Indique les champs qui peuvent être utilisés pour détecter les conflits pendant une mise à jour optimiste d'une ligne de la source de données avec un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="adcprop-updateresync-enum.md">ADCPROP_UPDATERESYNC_ENUM</a></p></td>
<td><p>Indique si la méthode <strong>UpdateBatch</strong> est suivie d'une opération implicite de la méthode <strong>Resync</strong> et, dans ce cas, la portée de cette opération.</p></td>
</tr>
<tr class="odd">
<td><p><a href="affectenum.md">AffectEnum</a></p></td>
<td><p>Indique les enregistrements affectés par une opération.</p></td>
</tr>
<tr class="even">
<td><p><a href="bookmarkenum.md">BookmarkEnum</a></p></td>
<td><p>Spécifie un signet indiquant où doit commencer l'opération.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtypeenum.md">CommandTypeEnum</a></p></td>
<td><p>Spécifie comment interpréter un argument de commande.</p></td>
</tr>
<tr class="even">
<td><p><a href="compareenum.md">CompareEnum</a></p></td>
<td><p>Spécifie la position relative de deux enregistrements représentés par leurs signets.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectmodeenum.md">ConnectModeEnum</a></p></td>
<td><p>Spécifie les autorisations disponibles pour modifier les données dans une <strong>Connexion</strong>, en ouvrant un <strong>Enregistrement</strong>, ou en spécifiant des valeurs pour la propriété <strong>Mode</strong> de l' <strong>Enregistrement</strong> et des objets <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectoptionenum.md">ConnectOptionEnum</a></p></td>
<td><p>Indique si la méthode <strong>Open</strong> d'un objet <strong>Connection</strong> doit être exécutée après (de façon synchrone) ou avant (de façon asynchrone) l'établissement de la connexion.</p></td>
</tr>
<tr class="odd">
<td><p><a href="connectpromptenum.md">ConnectPromptEnum</a></p></td>
<td><p>Indique si une boîte de dialogue doit être affichée pour demander les paramètres manquants lors de l'ouverture d'une connexion à une source de données ODBC.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecordoptionsenum.md">CopyRecordOptionsEnum</a></p></td>
<td><p>Spécifie le fonctionnement de la méthode <strong>CopyRecord</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocationenum.md">CursorLocationEnum</a></p></td>
<td><p>Spécifie l'emplacement du moteur de curseur.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursoroptionenum.md">CursorOptionEnum</a></p></td>
<td><p>Spécifie la fonctionnalité que la méthode <strong>Supports</strong> doit tester.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortypeenum.md">CursorTypeEnum</a></p></td>
<td><p>Spécifie le type de curseur utilisé dans un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="datatypeenum.md">DataTypeEnum</a></p></td>
<td><p>Spécifie le type de données d'un <strong>Champ</strong>, d'un <strong>Paramètre</strong> ou d'une <strong>Propriété</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmodeenum.md">EditModeEnum</a></p></td>
<td><p>Spécifie l'état d'édition d'un enregistrement.</p></td>
</tr>
<tr class="even">
<td><p><a href="errorvalueenum.md">ErrorValueEnum</a></p></td>
<td><p>Spécifie le type d'erreur d'exécution ADO.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eventreasonenum.md">EventReasonEnum</a></p></td>
<td><p>Spécifie la cause à l'origine d'un événement.</p></td>
</tr>
<tr class="even">
<td><p><a href="eventstatusenum.md">EventStatusEnum</a></p></td>
<td><p>Spécifie l'état en cours de l'exécution d'un événement.</p></td>
</tr>
<tr class="odd">
<td><p><a href="executeoptionenum.md">ExecuteOptionEnum</a></p></td>
<td><p>Spécifie la manière dont un fournisseur doit exécuter une commande.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldenum.md">FieldEnum</a></p></td>
<td><p>Spécifie les champs spéciaux référencés dans une collection <strong>Fields</strong> d'un objet <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="fieldattributeenum.md">FieldAttributeEnum</a></p></td>
<td><p>Spécifie un ou plusieurs attributs d'un objet <strong>Field</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="fieldstatusenum.md">FieldStatusEnum</a></p></td>
<td><p>Spécifie l'état d'un objet <strong>Field</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="filtergroupenum.md">FilterGroupEnum</a></p></td>
<td><p>Spécifie le groupe d'enregistrements à filtrer depuis un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getrowsoptionenum.md">GetRowsOptionEnum</a></p></td>
<td><p>Spécifie le nombre d'enregistrements à extraire depuis un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevelenum.md">IsolationLevelEnum</a></p></td>
<td><p>Spécifie le niveau d'isolement de transaction d'un objet <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="lineseparatorsenum.md">LineSeparatorsEnum</a></p></td>
<td><p>Spécifie le caractère utilisé comme séparateur de ligne dans les objets texte <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktypeenum.md">LockTypeEnum</a></p></td>
<td><p>Spécifie le type de verrouillage appliqué aux enregistrements pendant l'édition.</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptionsenum.md">MarshalOptions</a></p></td>
<td><p>Spécifie les enregistrements qui doivent être renvoyés au serveur.</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecordoptionsenum.md">MoveRecordOptionsEnum</a></p></td>
<td><p>Spécifie le fonctionnement de la méthode <strong>MoveRecord</strong> de l'objet <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="objectstateenum.md">ObjectStateEnum</a></p></td>
<td><p>Indique si un objet est ouvert ou fermé, s'il se connecte à une source de données, s'il exécute une commande ou s'il extrait des données.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameterattributesenum.md">ParameterAttributesEnum</a></p></td>
<td><p>Spécifie les attributs d'un objet <strong>Parameter</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="parameterdirectionenum.md">ParameterDirectionEnum</a></p></td>
<td><p>Spécifie si l'objet <strong>Parameter</strong> représente un paramètre d'entrée, un paramètre de sortie ou les deux, ou encore si le paramètre correspond à la valeur renvoyée par une procédure stockée.</p></td>
</tr>
<tr class="odd">
<td><p><a href="persistformatenum.md">PersistFormatEnum</a></p></td>
<td><p>Spécifie le format dans lequel enregistrer un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="positionenum.md">PositionEnum</a></p></td>
<td><p>Spécifie la position en cours du pointeur de l'enregistrement dans un objet <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="propertyattributesenum.md">PropertyAttributesEnum</a></p></td>
<td><p>Spécifie les attributs d'un objet <strong>Property</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcreateoptionsenum.md">RecordCreateOptionsEnum</a></p></td>
<td><p>Indique si un objet <strong>Record</strong> existant doit être ouvert ou si un nouvel objet <strong>Record</strong> doit être créé pour la méthode <strong>Open</strong> de l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordopenoptionsenum.md">RecordOpenOptionsEnum</a></p></td>
<td><p>Spécifie les options nécessaires pour ouvrir un objet <strong>Record</strong>. Ces valeurs peuvent être combinées avec un opérateur OR.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordstatusenum.md">RecordStatusEnum</a></p></td>
<td><p>Spécifie l'état d'un enregistrement en cas de mise à jour par lots et autres opérations globales de ce type.</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtypeenum.md">RecordTypeEnum</a></p></td>
<td><p>Spécifie le type de l'objet <strong>Record</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="resyncenum.md">ResyncEnum</a></p></td>
<td><p>Spécifie si les valeurs sous-jacentes sont remplacées par un appel à <strong>Resync</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="saveoptionsenum.md">SaveOptionsEnum</a></p></td>
<td><p>Spécifie si un fichier doit être créé ou remplacé en cas de sauvegarde d'un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND.</p></td>
</tr>
<tr class="even">
<td><p><a href="schemaenum.md">SchemaEnum</a></p></td>
<td><p>Spécifie le type d'objet <strong>Recordset</strong> de schéma extrait par la méthode <strong>OpenSchema</strong>. Spécifie le sens de la recherche d'un enregistrement dans un <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="searchdirectionenum.md">SearchDirectionEnum</a></p></td>
<td><p>Spécifie la direction d'une recherche d'enregistrement dans un objet <strong>Recordset</strong> et le type de méthode <strong>Seek</strong> à exécuter.</p></td>
</tr>
<tr class="even">
<td><p><a href="seekenum.md">SeekEnum</a></p></td>
<td><p>Spécifie le type de méthode <strong>Seek</strong> à exécuter et les options permettant d'ouvrir un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamopenoptionsenum.md">StreamOpenOptionsEnum</a></p></td>
<td><p>Spécifie les options permettant d'ouvrir un objet <strong>Stream</strong>. Les valeurs peuvent être combinées avec un opérateur AND. Indique également s'il faut lire l'ensemble du flux ou seulement la ligne suivante d'un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamreadenum.md">StreamReadEnum</a></p></td>
<td><p>Indique s'il faut lire l'ensemble du flux ou seulement la ligne suivante d'un objet <strong>Stream</strong>. Spécifie également le type des données stockées dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="streamtypeenum.md">StreamTypeEnum</a></p></td>
<td><p>Spécifie le type des données stockées dans un objet <strong>Stream</strong>. Indique également si un séparateur de ligne est ajouté à la chaîne écrite dans un objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="streamwriteenum.md">StreamWriteEnum</a></p></td>
<td><p>Indique si un séparateur de ligne est ajouté à la chaîne écrite dans un objet <strong>Stream</strong>. Spécifie également le format à utiliser pour extraire un objet <strong>Recordset</strong> sous forme de chaîne.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stringformatenum.md">StringFormatEnum</a></p></td>
<td><p>Spécifie le format à utiliser pour extraire un objet <strong>Recordset</strong> sous forme de chaîne. Indique également les attributs de transaction d'un objet <strong>Connection</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="xactattributeenum.md">XactAttributeEnum</a></p></td>
<td><p>Spécifie les attributs de transaction d'un objet <strong>Connection</strong>.</p></td>
</tr>
</tbody>
</table>

