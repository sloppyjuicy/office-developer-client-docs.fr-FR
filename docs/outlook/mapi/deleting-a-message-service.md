---
title: Suppression d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
ms.openlocfilehash: c4ec6c0177347b42e622a22c5c59f195507a9993
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63370014"
---
# <a name="deleting-a-message-service"></a>Suppression d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un service de message d’un profil**
  
1. **Appelez IMAPISession::GetMsgServiceTable** pour accéder à la table de service de message. 
    
2. Recherchez la ligne du service de message et passez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _lpuid_ à [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ MSG_SERVICE_DELETE. Les services de messages effectuent actuellement des tâches de nettoyage avant leur suppression du profil. 
  

