---
title: MemberTypeEnum (référence de base de données de bureau Access)
TOCTitle: MemberTypeEnum
ms:assetid: 3b6f9fff-fe54-b917-9404-927e3a627e0b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249150(v=office.15)
ms:contentKeyID: 48544286
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c1c6809ddc44c1de61afa064dba7603379bd95a6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593970"
---
# <a name="membertypeenum"></a>MemberTypeEnum

**S’applique à** : Access 2013, Office 2013

Spécifie le paramétrage de la propriété [Type](type-property-ado-md.md) d’un objet [Member](member-object-ado-md.md).

<br/>

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
<td><p><strong>adMemberAll</strong></p></td>
<td><p>4 </p></td>
<td><p>Indique que l'objet <strong>Member</strong> représente tous les membres du niveau.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMemberFormula</strong></p></td>
<td><p>3</p></td>
<td><p>Indique que l'objet <strong>Member</strong> est calculé à l'aide d'une expression de formule.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMemberMeasure</strong></p></td>
<td><p>2</p></td>
<td><p>Indique que l'objet <strong>Member</strong> appartient à la dimension Measures et représente un attribut quantitatif.</p></td>
</tr>
<tr class="even">
<td><p><strong>adMemberRegular</strong></p></td>
<td><p>1</p></td>
<td><p>Valeur par défaut. Indique que l'objet <strong>Member</strong> représente une instance d'une entité métier.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adMemberUnknown</strong></p></td>
<td><p>0</p></td>
<td><p>Il est impossible de déterminer le type du membre.</p></td>
</tr>
</tbody>
</table>

