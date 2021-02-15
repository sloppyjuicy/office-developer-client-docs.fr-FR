---
title: QueryDef.Type, propriété (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300944"
---
# <a name="querydeftype-property-dao"></a>QueryDef.Type, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui indique le type opérationnel ou le type de données d'un objet. En lecture seule **integer**.

## <a name="syntax"></a>Syntaxe

*expression* .Type

*expression* Variable représentant un objet **QueryDef**.

## <a name="remarks"></a>Remarques

Les paramètres et valeurs de retour possible d'un objet **QueryDef** sont décrits dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Type de requête</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbQAction</strong></p></td>
<td><p>Action</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQAppend</strong></p></td>
<td><p>Ajout</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQCompound</strong></p></td>
<td><p>Composé</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Crosstab</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Définition des données</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Supprimer</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Création de table</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Procédure (espaces de travail ODBCDirect uniquement)</p><p><strong>NOTE</strong> : Les espaces de travail ODBCDirect ne sont pas pris en charge dans Microsoft Access 2013. Utilisez ADO si vous voulez accéder aux sources de données externes sans avoir recours au moteur de base de données Microsoft Access.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Sélectionner</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>Union</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSPTBulk</strong></p></td>
<td><p>Utilisé avec <strong>dbQSQLPassThrough</strong> pour spécifier une requête qui ne renvoie pas d’enregistrements (espaces de travail Microsoft Access uniquement).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSQLPassThrough</strong></p></td>
<td><p>Requête SQL directe (espaces de travail Microsoft Access uniquement)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Update</p></td>
</tr>
</tbody>
</table>


Lorsque vous ajoutez un nouvel objet **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** ou **[Property](property-object-dao.md)** à la collection d'un objet **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**, une erreur se produit si la base de données sous-jacente ne prend pas en charge le type de données spécifié du nouvel objet.

