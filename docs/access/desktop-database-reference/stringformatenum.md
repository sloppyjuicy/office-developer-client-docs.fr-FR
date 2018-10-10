---
title: StringFormatEnum (référence de base de données du bureau Access)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7814b15c75cfd1dbd48c793ee8c30cc2c5348ec9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470198"
---
# <a name="stringformatenum"></a>StringFormatEnum


**S’applique à**: Access 2013 | Office 2013

Spécifie le format lors de l'extraction d'un [Recordset](recordset-object-ado.md) sous forme de chaîne.

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
<td><p><strong>adClipString</strong></p></td>
<td><p>2</p></td>
<td><p>Délimite les lignes par <em>RowDelimiter</em>, les colonnes par <em>ColumnDelimiter</em> et les valeurs nulles par <em>NullExpr</em>. Ces trois paramètres de la méthode <a href="getstring-method-ado.md">GetString</a> ne sont valides qu’avec un <em>StringFormat</em> de <strong>adClipString</strong>.</p></td>
</tr>
</tbody>
</table>


**Équivalent ADO/WFC**

Module : **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.StringFormat.CLIPSTRING</p></td>
</tr>
</tbody>
</table>

