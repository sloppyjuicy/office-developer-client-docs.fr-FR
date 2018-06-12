---
title: Envoi de Messages  T�ches du fournisseur de Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4625d9d09b067d064dac7ca67b7c79ebb818bcce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787120"
---
# <a name="sending-messages-transport-provider-tasks"></a>Envoi de Messages : T�ches du fournisseur de Transport

  
  
**S’applique à**: Outlook 
  
 **Pour transmettre un message, les fournisseurs de transport**
  
- Définissez la propriété du message **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) sur TRUE une fois que le fournisseur de transport a envoyé le message ou tenté d’envoyer le message. If an attempt to send a message fails, transport providers should call [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) to generate a nondelivery report. Si le message est envoyé avec succès et que la propriété **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) est définie sur TRUE, créez une structure [ADRLIST](adrlist.md) contenant les destinataires réussis, la propriété **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) pour chacun et appelez **StatusRecips** pour générer un rapport de remise. For more information about creating delivery and non-delivery reports, see the following topics: [Messages de rapport MAPI](mapi-report-messages.md), [Propri�t�s de Message de rapport requis](required-report-message-properties.md), [Propri�t�s de Message d'�tat facultatives](optional-report-message-properties.md), and [Envoi de rapports de remise de Message](sending-message-delivery-reports.md).
    
- D�finir le groupe de **PR_SENDER** du message de propri�t�s � l'identit� de l'utilisateur qui a ouvert une session. Ce groupe comprend : **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) et **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- D�finir les propri�t�s de message **PR_SENT_REPRESENTING**, dans la mesure du possible, soit l'identit� de l'utilisateur qui a ouvert une session ou une identit� de d�l�gu� valide. Les propri�t�s **PR_SENT_REPRESENTING** sont utilis�es pour impl�menter l'envoi de messages par un utilisateur au nom d'un autre utilisateur. Fournisseurs de transport qui ne prennent pas en charge ces propri�t�s doivent ignorer les messages sortants. 
    
- Définissez la propriété du message **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) pour indiquer si le client appelé [IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Définissez la propriété du message **PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) pour indiquer la date et l’heure auxquelles le fournisseur de banque de messages a marqué le message comme ayant été envoyé. 
    
Lorsqu'un message est envoy� � plusieurs destinataires avec plusieurs syst�mes de messagerie, chaque copie transmis aura une identit� diff�rente de l'exp�diteur. 
  
Le fournisseur de transport ou de banque de messages �troitement coupl�s et de transport est �galement responsable de la d�finition des informations de l'exp�diteur et de r�ponse. Informations de l'exp�diteur sont stock�es dans les propri�t�s **PR_ORIGINATOR** et r�pondre � des informations sont stock�es dans les propri�t�s de PR_REPLY. Le client peut d�finir ces propri�t�s ; Toutefois, le fournisseur de transport est autoris� � ignorer et remplacer les param�tres du client. 
  

