---
title: SendEmail, action de macro
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314650"
---
# <a name="sendemail-macro-action"></a>SendEmail, action de macro

**S’applique à** : Access 2013, Office 2013

**L’action EnvoyerEmail** envoie un message électronique.

> [!NOTE]
> L’action **EnvoyerMessage** est disponible uniquement dans les macros de données.

## <a name="setting"></a>Setting

L’action **EnvoyerMessage** utilise les arguments suivants.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Obligatoire</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Pour</strong></p></td>
<td><p>Oui</p></td>
<td><p>Destinataires du message dont vous souhaitez placer les noms sur la ligne <strong>À</strong> du message. Séparez les noms des destinataires que vous spécifiez dans cet argument (et dans les arguments <em>Cc</em> et <em>Cci)</em> par un point-virgule (;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Non</p></td>
<td><p>Destinataires du message dont vous souhaitez placer les noms sur la ligne Cc (copie &quot; &quot; carbone) du message.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc</strong></p></td>
<td><p>Non</p></td>
<td><p>Destinataires du message dont vous souhaitez placer les noms sur la ligne Bcc (copie carbone non &quot; &quot; voyante) du message.</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject</strong></p></td>
<td><p>Non</p></td>
<td><p>Objet du message. Ce texte apparaît sur la ligne <strong>Objet</strong> du message.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Corps</strong></p></td>
<td><p>Non</p></td>
<td><p>Texte que vous souhaitez inclure dans le corps du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

L'action **EnvoyerMessage** est disponible uniquement dans les événements de macros **[Après suppression](after-delete-macro-event.md)**, **[Après insertion](after-insert-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.

L'action **EnvoyerMessage** n'affiche pas le message en vue de sa modification.

