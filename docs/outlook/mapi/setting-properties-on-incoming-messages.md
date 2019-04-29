---
title: Définition des propriétés sur les messages entrants
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: d7043004799d534f11aa98770e2e323cbdae95a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432694"
---
# <a name="setting-properties-on-incoming-messages"></a>Définition des propriétés sur les messages entrants

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes au sein du sous-système MAPI attendent un certain nombre de propriétés dans n'importe quel message reçu. Lorsque le fournisseur de transport remet un message dans MAPI, il doit définir ces propriétés, car il s'agit du seul processus avec les informations nécessaires à ce faire, ou il s'agit au moins de la meilleure source d'informations.
  
Les fournisseurs sont encouragés à définir les valeurs de toutes ces propriétés dans les messages entrants.
  
|**Nom de la propriété**|**Description**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Objet du message.  <br/> |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texte du message en texte brut.  <br/> |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texte de message RTF compressé.  <br/> |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Date et heure auxquelles le message a été remis.  <br/> |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom complet de l'expéditeur du message.  <br/> |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Entrée de carnet d'adresses de l'expéditeur du message.  <br/> |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |La clé de recherche de carnet d'adresses de l'expéditeur du message.  <br/> |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Heure à laquelle le message a été envoyé à son système de messagerie par le client de messagerie de l'expéditeur.  <br/> |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Nom du délégué représentatif pour l'envoi.  <br/> |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Entrée de carnet d'adresses du délégué d'envoi.  <br/> |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |La clé de recherche de carnet d'adresses du délégué d'envoi.  <br/> |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Nom du délégué représentatif pour la réception.  <br/> |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Entrée de carnet d'adresses du délégué de réception.  <br/> |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |La clé de recherche de carnet d'adresses du délégué de réception.  <br/> |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Liste des noms d'affichage de destinataires délégués, séparés par un point-virgule et un espace («;»).  <br/> |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Liste des destinataires délégués pour une réponse.  <br/> |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé comme destinataire «à» (et non dans un groupe).  <br/> |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé comme destinataire «CC» (et non dans un groupe).  <br/> |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé comme destinataire «à», «CC» ou «CCI» (pas dans un groupe).  <br/> |
   
Les fournisseurs qui n'ont pas de mappages apparent peuvent définir le groupe **PR_SENT_REPRESENTING** de propriétés sur les mêmes valeurs que le groupe **PR_SENDER** , le groupe **PR_RCVD_REPRESENTING** de propriétés aux mêmes valeurs que le **PR_RECEIVED_BY **Group, et peut créer le groupe **PR_REPLY_RECIPIENT** de propriétés basé sur les valeurs du groupe **PR_SENDER** . Par exemple, **PR_SENT_REPRESENTING_NAME** peut être défini sur la même valeur que **PR_SENDER_NAME**.
  
La propriété **PR_ENTRYID** ou **PR_ENTRYLIST** peut être générée, si nécessaire, en appelant la méthode [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) . Le groupe **PR_SEARCH_KEY** de propriétés peut être généré en concaténant la propriété **PR_ADDRTYPE** associée à un utilisateur, un signe deux-points (:) et la propriété **PR_EMAIL_ADDRESS** associée à l'utilisateur, puis en modifiant le résultat en majuscules . La fonction d'API Windows **CharUpperBuff** est une fonction pratique à utiliser à cette fin. Ce qui est nécessaire pour ce processus est de créer une forme canonique de l'adresse qui peut être comparée en tant que quantité binaire. Notez que cette fonction n'est pas nécessaire si le fournisseur de transport respecte la casse des adresses de messagerie. 
  

