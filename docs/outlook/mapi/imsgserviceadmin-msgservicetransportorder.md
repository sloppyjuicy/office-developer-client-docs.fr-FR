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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 3d532e0eb46daa412711344421936a58da309b7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420093"
---
# <a name="imsgserviceadminmsgservicetransportorder"></a><span data-ttu-id="8db92-103">IMsgServiceAdmin::MsgServiceTransportOrder</span><span class="sxs-lookup"><span data-stu-id="8db92-103">IMsgServiceAdmin::MsgServiceTransportOrder</span></span>

  
  
<span data-ttu-id="8db92-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8db92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8db92-105">Définit l’ordre dans lequel les fournisseurs de transport sont appelés pour remettre un message.</span><span class="sxs-lookup"><span data-stu-id="8db92-105">Sets the order in which transport providers are called to deliver a message.</span></span>
  
```cpp
HRESULT MsgServiceTransportOrder(
  ULONG cUID,
  LPMAPIUID lpUIDList,
  ULONG ulFlags    
);
```

## <a name="parameters"></a><span data-ttu-id="8db92-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8db92-106">Parameters</span></span>

 <span data-ttu-id="8db92-107">_cUID_</span><span class="sxs-lookup"><span data-stu-id="8db92-107">_cUID_</span></span>
  
> <span data-ttu-id="8db92-108">[in] Nombre d’identificateurs uniques dans le _paramètre lpUIDList._</span><span class="sxs-lookup"><span data-stu-id="8db92-108">[in] The count of unique identifiers in the  _lpUIDList_ parameter.</span></span> 
    
 <span data-ttu-id="8db92-109">_lpUIDList_</span><span class="sxs-lookup"><span data-stu-id="8db92-109">_lpUIDList_</span></span>
  
> <span data-ttu-id="8db92-110">[in] Pointeur vers un tableau d’identificateurs uniques qui représentent des fournisseurs de transport.</span><span class="sxs-lookup"><span data-stu-id="8db92-110">[in] A pointer to an array of unique identifiers that represent transport providers.</span></span> <span data-ttu-id="8db92-111">Le tableau contient un identificateur pour chaque fournisseur de transport configuré dans le profil actuel.</span><span class="sxs-lookup"><span data-stu-id="8db92-111">The array contains one identifier for each transport provider configured in the current profile.</span></span>
    
 <span data-ttu-id="8db92-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8db92-112">_ulFlags_</span></span>
  
> <span data-ttu-id="8db92-113">[in] R�serv� ; doit �tre �gal � z�ro.</span><span class="sxs-lookup"><span data-stu-id="8db92-113">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8db92-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8db92-114">Return value</span></span>

<span data-ttu-id="8db92-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8db92-115">S_OK</span></span> 
  
> <span data-ttu-id="8db92-116">L’ordre de transport a été correctement établi.</span><span class="sxs-lookup"><span data-stu-id="8db92-116">The transport order was set successfully.</span></span>
    
<span data-ttu-id="8db92-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="8db92-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="8db92-118">La valeur du  _paramètre cUID_ diffère du nombre de fournisseurs de transport dans le profil.</span><span class="sxs-lookup"><span data-stu-id="8db92-118">The value in the  _cUID_ parameter differs from the number of transport providers actually in the profile.</span></span> 
    
<span data-ttu-id="8db92-119">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="8db92-119">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="8db92-120">Une ou plusieurs structures [MAPIUID](mapiuid.md) transmises dans le paramètre  _lpUIDList_ ne font pas référence à un fournisseur de transport actuellement dans le profil.</span><span class="sxs-lookup"><span data-stu-id="8db92-120">One or more of the [MAPIUID](mapiuid.md) structures passed in the  _lpUIDList_ parameter do not refer to a transport provider currently in the profile.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="8db92-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8db92-121">Remarks</span></span>

<span data-ttu-id="8db92-122">La **méthode IMsgServiceAdmin::MsgServiceTransportOrder** définit l’ordre de remise des fournisseurs de transport dans un profil.</span><span class="sxs-lookup"><span data-stu-id="8db92-122">The **IMsgServiceAdmin::MsgServiceTransportOrder** method sets the delivery order of transport providers in a profile.</span></span> <span data-ttu-id="8db92-123">Le paramètre _lpUIDList_ doit contenir une liste triée d’identificateurs d’entrée de fournisseur de transport obtenus à partir de la propriété **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) de la table renvoyée par la méthode [IMsgServiceAdmin::GetProviderTable.](imsgserviceadmin-getprovidertable.md)</span><span class="sxs-lookup"><span data-stu-id="8db92-123">The  _lpUIDList_ parameter must contain a sorted list of transport-provider entry identifiers obtained from the **PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md)) property of the table returned from the [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) method.</span></span> <span data-ttu-id="8db92-124">Une application cliente doit transmettre la liste complète dans  _lpUIDList_.</span><span class="sxs-lookup"><span data-stu-id="8db92-124">A client application must pass the complete list in  _lpUIDList_.</span></span>
  
 <span data-ttu-id="8db92-125">**SetTransportOrder** remplace les préférences de fournisseur de transport telles que l’indicateur STATUS_XP_PREFER_LAST définie dans la propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="8db92-125">**SetTransportOrder** overrides transport provider preferences such as the STATUS_XP_PREFER_LAST flag set in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8db92-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8db92-126">See also</span></span>



[<span data-ttu-id="8db92-127">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="8db92-127">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="8db92-128">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8db92-128">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)

