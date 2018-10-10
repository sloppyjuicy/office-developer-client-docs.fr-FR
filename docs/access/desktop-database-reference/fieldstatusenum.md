---
title: FieldStatusEnum (référence de base de données du bureau Access)
TOCTitle: FieldStatusEnum
ms:assetid: 49570042-8435-8618-3ba1-7006c47735e0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249225(v=office.15)
ms:contentKeyID: 48544635
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e5c7ecb345c993b2582ce6971044d325afca857a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472314"
---
# <a name="fieldstatusenum"></a>FieldStatusEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie l'état d'un objet **Field**.

Les valeurs **adFieldPending\*** indiquent l'opération à l'origine de l'état ; elles peuvent être combinées avec d'autres valeurs d'état.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adFieldAlreadyExists</strong></p></td>
<td><p>26</p></td>
<td><p>Indique que le champ spécifié existe déjà.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldBadStatus</strong></p></td>
<td><p>12</p></td>
<td><p>Indique qu’une valeur d’état non valide a été envoyée depuis ADO vers le fournisseur OLE DB. Causes possibles : un fournisseur OLE DB 1.0 ou 1.1, ou une combinaison incorrecte de <a href="value-property-ado.md">Value</a> et <a href="status-property-ado-field.md">Status</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCannotComplete</strong></p></td>
<td><p>20</p></td>
<td><p>Indique que le serveur de l’URL spécifiée par <a href="source-property-ado-record.md">Source</a> n’a pas pu terminer l’opération.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldCannotDeleteSource</strong></p></td>
<td><p>23</p></td>
<td><p>Indique que, pendant une opération de déplacement, un arbre ou sous-arbre a été déplacé vers un nouvel emplacement, mais que la source n'a pu être supprimée.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldCantConvertValue</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que le champ ne peut pas être extrait ni stocké sans perte de données.</p></td>
</tr>
<tr class="even">
<td><p><strong>Stocké</strong></p></td>
<td><p>7</p></td>
<td><p>Indique que le champ n'a pu être ajouté car le fournisseur a dépassé une limite (par exemple, le nombre de champs permis).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDataOverflow</strong></p></td>
<td><p>6</p></td>
<td><p>Indique que les données renvoyées par le fournisseur ont dépassé le type de données du champ.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldDefault</strong></p></td>
<td><p>13</p></td>
<td><p>Indique que la valeur par défaut du champ a été utilisée lors de la définition des données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldDoesNotExist</strong></p></td>
<td><p>16</p></td>
<td><p>Indique que le champ spécifié n'existe pas.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldIgnore</strong></p></td>
<td><p>15</p></td>
<td><p>Indique que ce champ a été ignoré lors de la définition des valeurs de données dans la source. Le fournisseur n'a pas défini de valeur.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIntegrityViolation</strong></p></td>
<td><p>10</p></td>
<td><p>Indique que le champ ne peut pas être modifié car il s'agit d'une entité calculée ou dérivée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldInvalidURL</strong></p></td>
<td><p>17</p></td>
<td><p>Indique l'URL de la source des données contient des caractères non valides.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldIsNull</strong></p></td>
<td><p>3</p></td>
<td><p>Indique que le fournisseur a renvoyé une valeur VARIANT de type VT_NULL et que ce champ n'est pas vide.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldOK</strong></p></td>
<td><p>0</p></td>
<td><p>Par défaut. Indique que le champ a été ajouté ou supprimé avec succès.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldOutOfSpace</strong></p></td>
<td><p>22</p></td>
<td><p>Indique que le fournisseur ne parvient pas à obtenir suffisamment d'espace de stockage pour réaliser un déplacement ou une copie.</p></td>
</tr>
<tr class="even">
<td><p><strong>égales à adFieldPendingChange</strong></p></td>
<td><p>0 x 40000</p></td>
<td><p>Indique soit que le champ a ét supprimé puis à nouveau ajouté, peut-être avec un type de données différent, soit que la valeur du champ a changé (dernier état connu : adFieldOK). La forme finale du champ modifiera la collection <a href="fields-collection-ado.md">Fields</a> après appel de la méthode <a href="update-method-ado.md">Update</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingDelete</strong></p></td>
<td><p>0 x 20000</p></td>
<td><p>Indique l'opération <strong>Delete</strong> a entraîné la définition de l'état. Le champ a été marqué pour suppression de la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingInsert</strong></p></td>
<td><p>0 x 10000</p></td>
<td><p>Indique que l'opération <strong>Append</strong> a entraîné la définition de l'état. <strong>Field</strong> a été marqué pour ajout à la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPendingUnknown</strong></p></td>
<td><p>0 x 80000</p></td>
<td><p>Indique que le fournisseur ne peut déterminer l'opération qui a défini l'état du champ.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldPendingUnknownDelete</strong></p></td>
<td><p>0 x 100000</p></td>
<td><p>Indique que le fournisseur ne peut déterminer l'opération qui a défini l'état du champ, et que ce dernier sera supprimé de la collection <strong>Fields</strong> après appel de la méthode <strong>Update</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldPermissionDenied</strong></p></td>
<td><p>9</p></td>
<td><p>Indique que le champ ne peut être modifié car il est défini en lecture seule.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldReadOnly</strong></p></td>
<td><p>24</p></td>
<td><p>Indique que le champ de la source de données est défini en lecture seule.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceExists</strong></p></td>
<td><p>19</p></td>
<td><p>Indique que le fournisseur n'a pu effectuer l'opération car un objet est déjà présent à l'URL de destination et le fournisseur ne peut l'effacer.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldResourceLocked</strong></p></td>
<td><p>18</p></td>
<td><p>Indique que le fournisseur n'a pas pu effectuer l'opération car la source de données est verrouillée par une application ou un processus (ou plusieurs).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldResourceOutOfScope</strong></p></td>
<td><p>25</p></td>
<td><p>Indique que l'URL source ou de destination est en dehors de l'étendue de l'enregistrement en cours.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldSchemaViolation</strong></p></td>
<td><p>11</p></td>
<td><p>Indique que la valeur a transgressé la contrainte de schéma de la source de données pour le champ.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldSignMismatch</strong></p></td>
<td><p>5</p></td>
<td><p>Indique que la valeur de donnée renvoyée par le fournisseur a été signée, contrairement au type de données de la valeur du champ ADO.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldTruncated</strong></p></td>
<td><p>4</p></td>
<td><p>Indique que des données de longueur variable ont été tronquées lors de la lecture de la source de données.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFieldUnavailable</strong></p></td>
<td><p>8</p></td>
<td><p>Indique que le fournisseur n'a pu déterminer la valeur lors de la lecture de la source de données. Par exemple, la ligne venait d'être créée, la valeur par défaut de la colonne n'était pas disponible, et une nouvelle valeur n'avait pas encore été spécifiée.</p></td>
</tr>
<tr class="even">
<td><p><strong>adFieldVolumeNotFound</strong></p></td>
<td><p>21</p></td>
<td><p>Indique que le fournisseur est incapable to localiser le volume de stockage indiqué par l'URL.</p></td>
</tr>
</tbody>
</table>


**Équivalent ADO/WFC**

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

