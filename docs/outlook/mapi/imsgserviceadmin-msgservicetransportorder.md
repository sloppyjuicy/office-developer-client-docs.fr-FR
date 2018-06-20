---
title: IMsgServiceAdminMsgServiceTransportOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.MsgServiceTransportOrder
api_type:
- COM
ms.assetid: c57ada0e-b9a1-496b-8548-75686d8cba4e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5b96a45bab4cd00d23604d0b0b25f3e772277395
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784241"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="d6ff5-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="d6ff5-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="d6ff5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d6ff5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d6ff5-105">Définit l’ordre dans les transports fournisseurs sont appelées pour remettre un message.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="d6ff5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6ff5-106">Parameters</span></span>

 <span data-ttu-id="d6ff5-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="d6ff5-107">_cUID_</span></span>
  
> <span data-ttu-id="d6ff5-108">[in] Le nombre des identificateurs uniques dans le paramètre _lpUIDList_ .</span><span class="sxs-lookup"><span data-stu-id="d6ff5-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="d6ff5-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="d6ff5-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="d6ff5-110">[in] Pointeur vers un tableau d’identificateurs uniques qui représentent des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="d6ff5-111">Le tableau contient un identificateur pour chaque fournisseur de transport configurée dans le profil actif.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="d6ff5-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d6ff5-112">_ulFlags_</span></span>
  
> <span data-ttu-id="d6ff5-113">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d6ff5-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d6ff5-114">Return value</span></span>

<span data-ttu-id="d6ff5-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="d6ff5-115">S_OK</span></span> 
  
> <span data-ttu-id="d6ff5-116">L’ordre de transport a été défini avec succès.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="d6ff5-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="d6ff5-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="d6ff5-118">La valeur dans le paramètre _cUID_ est différent du nombre de fournisseurs de transport réellement dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="d6ff5-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="d6ff5-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="d6ff5-120">Une ou plusieurs des structures [MAPIUID](mapiuid.md) passés dans le paramètre _lpUIDList_ ne font pas référence à un fournisseur de transport actuellement dans le profil.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d6ff5-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6ff5-121">Remarks</span></span>

<span data-ttu-id="d6ff5-122">La méthode **IMsgServiceAdmin::MsgServiceTransportOrder** définit l’ordre de remise des fournisseurs de transport dans un profil.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="d6ff5-123">Le paramètre _lpUIDList_ doit contenir une liste triée des identificateurs d’entrée-fournisseur de transport obtenu à partir de la propriété **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) du tableau renvoyé par la [IMsgServiceAdmin :: GetProviderTable](imsgserviceadmin-getprovidertable.md) méthode.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="d6ff5-124">Une application cliente doit transmettre la liste complète de _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="d6ff5-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="d6ff5-125">Les substitutions **SetTransportOrder** transportent préférences fournisseur telles que l’indicateur STATUS_XP_PREFER_LAST défini dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d6ff5-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d6ff5-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6ff5-126">See also</span></span>



[<span data-ttu-id="d6ff5-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="d6ff5-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="d6ff5-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d6ff5-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

