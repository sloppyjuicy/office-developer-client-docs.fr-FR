---
title: TableDef.OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: f4c9c89c-3348-d3c9-ce76-dd11e5ee11a7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836703(v=office.15)
ms:contentKeyID: 48548696
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a9b6e47d0480228d8f30be9cc06c2d51e896391d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605826"
---
# <a name="tabledefopenrecordset-method-dao"></a>TableDef.OpenRecordset, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l’ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*.* OpenRecordset(***Type** _, _*_Options_**)

*expression* Variable représentant un objet **TableDef**.

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
<td><p>Source des enregistrements du nouveau <strong>Recordset</strong>. La source peut être un nom de table, un nom de requête ou une instruction SQL qui renvoie des enregistrements. Pour les objets <strong>Recordset</strong> de type table dans les bases de données du moteur de base de données Microsoft Access, la source peut uniquement être un nom de table.</p></td>
</tr>
<tr class="even">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p><p><strong>REMARQUE</strong> : si vous ouvrez un objet <STRONG>Recordset</STRONG> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <STRONG>OpenRecordset</STRONG> crée un objet <STRONG>Recordset</STRONG> de type table, si possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p><p><strong>REMARQUE</strong> : <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p><p><strong>REMARQUE</strong> : vous pouvez utiliser <STRONG>dbReadOnly</STRONG> dans l’argument options ou dans l’argument lockededits, mais pas dans les deux. Si vous l’utilisez dans les deux arguments, une erreur d’exécution se produit.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Recordset

## <a name="remarks"></a>Remarques

En règle générale, si l’utilisateur obtient cette erreur lors de la mise à jour d’un enregistrement, votre code doit actualiser le contenu des champs et récupérer les valeurs nouvellement modifiées. Si une erreur survient lors de la suppression d’un enregistrement, votre code peut afficher les données du nouvel enregistrement à l’utilisateur, ainsi qu’un message indiquant que les données ont récemment été modifiées. À ce stade, votre code peut demander une confirmation pour s’assurer que l’utilisateur souhaite toujours supprimer l’enregistrement.

Vous pouvez également utiliser la constante **dbSeeChanges** si vous ouvrez un **Recordset** dans un espace de travail ODBC connecté au moteur de base de données Microsoft Access par rapport à une table Microsoft SQL Server 6.0 (ou version ultérieure) qui comporte une colonne IDENTITY, sinon une erreur peut survenir.

L’ouverture de plusieurs objets **Recordset** sur une source de données ODBC peut échouer car la connexion est occupée par un appel **OpenRecordset** précédent. Pour éviter cela, vous pouvez remplir complètement l’objet **Recordset** à l’aide de la méthode **MoveLast** dès l’ouverture du **Recordset**.

La fermeture d’un **Recordset** avec la méthode **[Close](connection-close-method-dao.md)** le supprime automatiquement de la collection **Recordsets**.

> [!NOTE]
> Si l’argument *source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et que les paramètres système spécifient un caractère décimal d’un format différent de celui des États-Unis, tel qu’une virgule (par exemple, strSQL = "PRICE &gt; " &amp; lngPrice, et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir l’objet **Recordset**. Cela s'explique par le fait que lors de la concaténation, le nombre est converti en chaîne à l'aide du caractère décimal par défaut du système et le langage SQL n'accepte que les caractères décimaux de la notation américaine.


