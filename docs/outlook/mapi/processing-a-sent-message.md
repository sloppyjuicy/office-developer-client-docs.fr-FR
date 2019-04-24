---
title: Traitement d'un message envoyé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351064"
---
# <a name="processing-a-sent-message"></a>Traitement d'un message envoyé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages sortants, une fois envoyés, peuvent être laissés dans le dossier boîte d'envoi, déplacé vers un dossier destiné à recevoir les messages envoyés, ou supprimé. Le type de traitement varie selon que vous avez ou non défini les propriétés de la base de messages:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** est une propriété booléenne, définie sur true si les messages doivent être supprimés après leur envoi, et false dans le cas contraire. **PR_SENTMAIL_ENTRYID** est l'identificateur d'entrée d'un dossier. Lorsque cette propriété est définie, vous devez déplacer les messages envoyés vers le dossier représenté par cet identificateur d'entrée. Les messages enregistrés ont généralement l'identité du dernier fournisseur de messagerie ou de transport pour les envoyer. 
  
L'une ou l'autre, ou aucune de ces propriétés, ne doit être définie, mais pas les deux. Toutefois, si vous définissez **PR_SENTMAIL_ENTRYID**, il doit contenir un identificateur d'entrée valide. 
  
Le tableau suivant décrit la façon dont ces propriétés affectent ce que vous faites avec des messages envoyés.
  
|||
|:-----|:-----|
|Si aucune des propriétés n'est définie:  <br/> |Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d'envoi).  <br/> |
|Si **PR_SENTMAIL_ENTRYID** est défini:  <br/> |Déplacer le message vers le dossier indiqué.  <br/> |
|Si **PR_DELETE_AFTER_SUBMIT** est défini:  <br/> |Supprimez le message.  <br/> |
   

