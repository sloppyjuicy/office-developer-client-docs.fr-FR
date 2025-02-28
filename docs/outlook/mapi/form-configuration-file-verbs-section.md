---
title: Section Fichier de configuration de formulaire [Verbes]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
ms.openlocfilehash: 22acbf85e4d554c3aedb8d58e85167e5448672a2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63369972"
---
# <a name="form-configuration-file-verbs-section"></a>Section Fichier de configuration de formulaire [Verbes]

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La section **[Verbes] répertorie** l’ensemble complet des verbes pris en charge par le formulaire. Le format de la section **[Verbes]** est le suivante : 
  
 **[Verbes]**
  
 **Verb1** =   _string_
  
Voici un exemple de section **[Verbes** ]. 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Chaque verbe est défini dans un **[Verbe.** _string_ **]** section. A **[Verbe.** _section_ **]** décrit un verbe unique proposé par le formulaire. Entrée **DisplayName** dans un **[Verbe.** _section_ **]** spécifie le nom de la commande affiché dans l’interface utilisateur. **L’entrée** de code correspond au numéro de verbe transmis dans la méthode [IMAPIForm::D oVerb](imapiform-doverb.md). Syntaxe du **[Verbe.** _la_ section **string ]** est la suivante : 
  
 **[Verbe.** _string_ **]**
  
 **DisplayName** =   _chaîne affichée_
  
 **Code** =   _integer_
  
  =   Indicateurs _integer_
  
 **Attribs** =   _integer_
  
Voici un exemple de **[Verbe.** _string_ **]** section. 
  
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

Les verbes répertoriés dans cette section sont récupérés par un client à l’aide de la méthode [IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md). Les verbes sont activés en appelant la méthode [IMAPIForm::D oVerb](imapiform-doverb.md) du formulaire et en lui passant le numéro de code du verbe à exécuter. 
  

