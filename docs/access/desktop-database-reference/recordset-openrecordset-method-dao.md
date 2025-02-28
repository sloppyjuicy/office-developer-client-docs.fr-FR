---
title: Recordset.OpenRecordset, méthode (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 2d0dbb40ffda0a856ffb334a484461ceeb3c1562
ms.sourcegitcommit: a355e6b8898e9a1d66ca1bc808fe106e78dcb68f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2022
ms.locfileid: "63726350"
---
# <a name="recordsetopenrecordset-method-dao"></a>Recordset.OpenRecordset, méthode (DAO)

**S’applique à** : Access 2013, Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l’ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*expression* .OpenRecordset(**Type**, _Options_)

*expression* Variable qui représente un objet **Recordset**.

## <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col />
<col />
<col />
<col />
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
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p><p><strong>REMARQUE</strong> : si vous ouvrez un objet <STRONG>Recordset</STRONG> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <STRONG>OpenRecordset</STRONG> crée un objet <STRONG>Recordset</STRONG> de type table, si possible. Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>Recordset</STRONG> de type feuille de réponse dynamique.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p></p><p><strong>REMARQUE</strong>: les constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement et l’utilisation des deux provoque une erreur. La fourniture d’un argument lockedits lorsque les options utilisent la constante <STRONG>dbReadOnly</STRONG> provoque également une erreur.</p>
</td>
</tr>
<tr class="even">
<td><p><em>LockEdit</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p></p><p><strong>REMARQUE</strong> : vous pouvez utiliser <STRONG>dbReadOnly</STRONG> dans l’argument options ou dans l’argument lockededits, mais pas dans les deux. Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</p>
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
> Si *source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal non-américain tel qu’une virgule (par exemple, strSQL = " PRICE &gt; " &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **Recordset**. En effet, pendant la concaténation, le nombre est converti en chaîne à l’aide du caractère décimal par défaut de votre système, et SQL accepte uniquement les caractères décimaux américains.


