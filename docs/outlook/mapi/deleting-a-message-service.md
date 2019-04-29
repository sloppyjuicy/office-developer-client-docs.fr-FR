---
title: Suppression d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428122"
---
# <a name="deleting-a-message-service"></a>Suppression d'un service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour supprimer un service de messagerie d'un profil**
  
1. Appelez **IMAPISession:: GetMsgServiceTable** pour accéder à la table des services de messagerie. 
    
2. Localisez la ligne du service de messagerie et transmettez sa colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) dans le paramètre _Lpuid_ à [IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md). 
    
 **DeleteMsgService** appelle la fonction de point d'entrée du service de messagerie avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_DELETE. Les services de messagerie effectuent toutes les tâches de nettoyage pour le moment précédant leur suppression du profil. 
  

