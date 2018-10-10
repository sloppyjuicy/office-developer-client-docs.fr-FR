---
title: EnvoyerMessage, action de macro
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db82c2d0c8350d517044df5848f8c264b92e928d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470148"
---
# <a name="sendemail-macro-action"></a>EnvoyerMessage, action de macro


**S’applique à**: Access 2013 | Office 2013

L'action **EnvoyerMessage** envoie un message électronique.


> [!NOTE]
> <P>[!REMARQUE] L'action <STRONG>EnvoyerMessage</STRONG> est disponible uniquement dans les macros de données.</P>



## <a name="setting"></a>Paramètre

L'action **EnvoyerMessage** utilise les arguments suivants.

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
<td><p>Les destinataires du message dont les noms doivent figurer sur la ligne <strong>à</strong> du message. Séparez les noms des destinataires que vous spécifiez dans cet argument (et dans les arguments <em>Cc</em> et <em>Cci</em> ) par un point-virgule ( ;).</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc</strong></p></td>
<td><p>Non</p></td>
<td><p>Destinataires du message dont les noms doivent figurer sur la liste Cc (&quot;copie carbone&quot;) ligne du message.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Cci</strong></p></td>
<td><p>Non</p></td>
<td><p>Destinataires du message dont les noms doivent figurer dans le champ Cci (&quot;copie carbone invisible&quot;) ligne du message.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objet</strong></p></td>
<td><p>Non</p></td>
<td><p>Objet du message. Ce texte apparaît sur la ligne <strong>Objet</strong> du message.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Body</strong></p></td>
<td><p>Non</p></td>
<td><p>Texte que vous souhaitez inclure dans le corps du message électronique. Si vous laissez cet argument vide, aucun texte supplémentaire n’est inclus dans le message.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

L'action **EnvoyerMessage** est disponible uniquement dans les événements de macros **[Après suppression](after-delete-macro-event.md)**, **[Après insertion](after-insert-macro-event.md)** et **[Après MAJ](after-update-macro-event.md)**.

L'action **EnvoyerMessage** n'affiche pas le message en vue de sa modification.

