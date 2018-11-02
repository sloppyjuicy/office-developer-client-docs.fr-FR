---
title: Méthode QueryDef.OpenRecordset (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f18982c733d6fcbf150e31dfccab630529135722
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924350"
---
# <a name="querydefopenrecordset-method-dao"></a>Méthode QueryDef.OpenRecordset (DAO)


**S’applique à**: Access 2013, Office 2013

Crée un objet **[Recordset](recordset-object-dao.md)** et l'ajoute à la collection **Recordsets**.

## <a name="syntax"></a>Syntaxe

*expression* . OpenRecordset (***Type***, ***Options***, ***VerrouillerModification***)

*expression* Variable qui représente un objet **QueryDef** .

### <a name="parameters"></a>Paramètres

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Name</p></th>
<th><p>Obligatoire/Facultatif</p></th>
<th><p>Type de données</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Type</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variante</strong></p></td>
<td><p>Constante <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> qui indique le type de <strong>Recordset</strong> à ouvrir.</p>

> [!NOTE]
> <P>Si vous ouvrez un <STRONG>Recordset</STRONG> dans un espace de travail Microsoft Access et que vous n’indiquez aucun type, <STRONG>OpenRecordset</STRONG> crée un <STRONG>Recordset</STRONG> de type table, si possible. Si vous spécifiez une table liée ou une requête, <STRONG>OpenRecordset</STRONG> crée un <STRONG>Recordset</STRONG> de type feuille de réponse dynamique.</P>


</td>
</tr>
<tr class="even">
<td><p>Options</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Combinaison de constantes <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> qui indiquent les caractéristiques du nouveau <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>Les constantes <STRONG>dbConsistent</STRONG> et <STRONG>dbInconsistent</STRONG> s’excluent mutuellement, et l’utilisation de ces deux constantes peut entraîner une erreur. L’indication d’un argument lockedits lorsque options utilise la constante <STRONG>dbReadOnly</STRONG> génère également une erreur.</P>


</td>
</tr>
<tr class="odd">
<td><p>VerrouillerModification</p></td>
<td><p>Facultatif</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Constante <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> qui détermine le verrouillage du <strong>Recordset</strong>.</p>

> [!NOTE]
> <P>Vous pouvez utiliser <STRONG>dbReadOnly</STRONG> dans l’argument options ou l’argument lockededits, mais pas dans les deux. Si vous l’utilisez pour les deux arguments, une erreur d’exécution se produit.</P>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Recordset

## <a name="remarks"></a>Remarques

Vous devez également utiliser la constante **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** si vous ouvrez un objet **Recordset** dans un espace de travail ODBC connecté à un moteur de base de données Microsoft Access dans une table Microsoft SQL Server 6.0 (ou version ultérieure) possédant une colonne IDENTITY, autrement une erreur peut être générée.

L'ouverture de plusieurs objets **Recordset** dans une source de données ODBC peut entraîner un échec car la connexion est occupée par un appel d'objet **OpenRecordset** préalable. Pour contourner ce problème, vous pouvez renseigner totalement l'objet **Recordset** à l'aide de la méthode **[MoveLast](recordset-movelast-method-dao.md)** dès que l'objet **Recordset** est ouvert.

Si vous fermez un objet **Recordset** avec la méthode **Close**, l'objet est automatiquement supprimé de la collection **Recordsets**.


> [!NOTE]
> <P>Si <EM>la source</EM> fait référence à une instruction SQL composée d’une chaîne concaténée avec une valeur non entière, et les paramètres système spécifient un caractère décimal américain comme une virgule (par exemple, strSQL = « prix &gt; » &amp; lngPrice et lngPrice = 125,50), une erreur se produit lorsque vous essayez d’ouvrir le <STRONG>jeu d’enregistrements</STRONG>. Cela est dû au fait que pendant la concaténation, le nombre est converti en chaîne en utilisant le caractère décimal par défaut de votre système, et SQL n'accepte que les caractères décimaux usités aux États-Unis.</P>


