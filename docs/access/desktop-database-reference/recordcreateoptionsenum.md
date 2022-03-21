---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: f4b35fd41f66871f555760d9797d9f37164a2a0f
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632671"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie si un **Record** doit être ouvert ou si un nouveau **Record** doit être créé pour la méthode [Open](record-object-ado.md) de l'objet [Record](open-method-ado-record.md) . Les valeurs peuvent être combinées avec un opérateur AND.

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Crée un nouveau <strong>Record</strong> sur le nœud spécifié par le paramètre <em>Source</em>, au lieu d'ouvrir un <strong>Record</strong> existant. Si la source pointe sur un nœud existant, une erreur d'exécution se produit, à moins que <strong>adCreateCollection</strong> ne soit combiné avec <strong>adOpenIfExists</strong> ou <strong>adCreateOverwrite</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Crée un nouveau <strong>Record</strong> de type <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Modifie les indicateurs de création <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> et <strong>adCreateStructDoc</strong>. Quand OR est utilisé avec cette valeur et l'une des valeurs d'indicateur de création, et si l'URL source pointe sur un nœud ou un <strong>Record</strong> existant, le <strong>Record</strong> est remplacé par un nouveau. Cette valeur ne peut être utilisée avec <strong>adOpenIfExists</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Crée un nouveau <strong>Record</strong> de type <a href="recordtypeenum.md">adStructDoc</a>, au lieu d’ouvrir un <strong>Record</strong> existant.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Provoque une erreur d'exécution si <em>Source</em> pointe sur un nœud inexistant.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Modifie les indicateurs de création <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong> et <strong>adCreateStructDoc</strong>. Quand OR est utilisé avec cette valeur et l’une des valeurs d’indicateur de création, et si l’URL source pointe sur un nœud existant ou sur un objet <strong>Record</strong>, le fournisseur doit ouvrir le <strong>Record</strong> existant au lieu d’en créer un nouveau. Cette valeur ne peut pas être utilisée avec <strong>adCreateOverwrite</strong>.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

