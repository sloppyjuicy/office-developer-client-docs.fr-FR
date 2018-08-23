---
title: Ajout d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590693"
---
# <a name="adding-a-message-service"></a>Ajout d’un service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour ajouter un nouveau service de message à un profil et accéder au nouveau service de message**
  
Appelez [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** effectue les tâches suivantes : 
  
1. Copie toutes les informations pertinentes pour le service de message qui se trouve dans le fichier MAPISVC.inf. Fichier INF, création d’une section de profil pour chaque section fournisseur.
    
2. Appelle la fonction de point d’entrée du message service **MSGSERVICEENTRY**, avec le paramètre _ulContext_ défini sur MSG_SERVICE_CREATE. 
    
3. Définit et extrait les propriétés de **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message.
    
 **Pour accéder à n’importe quel service de message nouvellement ajouté**
  
1. Appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table de service de message. 
    
2. Appelez la méthode de [IMAPITable::Advise](imapitable-advise.md) de la table de service de message pour s’inscrire pour les notifications de table. 
    
3. Lorsque MAPI envoie une notification TABLE_ROW_ADDED, recherchez l’identificateur d’entrée du service de message nouvellement ajoutés dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) . 
    

