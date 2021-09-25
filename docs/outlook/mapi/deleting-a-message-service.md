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
ms.openlocfilehash: 2ad38e1d5fb483956a387e3b6e001479d7153545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605047"
---
# <a name="deleting-a-message-service"></a>Suppression d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un service de message d’un profil**
  
1. Appelez **IMAPISession::GetMsgServiceTable** pour accéder à la table du service de message. 
    
2. Recherchez la ligne du service de message et passez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre  _lpuid_ à [IMsgServiceAdmin::D eleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre  _ulContext_ MSG_SERVICE_DELETE. Les services de messages effectuent actuellement des tâches de nettoyage avant qu’elles ne soient supprimées du profil. 
  

