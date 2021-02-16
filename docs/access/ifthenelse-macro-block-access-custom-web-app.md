---
title: Si... Ensuite... Else Macro Block (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 18d28dc1-c41f-47c6-b5c7-258d5f877d01
description: Vous pouvez utiliser le bloc de macro If pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression.
ms.openlocfilehash: 6fe82e2c42f8e5d93cdc26798e7572e32d6cdc7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434493"
---
# <a name="ifthenelse-macro-block-access-custom-web-app"></a>Si... Ensuite... Else Macro Block (Access custom web app)

Vous pouvez utiliser le bloc de macro **If** pour exécuter de façon conditionnelle un groupe d’actions, selon la valeur d’une expression. 
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 
  
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

## <a name="setting"></a>Setting

For both **If** and ** Else If **, the following arguments are required. 
  
|**Argument de l'action**|**Description**|
|:-----|:-----|
|**Expression** <br/> |Condition que vous souhaitez tester. Il doit s’agir d’une expression évaluée à True ou False.  <br/> |
   
## <a name="remarks"></a>Remarques

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
  

