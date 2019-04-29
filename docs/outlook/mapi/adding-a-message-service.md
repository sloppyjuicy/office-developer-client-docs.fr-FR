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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407234"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="73a46-103">Ajout d'un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="73a46-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="73a46-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="73a46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="73a46-105">**Pour ajouter un nouveau service de messagerie à un profil et accéder au nouveau service de messagerie**</span><span class="sxs-lookup"><span data-stu-id="73a46-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="73a46-106">Appelez [IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="73a46-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="73a46-107">**CreateMsgServiceEx** effectue les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="73a46-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="73a46-108">Copie toutes les informations pertinentes pour le service de messagerie qui se trouve dans le MAPISVC. Fichier INF, création d'une section de profil pour chaque section de fournisseur.</span><span class="sxs-lookup"><span data-stu-id="73a46-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="73a46-109">Appelle la fonction de point d'entrée du service de messagerie, **MSGSERVICEENTRY**, avec le paramètre _ULCONTEXT_ défini sur MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="73a46-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="73a46-110">Définit et récupère la propriété **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) du service de messagerie.</span><span class="sxs-lookup"><span data-stu-id="73a46-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="73a46-111">**Pour accéder à tout service de message récemment ajouté**</span><span class="sxs-lookup"><span data-stu-id="73a46-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="73a46-112">Appelez [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour récupérer la table des services de messagerie.</span><span class="sxs-lookup"><span data-stu-id="73a46-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="73a46-113">Appelez la méthode [IMAPITable:: Advise](imapitable-advise.md) pour enregistrer les notifications de table.</span><span class="sxs-lookup"><span data-stu-id="73a46-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="73a46-114">Lorsque MAPI envoie une notification TABLE_ROW_ADDED, localisez l'identificateur d'entrée du service de messagerie nouvellement ajouté dans la structure [SRow](srow.md) incluse dans la structure [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="73a46-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

