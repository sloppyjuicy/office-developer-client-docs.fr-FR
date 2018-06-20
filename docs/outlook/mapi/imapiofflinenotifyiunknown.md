---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783878"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="cc64c-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cc64c-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="cc64c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cc64c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cc64c-105">Prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 l’envoi de rappels de notification à un client.</span><span class="sxs-lookup"><span data-stu-id="cc64c-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc64c-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="cc64c-106">Provided by:</span></span>  <br/> |<span data-ttu-id="cc64c-107">Client</span><span class="sxs-lookup"><span data-stu-id="cc64c-107">Client</span></span>  <br/> |
|<span data-ttu-id="cc64c-108">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="cc64c-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cc64c-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="cc64c-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cc64c-110">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="cc64c-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cc64c-111">Avertir</span><span class="sxs-lookup"><span data-stu-id="cc64c-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="cc64c-112">Envoie des notifications à un client sur les modifications de l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="cc64c-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cc64c-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc64c-113">Remarks</span></span>

<span data-ttu-id="cc64c-114">Le client doit implémenter cette interface et lui passer un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lorsque vous configurez des rappels à l’aide de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="cc64c-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="cc64c-115">Ensuite, Outlook 2010 ou Outlook 2013 sera en mesure d’utiliser cette interface pour envoyer les rappels de notification au client.</span><span class="sxs-lookup"><span data-stu-id="cc64c-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc64c-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc64c-116">See also</span></span>



[<span data-ttu-id="cc64c-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="cc64c-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="cc64c-118">À propos de l’API d’état en mode hors connexion</span><span class="sxs-lookup"><span data-stu-id="cc64c-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="cc64c-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="cc64c-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cc64c-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="cc64c-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

