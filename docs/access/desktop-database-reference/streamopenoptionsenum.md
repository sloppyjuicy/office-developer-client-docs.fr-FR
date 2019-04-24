---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314748"
---
# <a name="streamopenoptionsenum"></a>StreamOpenOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie les options pour l'ouverture d'un objet [Stream](stream-object-ado.md). Les valeurs peuvent être combinées avec une opération OR.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td><p><strong>adOpenStreamAsync</strong></p></td>
<td><p>0,1</p></td>
<td><p>Ouvre l’objet <strong>Stream</strong> en mode asynchrone.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStreamFromRecord</strong></p></td>
<td><p>4</p></td>
<td><p>Identifie le contenu du paramètre <em>Source</em> en tant qu’objet <a href="record-object-ado.md">Record</a> déjà ouvert. L’action par défaut est de traiter <em>Source</em> comme une URL pointant directement sur un nœud d’un arbre. La chaîne de données associée à ce nœud est ouverte.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenStreamUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Spécifie l'ouverture de l'objet <strong>Stream</strong> avec des options par défaut.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

