---
title: If...Then...Else, bloc de macro
TOCTitle: If...Then...Else macro block
ms:assetid: 0c4a4b7a-4fdb-9dbc-a94e-939a2ff1c0e5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845158(v=office.15)
ms:contentKeyID: 48543188
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 7ac02a1fcd92384354f1ec337c95210e4fb2ceba
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63630643"
---
# <a name="ifthenelse-macro-block"></a>If...Then...Else, bloc de macro


**S’applique à** : Access 2013, Office 2013

Vous pouvez utiliser le bloc de macro **If** pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.

```vb
    If expression Then 
     Insert macro actions here ... 
    Else If expression 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

## <a name="setting"></a>Paramètre

Pour les deux **if** et **Else if**, les arguments suivants sont requis.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument de l’action</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Expression</strong></p></td>
<td><p>Condition que vous souhaitez tester. Il doit s’agir d’une expression qui donne une valeur True ou False.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Remarques

Lorsque vous sélectionnez le bloc de macro **If**, une zone de texte s'affiche afin de vous permettre d'entrer une expression qui représente la condition à tester. De plus, une zone de liste déroulante s'affiche, dans laquelle vous pouvez insérer une action de macro, sous laquelle le texte « End If » s'affiche automatiquement. If et End If entourent une zone dans laquelle vous pouvez entrer un groupe, ou bloc, d'actions. Le bloc s'exécute seulement si l'expression que vous entrez a la valeur True.

Pour évaluer une expression différente lorsque la première expression est False, vous pouvez cliquer sur **Ajouter Sinon si** pour insérer un bloc **Else If** facultatif. Vous devez entrer une expression évaluée à True ou False. Dans ce cas, le bloc s'exécute uniquement si l'expression a la valeur True et que la première expression a la valeur False.

Vous pouvez ajouter autant de blocs **Else if** que vous le souhaitez à un bloc If.

Vous pouvez cliquer sur **Ajouter Sinon** pour insérer un bloc **Else** facultatif. Dans ce cas, les actions que vous insérez sous **Else** forment le bloc **Else**, qui s'exécute uniquement lorsque les actions plus haut ne s'exécutent pas. Vous pouvez ajouter un seul bloc **Else** à un bloc **If**.

Dans l'exemple de code suivant, les actions de macro du premier bloc s'exécutent si la valeur de \[Status\] est supérieure à 0. Si la valeur de \[Status\] n'est pas supérieure à 0, l'expression qui suit **Else If** est évaluée. Les actions de macro du bloc **Else If** s'exécutent si la valeur de \[Status\] est égale à 0. Pour finir, si ni le premier ni le deuxième bloc ne s'exécutent, les actions du bloc **Else** s'exécutent.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
    Else If [Status] = 0 
     Insert macro actions here ... 
    Else 
     Insert macro actions here ... 
    End If
```

Vous pouvez imbriquer des blocs **If**. Il peut être préférable d'imbriquer un bloc **If** dans un bloc **If** si vous souhaitez évaluer une deuxième expression lorsque la première expression a la valeur True. Dans l'exemple de code suivant, le bloc **If** interne s'exécute uniquement lorsque la valeur de \[Status\] est à la fois supérieure à 0 *et* supérieure à 100.

```vb
    If [Status] > 0 Then 
     Insert macro actions here ... 
     If [Status] > 100 
     Insert macro actions here ... 
     EndifEnd If
```
