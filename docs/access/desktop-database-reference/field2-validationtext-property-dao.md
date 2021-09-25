---
title: Field2.ValidationText, propriété (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a2c4d3ae0d681cbb6863ae44ed098f2cc0404d06
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552933"
---
# <a name="field2validationtext-property-dao"></a>Field2.ValidationText, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field2** ne respecte par la règle de validation spécifiée par le paramètre de propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* ValidationText

*expression* une variable qui représente une **champ2** objet.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une **String** qui spécifie le texte affiché si un utilisateur tente d'entrer une valeur non valide pour un champ. Pour un objet pas encore ajouté à une collection, cette propriété est en lecture/écriture.

Pour un objet **Field2**, l'utilisation de la propriété **ValidationText** dépend de l'objet qui contient la collection **[Fields](fields-collection-dao.md)** à laquelle l'objet **Field2** est ajouté, comme illustré dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objet ajouté à</p></th>
<th><p>Utilisation</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Index</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="even">
<td><p><strong>QueryDef</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="odd">
<td><p><strong>Recordset</strong></p></td>
<td><p>Lecture seule</p></td>
</tr>
<tr class="even">
<td><p><strong>Relation</strong></p></td>
<td><p>Non reconnu</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>Lecture/écriture</p></td>
</tr>
</tbody>
</table>

