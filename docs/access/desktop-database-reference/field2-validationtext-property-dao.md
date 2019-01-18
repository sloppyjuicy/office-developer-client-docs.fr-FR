---
title: Propriété Field2.ValidationText (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6128f66c-3891-ae4d-d12d-354a79a9c05e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194867(v=office.15)
ms:contentKeyID: 48545202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4d58cb6bd32bd46b0a6bcec40ff68cdc52eebc31
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698245"
---
# <a name="field2validationtext-property-dao"></a>Propriété Field2.ValidationText (DAO)


**S’applique à**: Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field2** ne respecte par la règle de validation spécifiée par le paramètre de propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*expression* . ValidationText (MessageSiErreur)

*expression* Variable qui représente un objet **Field2** .

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
<td><p>Non pris en charge</p></td>
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
<td><p>Non pris en charge</p></td>
</tr>
<tr class="odd">
<td><p><strong>TableDef</strong></p></td>
<td><p>En lecture-écriture.</p></td>
</tr>
</tbody>
</table>

