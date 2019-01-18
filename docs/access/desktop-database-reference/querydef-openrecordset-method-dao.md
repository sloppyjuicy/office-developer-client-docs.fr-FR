---
title: Méthode QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: a046359f39611e38b9e517495f54041f876addfc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710243"
---
# <a name="querydefopenrecordset-method-dao"></a>Méthode QueryDef.OpenRecordset (DAO)

**S’applique à**: Access 2013, Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*expression* . OpenRecordset (***Type***, ***Options***, ***VerrouillerModification***)

*expression* Variable qui représente un objet **QueryDef** .

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
<th><p>Requis/facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Type</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p><p><strong>Remarque</strong>: Si vous ouvrez un <STRONG>objet Recordset</STRONG> dans un espace de travail Microsoft Access et que vous ne spécifiez pas un type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>objet Recordset</STRONG>de type table, si possible. Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>jeu d’enregistrements</STRONG>de type feuille de réponse dynamique.</p>
</td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p></p><p><strong>Remarque</strong>: l’une des constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et les deux entraîne une erreur. Fournir un argument lockedits lorsque options utilise la constante <STRONG>peut entraîner</STRONG> génère également une erreur.</p>
</td>
</tr>
<tr class="odd">
<td><p><em>VerrouillerModification</em></p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p></p><p><strong>Remarque</strong>: vous pouvez utiliser <STRONG>peut entraîner</STRONG> dans l’argument options ou l’argument lockedits, mais pas les deux. Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Valeur renvoyée

Recordset

## <a name="remarks"></a>Remarques

Vous devez également utiliser la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.

L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **[MoveLast](recordset-movelast-method-dao.md)** dès que l'objet **Recordset** est ouvert.

Si vous fermez un objet **Recordset** avec la méthode **Close**, l'objet est automatiquement supprimé de la collection **Recordsets**.

> [!NOTE]
> Si *la source* fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le **jeu d’enregistrements**. Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.


