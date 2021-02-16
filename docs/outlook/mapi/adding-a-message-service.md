---
title: Ajout d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407234"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="15d06-103">Ajout d’un service de message</span><span class="sxs-lookup"><span data-stu-id="15d06-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="15d06-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15d06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="15d06-105">**Pour ajouter un nouveau service de message à un profil et accéder au nouveau service de message**</span><span class="sxs-lookup"><span data-stu-id="15d06-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="15d06-106">Appelez [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="15d06-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="15d06-107">**CreateMsgServiceEx effectue** les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="15d06-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="15d06-108">Copie toutes les informations pertinentes pour le service de message qui se trouve dans mapISVC. Fichier INF, création d’une section de profil pour chaque section fournisseur.</span><span class="sxs-lookup"><span data-stu-id="15d06-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="15d06-109">Appelle la fonction de point d’entrée du service de message, **MSGSERVICEENTRY,** avec le paramètre  _ulContext_ paramétré sur MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="15d06-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="15d06-110">Définit et récupère la propriété PR_SERVICE_UID **(** [PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de message.</span><span class="sxs-lookup"><span data-stu-id="15d06-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="15d06-111">**Pour accéder à un service de message nouvellement ajouté**</span><span class="sxs-lookup"><span data-stu-id="15d06-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="15d06-112">Appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table de service de message.</span><span class="sxs-lookup"><span data-stu-id="15d06-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="15d06-113">Appelez la méthode [IMAPITable::Advise](imapitable-advise.md) de la table de service de message pour vous inscrire aux notifications de table.</span><span class="sxs-lookup"><span data-stu-id="15d06-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="15d06-114">Lorsque MAPI envoie une notification TABLE_ROW_ADDED, recherchez l’identificateur d’entrée du service de message nouvellement ajouté dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) de message.</span><span class="sxs-lookup"><span data-stu-id="15d06-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

