---
title: Modèle de dépôt des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4bcd19f6-c225-43ac-8c27-c46388e9097a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 090a765fd6c758e5f146caa0e7f36276b052f69e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356874"
---
# <a name="message-submission-model"></a>Modèle de dépôt des messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
L'envoi de messages est effectué par une série d'appels depuis le spouleur MAPI vers le fournisseur de transport. Les appels sont séquencés comme suit:
  
1. Le spouleur MAPI appelle [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md), en transmettant une instance [IMessage: IMAPIProp](imessageimapiprop.md) , pour commencer le processus. 
    
2. Le fournisseur de transport place ensuite une valeur de référence, c'est-à-dire un identificateur défini par le transport utilisé dans les références futures à ce message, à l'emplacement référencé dans **SubmitMessage**.
    
3. Le fournisseur de transport accède aux données de message à l'aide de l'instance **IMessage** passée. Pour chaque destinataire dans l' **IMessage** passé pour lequel il accepte la responsabilité, le fournisseur de transport définit la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)), puis renvoie.
    
4. Le fournisseur de transport peut utiliser la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour indiquer s'il reconnaît tous les destinataires qui ne peuvent pas être remis à ou pour créer un rapport de remise standard. **StatusRecips** est pratique pour les fournisseurs de transport qui ont déterminé que certains des destinataires ne peuvent pas être remis à ou qui ont reçu des informations de remise de la part de leur système de messagerie sous-jacent, que l'utilisateur ou l'application cliente pourrait trouver utile. 
    
5. L'appel du spouleur MAPI vers [IXPLogon:: EndMessage](ixplogon-endmessage.md) est la responsabilité finale du message du spouleur MAPI vers le fournisseur de transport. 
    
6. Le spouleur MAPI peut utiliser [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) pour annuler le traitement des messages pendant les appels **SubmitMessage** ou **EndMessage** . 
    

