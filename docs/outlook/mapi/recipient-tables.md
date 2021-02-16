---
title: Tables des destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437286"
---
# <a name="recipient-tables"></a>Tables des destinataires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table des destinataires contient des informations sur tous les destinataires d’un message. Les fournisseurs de magasins de messages implémentent les tables des destinataires et les applications clientes les utilisent. Les clients accèdent à une table des destinataires en appelant la méthode [IMessage::GetRecipientTable,](imessage-getrecipienttable.md) ou si le fournisseur de magasin de messages la prend en charge, à la méthode [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Clients access recipient tables with **OpenProperty** by specifying **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) for the property tag and IID_IMAPITable for the interface identifier. Les modifications apportées à une table des destinataires peuvent être apportées en appelant la méthode [IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
Les tables des destinataires ont un ensemble de colonnes différent selon que le message a été envoyé ou non. Les propriétés suivantes définissent la colonne requise dans les tables des destinataires :
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Les propriétés facultatives sont :
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Les messages envoyés doivent inclure ces propriétés supplémentaires dans l’ensemble de colonnes requis :
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Selon l’implémentation d’un fournisseur, des colonnes supplémentaires, telles que **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et [ENTRYID](entryid.md), peuvent être dans le tableau.
  
Tout fournisseur de magasins de messages qui prend en charge la transmission de messages, comme indiqué par le bit STORE_SUBMIT_OK en cours de paralocalisation dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)du fournisseur, doit prendre en charge un ensemble particulier de restrictions dans l’implémentation d’une table des destinataires. Les restrictions **and**, **OR**, existent et les restrictions de propriété font partie des types de restrictions qui doivent être disponibles pour les utilisateurs de la table des destinataires. Seuls les opérateurs égal et non égal doivent être pris en charge dans la restriction de propriété. Ces restrictions doivent fonctionner avec les propriétés suivantes :
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Voir aussi



[MAPI Tables](mapi-tables.md)

