---
title: Suppression d’un Service de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783146"
---
# <a name="deleting-a-message-service"></a>Suppression d’un Service de Message

  
  
**S’applique à**: Outlook 
  
 **Pour supprimer un service de message à partir d’un profil**
  
1. Appelez **IMAPISession::GetMsgServiceTable** pour accéder à la table de service de message. 
    
2. Localisez la ligne pour le service de message et le secret de sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _lpuid_ à [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d’entrée du service de message avec le paramètre _ulContext_ défini sur MSG_SERVICE_DELETE. Services de messagerie effectuer l’une des tâches de nettoyage pour le moment où ils sont supprimés du profil. 
  

