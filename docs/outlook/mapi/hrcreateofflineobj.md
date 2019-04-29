---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0a34c441a473154a43a107b4236ccc259d327dba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414388"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="b82ce-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b82ce-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="b82ce-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b82ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b82ce-105">Crée un objet MAPI hors connexion qui est utilisé par le fournisseur et le magasin afin d'informer MAPI lorsque l'objet passe en ligne et hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b82ce-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b82ce-106">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="b82ce-106">Exported by:</span></span>  <br/> |<span data-ttu-id="b82ce-107">Msmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="b82ce-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="b82ce-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b82ce-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b82ce-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="b82ce-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="b82ce-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b82ce-110">Called by:</span></span>  <br/> |<span data-ttu-id="b82ce-111">Client</span><span class="sxs-lookup"><span data-stu-id="b82ce-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="b82ce-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b82ce-112">Parameters</span></span>

<span data-ttu-id="b82ce-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b82ce-113">_ulFlags_</span></span>
  
> <span data-ttu-id="b82ce-114">dans Il doit être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="b82ce-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="b82ce-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="b82ce-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="b82ce-116">dans Pointeur vers une structure **MAPIOFFLINE_CREATEINFO** qui contient les informations nécessaires à la création de l'objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="b82ce-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="b82ce-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="b82ce-117">_ppOffline_</span></span>
  
> <span data-ttu-id="b82ce-118">remarquer Pointeur vers l'interface **IMAPIOfflineMgr** .</span><span class="sxs-lookup"><span data-stu-id="b82ce-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b82ce-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b82ce-119">Return value</span></span>

<span data-ttu-id="b82ce-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b82ce-120">None.</span></span>
  
<span data-ttu-id="b82ce-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="b82ce-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="b82ce-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="b82ce-122">Example</span></span>

```cpp
// create/get global offline object to use as parent.
 ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = &GUID_GlobalState;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = NULL;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
// Create an offline object for the provider with global as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = pGuid;
  OfflineCreateInfo.pInstance = pInstance;
  OfflineCreateInfo.pParent = pGlobalOfflineMgr;
  OfflineCreateInfo.pMAPISupport = NULL;
  OfflineCreateInfo.pAggregateInfo = NULL;
  OfflineCreateInfo.pConnectInfo = NULL;
  // create store offline object which aggregates with the store object and has provider offline object as parent.
  ZeroMemory(&OfflineCreateInfo, sizeof(OfflineCreateInfo));
  OfflineCreateInfo.ulSize = sizeof(OfflineCreateInfo);
  OfflineCreateInfo.ulCreateFlags = 0;
  OfflineCreateInfo.pwszProfileName = pszProfileName;
  OfflineCreateInfo.ulCapabilities = ulCapabilities;
  OfflineCreateInfo.pGUID = NULL;
  OfflineCreateInfo.pInstance = NULL;
  OfflineCreateInfo.pParent = m_pProviderOfflineMgr;
  OfflineCreateInfo.pMAPISupport = pMAPISup;
  OfflineCreateInfo.pAggregateInfo = &AggregateInfo;
  OfflineCreateInfo.pConnectInfo = NULL;
  ZeroMemory(&AggregateInfo, sizeof(AggregateInfo));
  AggregateInfo.ulSize = sizeof(AggregateInfo);
  AggregateInfo.pOuterObj = (IMsgStore *)this;
  AggregateInfo.pRefTrackRoot = NULL;

```

## <a name="see-also"></a><span data-ttu-id="b82ce-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b82ce-123">See also</span></span>

- [<span data-ttu-id="b82ce-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="b82ce-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="b82ce-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="b82ce-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

