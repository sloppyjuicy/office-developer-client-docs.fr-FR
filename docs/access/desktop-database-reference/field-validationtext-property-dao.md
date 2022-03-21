---
title: Field.ValidationText, propriété (DAO)
TOCTitle: ValidationText Property
ms:assetid: 6d9ec790-a9d2-84d7-ccba-57d738491e36
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195540(v=office.15)
ms:contentKeyID: 48545494
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 99cdf3fd82d65d956a6c877f3c7cf637b9ba5646
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63632153"
---
# <a name="fieldvalidationtext-property-dao"></a>Field.ValidationText, propriété (DAO)


**S’applique à** : Access 2013, Office 2013

Définit ou renvoie une valeur qui spécifie le texte du message que votre application affiche si la valeur d'un objet **Field** n'est pas conforme à la règle de validation spécifiée par la valeur de la propriété **ValidationRule** (espaces de travail Microsoft Access uniquement). Valeur **String** en lecture-écriture.

## <a name="syntax"></a>Syntaxe

*.* ValidationText

*expression* Variable qui représente un objet **Field**.

## <a name="remarks"></a>Remarques

Le paramètre ou la valeur de retour est une chaîne (type de données **String**) qui spécifie le texte affiché lorsqu'un utilisateur tente d'entrer une valeur non valide dans un champ. Cette propriété est en lecture/écriture pour les objets non encore ajoutés à une collection.

Pour un objet **Field**, l'utilisation de la propriété **ValidationText** dépend de l'objet contenant la collection **[Fields](fields-collection-dao.md)** à laquelle est ajouté l'objet **Field**, comme le montre le tableau suivant.

<table>
<colgroup>
<col />
<col />
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

