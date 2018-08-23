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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568146"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="ccd30-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ccd30-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="ccd30-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ccd30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ccd30-105">Prend en charge Microsoft Outlook 2010 et Microsoft Outlook 2013 l’envoi de rappels de notification à un client.</span><span class="sxs-lookup"><span data-stu-id="ccd30-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ccd30-106">Fourni par :</span><span class="sxs-lookup"><span data-stu-id="ccd30-106">Provided by:</span></span>  <br/> |<span data-ttu-id="ccd30-107">Client</span><span class="sxs-lookup"><span data-stu-id="ccd30-107">Client</span></span>  <br/> |
|<span data-ttu-id="ccd30-108">Identificateur de l’interface :</span><span class="sxs-lookup"><span data-stu-id="ccd30-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ccd30-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="ccd30-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ccd30-110">Ordre vtable</span><span class="sxs-lookup"><span data-stu-id="ccd30-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ccd30-111">Avertir</span><span class="sxs-lookup"><span data-stu-id="ccd30-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="ccd30-112">Envoie des notifications à un client sur les modifications de l’état de connexion.</span><span class="sxs-lookup"><span data-stu-id="ccd30-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ccd30-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ccd30-113">Remarks</span></span>

<span data-ttu-id="ccd30-114">Le client doit implémenter cette interface et lui passer un pointeur en tant que membre dans **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** lorsque vous configurez des rappels à l’aide de **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ccd30-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ccd30-115">Ensuite, Outlook 2010 ou Outlook 2013 sera en mesure d’utiliser cette interface pour envoyer les rappels de notification au client.</span><span class="sxs-lookup"><span data-stu-id="ccd30-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ccd30-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ccd30-116">See also</span></span>



[<span data-ttu-id="ccd30-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="ccd30-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="ccd30-118">À propos de l’API d’état hors connexion</span><span class="sxs-lookup"><span data-stu-id="ccd30-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="ccd30-119">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ccd30-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ccd30-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="ccd30-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

