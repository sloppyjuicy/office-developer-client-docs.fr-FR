---
title: StreamWriteEnum (référence de base de données de bureau Access)
TOCTitle: StreamWriteEnum
ms:assetid: b4356999-d7a8-abfa-f6a8-6c2dd04b9257
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249861(v=office.15)
ms:contentKeyID: 48547216
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: b6a3d96bec786b461873a177cfad310004cece62
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630496"
---
# <a name="streamwriteenum"></a>StreamWriteEnum

**S’applique à** : Access 2013, Office 2013

Spécifie si un séparateur de ligne est ajouté à la chaîne écrite dans un objet [Stream](stream-object-ado.md).


<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adWriteChar</strong></p></td>
<td><p>0</p></td>
<td><p>Par défaut. Écrit la chaîne de texte spécifiée (paramètre <em>Data</em>) dans l'objet <strong>Stream</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adWriteLine</strong></p></td>
<td><p>1</p></td>
<td><p>Écrit une chaîne de texte et un caractère de séparateur de ligne dans un objet <strong>Stream</strong>. Si la propriété <a href="lineseparator-property-ado.md">LineSeparator</a> n’est pas définie, une erreur d’exécution est renvoyée.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

