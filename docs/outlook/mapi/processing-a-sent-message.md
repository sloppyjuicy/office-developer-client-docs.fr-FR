---
title: Traitement d’un Message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786923"
---
# <a name="processing-a-sent-message"></a>Traitement d’un Message

  
  
**S’applique à**: Outlook 
  
Les messages, sortants une fois qu’ils ont été envoyés, peuvent rester dans la boîte d’envoi dossier, déplacé vers un dossier désigné pour stocker les messages envoyés ou supprimés. Le type de traitement dépend si vous avez défini le message banque de propriétés :
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** est une propriété booléenne, la valeur TRUE si les messages doivent être supprimées une fois qu’ils sont envoyés et FALSE dans le cas contraire. **PR_SENTMAIL_ENTRYID** est l’identificateur d’entrée d’un dossier. Lorsque cette propriété est définie, vous devez déplacer les messages envoyés vers le dossier représenté par cet identificateur d’entrée. En général, les messages enregistrés ont l’identité de la dernière banque d’informations ou de les envoyer au fournisseur de transport. 
  
Un ou l’autre des deux ou aucune de ces propriétés doit être ensemble, mais pas les deux. Toutefois, si vous définissez **PR_SENTMAIL_ENTRYID**, il doit contenir un identificateur d’entrée valide. 
  
Le tableau suivant décrit la façon dont ces propriétés affectent que faire avec des messages envoyés.
  
|||
|:-----|:-----|
|Si aucune propriété n’est définie :  <br/> |Laissez le message dans le dossier à partir de laquelle il a été envoyé (généralement la boîte d’envoi).  <br/> |
|Si **PR_SENTMAIL_ENTRYID** est défini :  <br/> |Déplacer le message vers le dossier indiqué.  <br/> |
|Si **PR_DELETE_AFTER_SUBMIT** est défini :  <br/> |Supprimer le message.  <br/> |
   

