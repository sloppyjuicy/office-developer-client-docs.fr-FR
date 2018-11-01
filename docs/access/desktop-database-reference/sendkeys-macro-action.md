---
title: EnvoiTouches, action de macro
TOCTitle: SendKeys Macro Action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3f8ddc6c19f675db7cc04cb46a24e0f42ac991df
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881355"
---
# <a name="sendkeys-macro-action"></a>EnvoiTouches, action de macro


**S’applique à**: Access 2013, Office 2013

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="Remarque sur la sécurité" alt="Security note" />de sécurité**</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      Évitez d’utiliser l’instruction <strong>SendKeys</strong> ou une macro AutoKeys avec des informations sensibles et confidentielles. Un utilisateur malveillant pourrait intercepter la frappe et compromettre la sécurité de votre ordinateur et de vos données.
</td>
</tr>
</tbody>
</table>


Vous pouvez utiliser l'action **EnvoiTouches** pour envoyer directement une séquence de touches à Microsoft Access ou à une application Windows active.


> [!NOTE]
> <P>[!REMARQUE] Cette action ne sera pas autorisée si la base de données n'est pas approuvée. Pour plus d'informations sur l'activation des macros, voir les liens dans la section See Alsode cet article.</P>



## <a name="setting"></a>Valeur

L'action **EnvoiTouches** accepte les arguments suivants.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Touches</strong></p></td>
<td><p>Séquence de touches qu’Access ou l’application doit traiter. Entrez la séquence de touches dans la zone <strong>Touches</strong> de la section <strong>Arguments de l’action</strong> du volet Générateur de macro. Cette zone peut contenir jusqu’à 255 caractères. Cet argument est obligatoire.</p></td>
</tr>
<tr class="even">
<td><p><strong>Wait</strong></p></td>
<td><p>Spécifie si la macro doit attendre que la séquence de touches ait été traitée. Cliquez sur <strong>Oui</strong> (pour attendre) ou <strong>Non</strong> (pour ne pas attendre). La valeur par défaut est <strong>Non</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Notes

Access traite la séquence de touches qu'il reçoit via l'action **EnvoiTouches** comme si vous l'aviez tapée directement dans une fenêtre Access.

Pour spécifier la séquence de touches, utilisez la même syntaxe que celle utilisée dans l'instruction **EnvoiTouches**.


> [!NOTE]
> <P>[!REMARQUE] Une erreur peut se produire si l'argument <STRONG>Touches</STRONG> contient une syntaxe incorrecte, du texte mal orthographié ou des valeurs non appropriées pour la fenêtre à laquelle la séquence de touches est envoyée.</P>



Vous pouvez utiliser cette action pour entrer des informations dans une boîte de dialogue, notamment si vous ne voulez pas interrompre la macro pour répondre manuellement à la boîte de dialogue. Certaines actions Access, telles que **Imprimer** et **TrouverEnregistrement**, sélectionnent automatiquement les options de certaines boîtes de dialogue souvent utilisées. Vous pouvez utiliser l'action **EnvoiTouches** pour sélectionner des options de boîte de dialogue moins utilisées.


> [!NOTE]
> <UL>
> <LI>
> <P>Dans la mesure où la boîte de dialogue interrompt la macro, vous devez placer l'action <STRONG>EnvoiTouches</STRONG> avant l'action qui entraîne l'ouverture de la boîte de dialogue et définir l'argument <STRONG>Attendre</STRONG> la valeur sur <STRONG>Non</STRONG>.</P>
> <LI>
> <P>Il est parfois difficile d'estimer le temps qu'il faudra à la séquence de touches pour atteindre Access ou une autre application. En conséquence, lorsqu'il existe une autre méthode (telle que l'action <STRONG>TrouverEnregistrement</STRONG> ) pour effectuer la tâche souhaitée, il est conseillé d'utiliser cette méthode au lieu de l'action <STRONG>EnvoiTouches</STRONG> pour compléter les options d'une boîte de dialogue.</P></LI></UL>



Si vous voulez envoyer plus de 255 caractères à Access ou à une autre application Windows, vous pouvez utiliser successivement plusieurs actions **EnvoiTouches** dans une macro.

Le recours à l'action **EnvoiTouches** pour envoyer une séquence de touches déclenche les événements **KeyDown**, **KeyUp** et **KeyPress** appropriés. L'envoi d'une séquence de touches non-ANSI (une touche de fonction, par exemple) ne déclenche pas l'événement **KeyPress**.

Cette action n'est pas disponible à partir d'un module Visual Basic pour Applications (VBA). Utilisez dans ce cas l'instruction **SendKeys**.

