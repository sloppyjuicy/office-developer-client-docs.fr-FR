---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300692"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**S’applique à** : Access 2013, Office 2013

Spécifie si un **Record** doit être ouvert ou si un nouveau **Record** doit être créé pour la méthode [Open](record-object-ado.md) de l'objet [Record](open-method-ado-record.md) . Les valeurs peuvent être combinées avec un opérateur AND.

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

