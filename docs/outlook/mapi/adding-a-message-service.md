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
# <a name="adding-a-message-service"></a><span data-ttu-id="ef273-103">Ajout d’un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="ef273-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="ef273-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef273-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ef273-105">**Pour ajouter un nouveau service de message à un profil et accéder au nouveau service de message**</span><span class="sxs-lookup"><span data-stu-id="ef273-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="ef273-106">Appelez [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="ef273-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="ef273-107">**CreateMsgServiceEx** effectue les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef273-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="ef273-108">Copie toutes les informations pertinentes pour le service de message qui se trouve dans le fichier MAPISVC.inf. Fichier INF, création d’une section de profil pour chaque section fournisseur.</span><span class="sxs-lookup"><span data-stu-id="ef273-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="ef273-109">Appelle la fonction de point d’entrée du message service **MSGSERVICEENTRY**, avec le paramètre _ulContext_ défini sur MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="ef273-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="ef273-110">Définit et extrait les propriétés de **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message.</span><span class="sxs-lookup"><span data-stu-id="ef273-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="ef273-111">**Pour accéder à n’importe quel service de message nouvellement ajouté**</span><span class="sxs-lookup"><span data-stu-id="ef273-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="ef273-112">Appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="ef273-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="ef273-113">Appelez la méthode de [IMAPITable::Advise](imapitable-advise.md) de la table de service de message pour s’inscrire pour les notifications de table.</span><span class="sxs-lookup"><span data-stu-id="ef273-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="ef273-114">Lorsque MAPI envoie une notification TABLE_ROW_ADDED, recherchez l’identificateur d’entrée du service de message nouvellement ajoutés dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="ef273-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

