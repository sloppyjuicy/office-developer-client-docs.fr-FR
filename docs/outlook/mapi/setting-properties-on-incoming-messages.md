---
title: Définition des propriétés sur les messages entrants
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: cf4a0501-f42b-4652-a239-003022686475
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4e5b9c80b872dfae1a2b9f9788c1a5eebd134186
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782555"
---
# <a name="setting-properties-on-incoming-messages"></a>Définition des propriétés sur les messages entrants

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes au sein du sous-système MAPI attendent un certain nombre de propriétés dans un message reçu. Lorsque le fournisseur de transport envoie un message dans MAPI, il doit définir ces propriétés, car il s’agit soit du seul processus avec les informations nécessaires pour le faire, soit au moins de la meilleure source d’informations.
  
Les fournisseurs sont encouragés à définir les valeurs de toutes ces propriétés dans les messages entrants.
  
|**Nom de la propriété**|**Description**|
|:-----|:-----|
|**PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |Objet du message. |
|**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))  <br/> |Texte du message en texte simple. |
|**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md))  <br/> |Texte compressé du message RTF. |
|**PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |Date et heure de livraison du message. |
|**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |Nom complet de l’auteur du message. |
|**PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md))  <br/> |Entrée du carnet d’adresses de l’auteur du message. |
|**PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md))  <br/> |Clé de recherche du carnet d’adresses de l’auteur du message. |
|**PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md))  <br/> |Heure à quoi le message a été envoyé à son système de messagerie par le client de messagerie de l’expéditeur. |
|**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |Nom du délégué représentatif pour l’envoi. |
|**PR_SENT_REPRESENTING_ENTRYID** ([PidTagSentRepresentingEntryId](pidtagsentrepresentingentryid-canonical-property.md))  <br/> |Entrée du carnet d’adresses du délégué d’envoi. |
|**PR_SENT_REPRESENTING_SEARCH_KEY** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md))  <br/> |Clé de recherche du carnet d’adresses du délégué d’envoi. |
|**PR_RCVD_REPRESENTING_NAME** ([PidTagReceivedRepresentingName](pidtagreceivedrepresentingname-canonical-property.md))  <br/> |Nom du délégué représentatif à recevoir. |
|**PR_RCVD_REPRESENTING_ENTRYID** ([PidTagReceivedRepresentingEntryId](pidtagreceivedrepresentingentryid-canonical-property.md))  <br/> |Entrée du carnet d’adresses du délégué de réception. |
|**PR_RCVD_REPRESENTING_SEARCH_KEY** ([PidTagReceivedRepresentingSearchKey](pidtagreceivedrepresentingsearchkey-canonical-property.md))  <br/> |Clé de recherche du carnet d’adresses du délégué de réception. |
|**PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md))  <br/> |Liste des noms d’affichage des destinataires délégués, séparés par un point-virgule et un espace (« ; « ). |
|**PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md))  <br/> |Liste des destinataires délégués pour une réponse. |
|**PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé en tant que destinataire « à » (et non dans un groupe). |
|**PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé en tant que destinataire « cc » (et non dans un groupe). |
|**PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))  <br/> |Indique que le destinataire a été spécifiquement nommé en tant que destinataire « à », « cc » ou « Cci » (pas dans un groupe). |
   
Les fournisseurs qui n’ont aucun mappage apparent peuvent définir le groupe de propriétés **PR_SENT_REPRESENTING** sur les mêmes valeurs que le groupe **PR_SENDER** , le groupe de propriétés **PR_RCVD_REPRESENTING** sur les mêmes valeurs que le groupe **PR_RECEIVED_BY** et peuvent créer le groupe de propriétés **PR_REPLY_RECIPIENT** en fonction des valeurs du groupe **PR_SENDER** . Par exemple, **PR_SENT_REPRESENTING_NAME** peut être définie sur la même valeur que **PR_SENDER_NAME**.
  
La **PR_ENTRYID** ou **PR_ENTRYLIST** peut être générée, si nécessaire, en appelant la méthode [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . Le **groupe** de propriétés PR_SEARCH_KEY peut être généré en concassant la propriété **PR_ADDRTYPE** associée à un utilisateur, un deux-points (:) et la propriété **PR_EMAIL_ADDRESS** associée à l’utilisateur, puis en modifiant le résultat en minuscules. La Windows API **CharUpperBuff** est une fonction pratique à utiliser à cet effet. Ce processus exige la création d’une forme canonique de l’adresse qui peut être comparée en tant que quantité binaire. Notez que cela n’est pas nécessaire si le fournisseur de transport respecte la cas par rapport aux adresses e-mail. 
  

