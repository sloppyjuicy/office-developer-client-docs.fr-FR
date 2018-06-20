---
title: Définition des propriétés sur les Messages entrants
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f6233afffd532c420ae170ae45b1bf93d6571865
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787160"
---
# <a name="setting-properties-on-incoming-messages"></a>Définition des propriétés sur les Messages entrants

  
  
**S’applique à**: Outlook 
  
Les applications clientes dans le sous-système MAPI prévoient un nombre de propriétés dans tous les messages reçus. Lorsque le fournisseur de transport affiche un message MAPI, il doit définir ces propriétés, car il est le seul processus avec les informations nécessaires pour effectuer cette opération, ou est au moins la meilleure source d’informations.
  
Les fournisseurs sont invités à définir les valeurs de toutes ces propriétés dans les messages entrants.
  
|**Nom de la propriété**|**Description**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Objet du message.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texte du message en texte brut.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texte du message au format RTF compressé.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |La date et l’heure que le message a été remis.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Le nom complet de l’expéditeur du message.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |L’entrée d’adresse de l’expéditeur du message.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |La clé de recherche du livre adresse de l’expéditeur du message.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Heure à laquelle le message a été envoyé à son système de messagerie par le client de messagerie de l’expéditeur.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Le nom du délégué représentatif pour l’envoi.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |L’entrée d’adresse de l’envoi du délégué.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |La clé de recherche adresse téléchargeable du délégué envoi.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Le nom du délégué représentant pour la réception.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |L’entrée d’adresse du destinataire délégué.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |La clé de recherche du livre adresse du destinataire délégué.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |La liste des destinataires déléguée afficher les noms, séparés par un point-virgule et un espace (« ; »).  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |La liste des destinataires déléguées pour une réponse.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé comme destinataire « à » (pas dans un groupe).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé en tant que « cc » destinataire (pas dans un groupe).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indique que le destinataire a été nommé spécifiquement comme un « à », « cc » ou « Cci » destinataire (pas dans un groupe).  <br/> |
   
Fournisseurs ne dont aucun mappage apparente pour paramétrer le groupe **PR_SENT_REPRESENTING** de propriétés pour les mêmes valeurs que le groupe **PR_SENDER** , le groupe **PR_RCVD_REPRESENTING** de propriétés pour les mêmes valeurs que la **PR_RECEIVED_BY **de groupe et peut créer le groupe de **PR_REPLY_RECIPIENT** des propriétés en fonction des valeurs du groupe **PR_SENDER** . Par exemple, **PR_SENT_REPRESENTING_NAME** peut avoir la même valeur que **PR_SENDER_NAME**.
  
La propriété **PR_ENTRYID** ou **PR_ENTRYLIST** peut être générée, si nécessaire, en appelant la méthode [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . Le groupe **clé PR_SEARCH_KEY** de propriétés peut être généré par la concaténation de la propriété **TYPEADR_PR** associée à un utilisateur, un signe deux-points ( :)) et la propriété **ADRESSE_EMAIL_PR** associée à l’utilisateur, puis modifier le résultat en majuscules . La fonction API Windows **CharUpperBuff** est une fonction pratique à utiliser dans ce but. Ce processus est nécessaire pour rendre un formulaire de l’adresse qui peut être comparée en tant que binaire quantité canonique. Notez qu’il n’est pas nécessaire si le fournisseur de transport respecte la casse en ce qui concerne les adresses de messagerie. 
  

