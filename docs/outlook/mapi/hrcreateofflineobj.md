---
title: HrCreateOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 04d57c1d-ce91-42ce-9f0f-00563092f6f4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 465121d37489b6810ca141d798b6c96d3f14980e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783532"
---
# <a name="hrcreateofflineobj"></a><span data-ttu-id="3bbaf-103">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3bbaf-103">HrCreateOfflineObj</span></span>

<span data-ttu-id="3bbaf-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3bbaf-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="3bbaf-105">Crée un objet en mode hors connexion MAPI qui est utilisé par le fournisseur et le magasin afin d’informer MAPI lorsque l’objet passe en ligne et hors connexion,</span><span class="sxs-lookup"><span data-stu-id="3bbaf-105">Creates a MAPI offline object that is used by the provider and store in order to notify MAPI when the object goes online and offline,</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bbaf-106">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="3bbaf-106">Exported by:</span></span>  <br/> |<span data-ttu-id="3bbaf-107">Msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="3bbaf-107">Msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="3bbaf-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="3bbaf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3bbaf-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="3bbaf-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="3bbaf-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="3bbaf-110">Called by:</span></span>  <br/> |<span data-ttu-id="3bbaf-111">Client</span><span class="sxs-lookup"><span data-stu-id="3bbaf-111">Client</span></span>  <br/> |
   
```cpp
STDAPI HrCreateOfflineObj(
ULONG ulFlags,
MAPIOFFLINE_CREATEINFO* pCreateInfo,
IMAPIOfflineMgr** ppOffline
);
```

## <a name="parameters"></a><span data-ttu-id="3bbaf-112">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3bbaf-112">Parameters</span></span>

<span data-ttu-id="3bbaf-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3bbaf-113">_ulFlags_</span></span>
  
> <span data-ttu-id="3bbaf-114">[in] Il doit être 0.</span><span class="sxs-lookup"><span data-stu-id="3bbaf-114">[in] It must be 0.</span></span>
    
<span data-ttu-id="3bbaf-115">_pCreateInfo_</span><span class="sxs-lookup"><span data-stu-id="3bbaf-115">_pCreateInfo_</span></span>
  
> <span data-ttu-id="3bbaf-116">[in] Pointeur vers une structure **MAPIOFFLINE_CREATEINFO** qui contient les informations nécessaires pour créer l’objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="3bbaf-116">[in] A pointer to a **MAPIOFFLINE_CREATEINFO** structure that contains the information needed to create the offline object.</span></span> 
    
<span data-ttu-id="3bbaf-117">_ppOffline_</span><span class="sxs-lookup"><span data-stu-id="3bbaf-117">_ppOffline_</span></span>
  
> <span data-ttu-id="3bbaf-118">[out] Pointeur vers l’interface **IMAPIOfflineMgr** .</span><span class="sxs-lookup"><span data-stu-id="3bbaf-118">[out] A pointer to the **IMAPIOfflineMgr** interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3bbaf-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3bbaf-119">Return value</span></span>

<span data-ttu-id="3bbaf-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="3bbaf-120">None.</span></span>
  
<span data-ttu-id="3bbaf-121">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3bbaf-121">HrOpenOfflineObj</span></span>
  
## <a name="example"></a><span data-ttu-id="3bbaf-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="3bbaf-122">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3bbaf-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3bbaf-123">See also</span></span>

- [<span data-ttu-id="3bbaf-124">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="3bbaf-124">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)
- [<span data-ttu-id="3bbaf-125">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="3bbaf-125">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

