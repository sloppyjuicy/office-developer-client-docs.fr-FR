---
title: Suppression d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 20bd8bf8222a202b075a600203fe7b1515356382
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462994"
---
# <a name="deleting-a-message-service"></a>Suppression d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un service de message d’un profil**
  
1. **Appelez IMAPISession::GetMsgServiceTable** pour accéder à la table de service de message. 
    
2. Recherchez la ligne du service de message et passez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _lpuid_ à [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ MSG_SERVICE_DELETE. Les services de messages effectuent actuellement des tâches de nettoyage avant leur suppression du profil. 
  

