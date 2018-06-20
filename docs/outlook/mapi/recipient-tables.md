---
title: Tables de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: cc7635c474b99898d59589f33fcf06cf24697378
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786968"
---
# <a name="recipient-tables"></a>Tables de destinataires

  
  
**S’applique à**: Outlook 
  
La table de destinataires contient des informations sur tous les destinataires d’un message. Tables de destinataires implémentés par les fournisseurs de banque de message et les applications clientes pour les utilisent. Accéder à une table de destinataires par un appel à la méthode [IMessage::GetRecipientTable](imessage-getrecipienttable.md) clients, ou si la banque de messages fournisseur prend en charge, à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Clients accéder aux tables de destinataires avec **OpenProperty** en spécifiant **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l’identificateur d’interface. Modifications apportées à une table de destinataires est possible en appelant la méthode [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
Tables de destinataires ont une colonne différente selon que le message a été envoyé. Les propriétés suivantes constituent la colonne obligatoire définie dans les tables de destinataires :
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Les propriétés facultatives sont les suivants :
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Messages envoyés doivent inclure les propriétés supplémentaires dans leur ensemble de colonnes requises :
  
- **TYPEADR_PR** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
En fonction de l’implémentation d’un fournisseur, des colonnes supplémentaires, telles que **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et [ENTRYID](entryid.md), peut-être dans le tableau.
  
Tout fournisseur de banque de message qui prend en charge la transmission des messages, comme indiqué par le bit STORE_SUBMIT_OK défini dans la propriété de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) du fournisseur — doit offrir un ensemble particulier de prise en charge restrictions dans une implémentation de la table des destinataires. Le **et**, **ou**, existent et restrictions de propriété sont les types de restrictions qui doivent être disponibles aux utilisateurs de la table de destinataires. Seuls les opérateurs égales et n’est pas égales doivent être pris en charge sur la restriction de propriété. Ces restrictions doivent fonctionner avec les propriétés suivantes :
  
- **TYPEADR_PR**
    
- **ADRESSE_EMAIL_PR** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

