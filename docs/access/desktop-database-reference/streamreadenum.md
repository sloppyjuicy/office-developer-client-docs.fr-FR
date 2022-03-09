---
title: StreamReadEnum (référence de base de données de bureau Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5a1aeaba60be5179102a52b49a51bc6036601202
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463127"
---
# <a name="streamreadenum"></a>StreamReadEnum

**S’applique à** : Access 2013, Office 2013

Spécifie si la chaîne de données entière ou si la ligne suivante doit être lue depuis un objet [Stream](stream-object-ado.md).


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
<td><p><strong>adReadAll</strong></p></td>
<td><p>-1</p></td>
<td><p>Par défaut. Lit tous les octets de la chaîne de données, depuis la position en cours jusqu’au marqueur <a href="eos-property-ado.md">EOS</a>. C’est la seule valeur à chaînes binaires <strong>StreamReadEnum</strong> valide (le <a href="type-property-ado-stream.md">Type</a> est <strong>adTypeBinary</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adReadLine</strong></p></td>
<td><p>-2</p></td>
<td><p>Lit la ligne suivante de la chaîne (désignée par la propriété <a href="lineseparator-property-ado.md">LineSeparator</a>).</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Équivalent ADO/WFC

Ces constantes ne possèdent pas d'équivalent ADO/WFC.

