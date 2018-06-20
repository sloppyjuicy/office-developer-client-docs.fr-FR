---
title: Section de formulaire Configuration de fichier [verbes]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e7e1f371-9e9a-4bec-a0b3-87753a16f5e0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5fe1b064b48bc9112a872677fbf5042b7dfe5449
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783343"
---
# <a name="form-configuration-file-verbs-section"></a>Section de formulaire Configuration de fichier [verbes]

  
  
**S’applique à**: Outlook 
  
La section **[verbes]** répertorie l’ensemble complet des verbes pris en charge par le formulaire. Le format de la section **[verbes]** est la suivante : 
  
 **[Verbes]**
  
 **Verb1** =  _chaîne_
  
Voici un exemple d’une section **[verbes]** . 
  
```cpp
[Verbs]
Verb1=1
Verb2=2

```

Chaque verbe est défini dans un distinct **[verbe.** _chaîne_ section **]** . A **[verbe.** _chaîne_ section **]** décrit un verbe unique offert par le formulaire. L’entrée **DisplayName** dans un **[verbe.** _chaîne_ section **]** Spécifie le nom de la commande affiché dans l’interface utilisateur. L’entrée de **Code** correspond au numéro de verbe passé dans la méthode [IMAPIForm::DoVerb](imapiform-doverb.md) . La syntaxe de la **[verbe.** _chaîne_ section **]** est : 
  
 **[Verbe.** _chaîne_ **]**
  
 **DisplayName** =  _affiche la chaîne_
  
 **Code** =  _entier_
  
 **Indicateurs** =  _entier_
  
 **Attributs** =  _entier_
  
Voici un exemple d’un **[verbe.** _chaîne_ section **]** . 
  
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

Les verbes répertoriés dans cette section sont récupérés par un client à l’aide de la [méthode IMAPIFormInfo::CalcVerbSet](imapiforminfo-calcverbset.md). Verbes sont activés en appelant la méthode du formulaire [IMAPIForm::DoVerb](imapiform-doverb.md) et en lui transmettant le numéro de code de l’action à effectuer. 
  

