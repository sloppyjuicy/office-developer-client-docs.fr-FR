---
title: Section [verbes] du fichier de configuration de formulaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: bb7d49d69fadab54212ff7e8b50ac969e4890c0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327495"
---
# <a name="form-configuration-file-verbs-section"></a>Section [verbes] du fichier de configuration de formulaire

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Verbs]** répertorie l'ensemble complet des verbes pris en charge par le formulaire. Le format de la section **[Verbs]** est le suivant: 
  
 **Verbes**
  
 **** =  _Chaîne_ Verb1
  
Voici un exemple de section **[Verbs]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Chaque verbe est défini dans un **verbe [Verb.** _String (chaîne_ ) **]** . Un **verbe.** _String (chaîne_ ) **]** décrit un verbe unique offert par le formulaire. L'entrée **DisplayName** dans un **verbe [.** _String (chaîne_ ) **]** indique le nom de la commande affiché dans l'interface utilisateur. L'entrée de **code** correspond au numéro de verbe transmis dans la méthode [IMAPIForm::D overb](imapiform-doverb.md) . Syntaxe du **verbe [.** _String (chaîne_ ) **]** est la suivante: 
  
 **Action.** _String (chaîne_ ) **]**
  
 **** =  _Chaîne affichée_ DisplayName
  
 **** =  _Entier_ de code
  
 **Indicateurs** =  de_nombre entier_
  
 **** =  _Entier_ attribs
  
Voici un exemple d'un **verbe [verbe.** _String (chaîne_ ) **]** . 
  
```cpp
[Verb.1]
DisplayName=Reply
code=1
Flags=0
Attribs=2
[Verb.2]
DisplayName=Delete
Code=2
Flags=0
Attribs=2

```

Les verbes répertoriés dans cette section sont récupérés par un client à l'aide de la [méthode IMAPIFormInfo:: CalcVerbSet](imapiforminfo-calcverbset.md). Les verbes sont activés en appelant la méthode [IMAPIForm::D overb](imapiform-doverb.md) et en lui transmettant le numéro de code du verbe à effectuer. 
  

