---
title: Ajout d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328183"
---
# <a name="adding-a-message-service"></a>Ajout d'un service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour ajouter un nouveau service de messagerie à un profil et accéder au nouveau service de messagerie**
  
Appelez [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx** effectue les tâches suivantes: 
  
1. Copie toutes les informations pertinentes pour le service de messagerie qui se trouve dans le MAPISVC. Fichier INF, création d'une section de profil pour chaque section de fournisseur.
    
2. Appelle la fonction de point d'entrée du service de messagerie, **MSGSERVICEENTRY**, avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_CREATE. 
    
3. Définit et récupère la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de messagerie.
    
 **Pour accéder à tout service de message récemment ajouté**
  
1. Appelez [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table des services de messagerie. 
    
2. Appelez la méthode [IMAPITable:: Advise](imapitable-advise.md) pour enregistrer les notifications de table. 
    
3. Lorsque MAPI envoie une notification TABLE_ROW_ADDED, localisez l'identificateur d'entrée du service de messagerie nouvellement ajouté dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) . 
    

