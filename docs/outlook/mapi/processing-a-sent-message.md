---
title: Traitement d’un message envoyé
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 969977764539c05735704f9bceea45c2c84036e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624404"
---
# <a name="processing-a-sent-message"></a>Traitement d’un message envoyé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les messages sortants, une fois envoyés, peuvent être laissés dans le dossier Boîte d’envoi, déplacés vers un dossier désigné pour contenir les messages envoyés ou supprimés. Le type de traitement varie selon que vous avez ou non définie les propriétés de la boutique de messages :
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** est une propriété Boolean, définie sur TRUE si les messages doivent être supprimés après leur envoi, et FALSE dans le cas contraire. **PR_SENTMAIL_ENTRYID** est l’identificateur d’entrée d’un dossier. Lorsque cette propriété est définie, vous devez déplacer les messages envoyés vers le dossier représenté par cet identificateur d’entrée. Les messages enregistrés ont généralement l’identité de la dernière boutique de messages ou du dernier fournisseur de transport pour les envoyer. 
  
L’une ou l’autre, ou aucune de ces propriétés ne doit être définie, mais pas les deux. Toutefois, si vous définissez **PR_SENTMAIL_ENTRYID,** il doit contenir un identificateur d’entrée valide. 
  
Le tableau suivant décrit comment ces propriétés affectent ce que vous faites avec les messages envoyés.
  
|||
|:-----|:-----|
|Si aucune des deux propriétés n’est définie :  <br/> |Laissez le message dans le dossier à partir duquel il a été envoyé (généralement la boîte d’envoi).  <br/> |
|Si **PR_SENTMAIL_ENTRYID** est définie :  <br/> |Déplacez le message vers le dossier indiqué.  <br/> |
|Si **PR_DELETE_AFTER_SUBMIT** est définie :  <br/> |Supprimez le message.  <br/> |
   

