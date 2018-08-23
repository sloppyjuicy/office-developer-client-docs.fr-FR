---
title: Suppression d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583567"
---
# <a name="deleting-a-message-service"></a>Suppression d’un service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un service de message à partir d’un profil**
  
1. Appelez **IMAPISession::GetMsgServiceTable** pour accéder à la table de service de message. 
    
2. Localisez la ligne pour le service de message et le secret de sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _lpuid_ à [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE. Services de messagerie effectuer l’une des tâches de nettoyage pour le moment où ils sont supprimés du profil. 
  

