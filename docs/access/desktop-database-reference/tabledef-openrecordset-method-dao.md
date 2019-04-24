---
title: TableDef. OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2035d4319f7821f2a0469193955c732231f30cf0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314335"
---
# <a name="tabledefopenrecordset-method-dao"></a>TableDef. OpenRecordset, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*expression* . OpenRecordset (***type***, ***options***)

*expression* Variable qui représente un objet **TableDef** .

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nom</p></th>
<th><p>Obligatoire/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Obligatoire</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.  </p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p><p><strong>Remarque</strong>: Si vous ouvrez un <STRONG>objet Recordset</STRONG> dans un espace de travail Microsoft Access et que vous ne spécifiez pas de type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>objet Recordset</STRONG>de type table, si possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p><p><strong>Remarque</strong>: les constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s'excluent mutuellement et l'utilisation des deux déclenche une erreur. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p><p><strong>Remarque</strong>: vous pouvez utiliser <STRONG>DBReadOnly</STRONG> dans l'argument options ou LockEdits, mais pas dans les deux. If you use it for both arguments, a run-time error occurs.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Recordset

## <a name="remarks"></a>Remarques

En général, si l'utilisateur obtient cette erreur lors de la mise à jour d'un enregistrement, le code peut actualiser le contenu des champs et extraire les valeurs qui viennent d'être modifiées. Si l'erreur se produit lors de la suppression d'un enregistrement, le code peut afficher les nouvelles données de l'enregistrement pour l'utilisateur et un message indique que les données ont été modifiées dernièrement. À ce niveau, le code peut demander une confirmation que l'utilisateur souhaite encore supprimer l'enregistrement.

Vous devez également utiliser la constante **dbSeeChanges** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.

L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **MoveLast** dès que l'objet **Recordset** est ouvert.

Si vous fermez un objet **Recordset** avec la méthode **[Close](connection-close-method-dao.md)**, l'objet est automatiquement supprimé de la collection **Recordsets**.

> [!NOTE]
> Si *source* fait référence à une instruction SQL composée d'une chaîne concaténée avec une valeur non entière, et que les paramètres système spécifient un caractère non-U. S. Decimal tel qu'une virgule (par exemple, strSQL = &gt; " &amp; Price" lngPrice et lngPrice = 125, 50), une erreur se produit lorsque vous essayez d'ouvrir l' **objet Recordset**. Cela s'explique par le fait que lors de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut du système et le langage SQL n'accepte que les caractères décimaux de la notation américaine.


