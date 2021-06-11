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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439876"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="1d3a4-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d3a4-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="1d3a4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d3a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d3a4-105">Prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 l’envoi de rappels de notification à un client.</span><span class="sxs-lookup"><span data-stu-id="1d3a4-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1d3a4-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="1d3a4-106">Provided by:</span></span>  <br/> |<span data-ttu-id="1d3a4-107">Client</span><span class="sxs-lookup"><span data-stu-id="1d3a4-107">Client</span></span>  <br/> |
|<span data-ttu-id="1d3a4-108">Identificateur d’interface :</span><span class="sxs-lookup"><span data-stu-id="1d3a4-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1d3a4-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="1d3a4-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1d3a4-110">Ordre des vtables</span><span class="sxs-lookup"><span data-stu-id="1d3a4-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1d3a4-111">Notification</span><span class="sxs-lookup"><span data-stu-id="1d3a4-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="1d3a4-112">Envoie des notifications à un client concernant les modifications apportées à l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="1d3a4-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d3a4-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d3a4-113">Remarks</span></span>

<span data-ttu-id="1d3a4-114">Le client doit implémenter cette interface et lui transmettre un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lors de la configuration des rappels à l’aide **[d’IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1d3a4-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="1d3a4-115">Par la suite, Outlook 2010 ou Outlook 2013 pourra utiliser cette interface pour envoyer des rappels de notification au client.</span><span class="sxs-lookup"><span data-stu-id="1d3a4-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1d3a4-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d3a4-116">See also</span></span>



[<span data-ttu-id="1d3a4-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="1d3a4-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="1d3a4-118">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="1d3a4-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="1d3a4-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="1d3a4-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="1d3a4-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="1d3a4-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

