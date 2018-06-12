---
title: If... Procédez comme suit... Bloc de Macro else (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Vous pouvez utiliser If bloc de macro à exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.
ms.openlocfilehash: 8ac78ff0eaf22c1d821e306654ebfa8fac4ed34a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781834"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>If... Procédez comme suit... Bloc de Macro else (accès personnalisé web app)

Vous pouvez utiliser le bloc de macro **If** pour exécuter de façon conditionnelle un groupe d'actions, selon la valeur d'une expression. 
  
> [!IMPORTANT]
> [!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
## <a name="syntax"></a>Syntaxe

```vb
IfexpressionThen 
 Insert macro actions here ... 
Else Ifexpression  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

## <a name="setting"></a>Paramètre

Pour les deux **Si** et ** Else If **, les arguments suivants sont requis. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
|**Expression** <br/> |La condition que vous souhaitez tester. Il doit être une expression qui prend la valeur True ou False.  <br/> |
   
## <a name="remarks"></a>Notes

Lorsque vous sélectionnez le bloc de macro **If**, une zone de texte s'affiche afin de vous permettre d'entrer une expression qui représente la condition à tester. De plus, une zone de liste déroulante s'affiche, dans laquelle vous pouvez insérer une action de macro, sous laquelle le texte « End If » s'affiche automatiquement. If et End If entourent une zone dans laquelle vous pouvez entrer un groupe, ou bloc, d'actions. Le bloc s'exécute seulement si l'expression que vous entrez a la valeur True. 
  
Pour évaluer une expression différente lorsque la première expression est False, vous pouvez cliquer sur **Ajouter Sinon si** pour insérer un bloc **Else If** facultatif. Vous devez entrer une expression évaluée à True ou False. Dans ce cas, le bloc s'exécute uniquement si l'expression a la valeur True et que la première expression a la valeur False. 
  
Vous pouvez ajouter autant de blocs **Else if** que vous le souhaitez à un bloc If. 
  
Vous pouvez cliquer sur **Ajouter Sinon** pour insérer un bloc **Else** facultatif. Dans ce cas, les actions que vous insérez sous **Else** forment le bloc **Else**, qui s'exécute uniquement lorsque les actions plus haut ne s'exécutent pas. Vous pouvez ajouter un seul bloc **Else** à un bloc **If**. 
  
Dans l'exemple de code suivant, les actions de macro du premier bloc s'exécutent si la valeur de [Status] est supérieure à 0. Si la valeur de [Status] n'est pas supérieure à 0, l'expression qui suit **Else If** est évaluée. Les actions de macro du bloc **Else If** s'exécutent si la valeur de [Status] est égale à 0. Pour finir, si ni le premier ni le deuxième bloc ne s'exécutent, les actions du bloc **Else** s'exécutent. 
  
```vb
If[Status] > 0Then 
 Insert macro actions here ... 
Else If[Status] = 0  
 Insert macro actions here ... 
Else 
 Insert macro actions here ... 
End If
```

Vous pouvez imbriquer des blocs **If**. Il peut être préférable d'imbriquer un bloc **If** dans un bloc **If** si vous souhaitez évaluer une deuxième expression lorsque la première expression a la valeur True. Dans l'exemple de code suivant, le bloc **If** interne s'exécute uniquement lorsque la valeur de [Status] est à la fois supérieure à 0  *et*  supérieure à 100. 
  

