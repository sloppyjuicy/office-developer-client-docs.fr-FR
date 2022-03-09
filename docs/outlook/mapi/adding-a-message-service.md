---
title: Ajouter un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
ms.openlocfilehash: e4732ed930b78e659c586ef560062d314821abf1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63379261"
---
# <a name="add-a-message-service"></a>Ajouter un service de message

**S’applique à** : Outlook 2013 | Outlook 2016
  
## <a name="to-add-a-new-message-service-to-a-profile-and-access-the-new-message-service"></a>Pour ajouter un nouveau service de message à un profil et accéder au nouveau service de message
  
[Appelez IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md). **CreateMsgServiceEx effectue** les tâches suivantes :
  
1. Copie toutes les informations pertinentes pour le service de message qui se trouve dans mapISVC. Fichier INF, création d’une section de profil pour chaque section fournisseur.

2. Appelle la fonction de point d’entrée du service de message, **MSGSERVICEENTRY**, avec le paramètre _ulContext_ paramétré sur MSG_SERVICE_CREATE.

3. Définit et récupère la propriété **PR_SERVICE_UID (**[PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message.

## <a name="to-access-any-newly-added-message-service"></a>Pour accéder à un service de message nouvellement ajouté
  
1. [Appelez IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table de service de message.

2. Appelez la méthode [IMAPITable::Advise](imapitable-advise.md) de la table de service de message pour vous inscrire aux notifications de table.

3. Lorsque MAPI envoie une notification TABLE_ROW_ADDED, recherchez l’identificateur d’entrée du service de message nouvellement ajouté dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) .
