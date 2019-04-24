---
title: Tables de destinataires
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328419"
---
# <a name="recipient-tables"></a>Tables de destinataires

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La table de destinataires contient des informations sur tous les destinataires d'un message. Les fournisseurs de banque de messages implémentent les tables de destinataires et les applications clientes les utilisent. Les clients accèdent à une table de destinataires en appelant la méthode [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) ou, si le fournisseur de banque de messages le prend en charge, à la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Les clients accèdent aux tables de destinataires avec **OpenProperty** en spécifiant **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) pour la balise de propriété et IID_IMAPITable pour l'identificateur d'interface. Les modifications apportées à une table de destinataires peuvent être effectuées en appelant la méthode [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . 
  
Les tables de destinataires ont un jeu de colonnes différent selon que le message a été envoyé ou non. Les propriétés suivantes constituent le jeu de colonnes obligatoire dans les tables de destinataires:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
Les propriétés facultatives sont les suivantes:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Les messages envoyés doivent inclure ces propriétés supplémentaires dans leur jeu de colonnes obligatoire:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
En fonction de l'implémentation d'un fournisseur, des colonnes supplémentaires, telles que **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) et [EntryID](entryid.md), peuvent se trouver dans le tableau.
  
Tout fournisseur de banque de messages qui prend en charge la transmission des messages, comme indiqué par le bit STORE_SUBMIT_OK défini dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) du fournisseur, doit proposer une prise en charge pour un ensemble particulier de restrictions dans l'implémentation d'une table de destinataires. Les restrictions **and**, **or**, EXISTS et Property figurent parmi les types de restrictions qui doivent être disponibles pour les utilisateurs de la table de destinataires. Seuls les opérateurs égales et non égales doivent être pris en charge sur la restriction de propriété. Ces restrictions doivent fonctionner avec les propriétés suivantes:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Voir aussi



[Tables MAPI](mapi-tables.md)

