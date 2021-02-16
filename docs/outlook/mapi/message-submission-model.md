---
title: Modèle d’envoi de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421122"
---
# <a name="message-submission-model"></a>Modèle d’envoi de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L’envoi du message est effectué par une série d’appels dupooler MAPI au fournisseur de transport. Les appels sont séquencés comme suit :
  
1. Lepooler MAPI appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md), en passant une instance [IMessage : IMAPIProp,](imessageimapiprop.md) pour commencer le processus. 
    
2. Le fournisseur de transport place ensuite une valeur de référence (un identificateur défini par le transport utilisé dans les références futures à ce message) à l’emplacement référencé dans **SubmitMessage**.
    
3. Le fournisseur de transport accède aux données de message à l’aide de l’instance **IMessage** transmise. Pour chaque destinataire dans **l’IMessage** passé pour lequel il accepte la responsabilité, le fournisseur de transport définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), puis renvoie.
    
4. Le fournisseur de transport peut utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour indiquer s’il reconnaît les destinataires qui ne peuvent pas être remis ou pour créer un rapport de remise standard. **StatusRecips** est pratique pour les fournisseurs de transport qui ont déterminé que certains destinataires ne peuvent pas être remis ou qui ont reçu des informations de remise de leur système de messagerie sous-jacent que l’utilisateur ou l’application cliente peut trouver utiles. 
    
5. L’appel dupooler MAPI à [IXPLogon::EndMessage](ixplogon-endmessage.md) est la dernière responsabilité de remise du message dupooler MAPI au fournisseur de transport. 
    
6. Lepooler MAPI peut utiliser [IXPLogon::TransportNotify](ixplogon-transportnotify.md) pour annuler le traitement des messages pendant les appels **SubmitMessage** ou **EndMessage.** 
    

