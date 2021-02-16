---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429564"
---
# <a name="mapioffline_createinfo"></a><span data-ttu-id="736f5-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="736f5-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="736f5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="736f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="736f5-105">Cette structure est utilisée [avec HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="736f5-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a><span data-ttu-id="736f5-106">Members</span><span class="sxs-lookup"><span data-stu-id="736f5-106">Members</span></span>

 <span data-ttu-id="736f5-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="736f5-107">**ulSize**</span></span>
  
> <span data-ttu-id="736f5-108">Taille de la structure.</span><span class="sxs-lookup"><span data-stu-id="736f5-108">The size of structure.</span></span>
    
 <span data-ttu-id="736f5-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="736f5-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="736f5-110">Elle doit être 0.</span><span class="sxs-lookup"><span data-stu-id="736f5-110">It must be 0.</span></span>
    
 <span data-ttu-id="736f5-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="736f5-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="736f5-112">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="736f5-112">The name of the profile.</span></span>
    
 <span data-ttu-id="736f5-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="736f5-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="736f5-114">Masque de bits des indicateurs de fonctionnalité suivants.</span><span class="sxs-lookup"><span data-stu-id="736f5-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="736f5-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="736f5-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="736f5-116">L’objet hors connexion est capable de passer hors connexion.</span><span class="sxs-lookup"><span data-stu-id="736f5-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="736f5-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="736f5-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="736f5-118">L’objet hors connexion est capable de passer en ligne.</span><span class="sxs-lookup"><span data-stu-id="736f5-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="736f5-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="736f5-119">**pGUID**</span></span>
  
> <span data-ttu-id="736f5-120">Pointeur vers un GUID utilisé pour identifier de manière unique ce type d’objet hors connexion à partir d’autres objets hors connexion.</span><span class="sxs-lookup"><span data-stu-id="736f5-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="736f5-121">GUID_GlobalState fait référence à l’objet hors connexion global que les objets peuvent utiliser comme objet parent.</span><span class="sxs-lookup"><span data-stu-id="736f5-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="736f5-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="736f5-122">**pInstance**</span></span>
  
> <span data-ttu-id="736f5-123">Pointeur vers le GUID qui identifie de manière unique cet objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="736f5-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="736f5-124">Il est utilisé pour déconnecter ces objets hors connexion des autres objets.</span><span class="sxs-lookup"><span data-stu-id="736f5-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="736f5-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="736f5-125">**pParent**</span></span>
  
> <span data-ttu-id="736f5-126">Pointeur vers l’objet hors connexion qui est le parent de cet objet hors connexion et dont cet objet hors connexion héritera des modifications.</span><span class="sxs-lookup"><span data-stu-id="736f5-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="736f5-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="736f5-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="736f5-128">Identifie l’objet de prise en charge MAPI qui utilisera cet objet hors connexion.</span><span class="sxs-lookup"><span data-stu-id="736f5-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="736f5-129">Par exemple, si cet objet hors connexion est utilisé pour suivre l’état hors connexion et en ligne d’un magasin, il s’agit de l’objet de prise en charge des magasins.</span><span class="sxs-lookup"><span data-stu-id="736f5-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="736f5-130">Toutefois, s’il s’agit d’un objet hors connexion pour un objet sans objet de prise en charge, il peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="736f5-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="736f5-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="736f5-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="736f5-132">Pointeur vers une structure MAPIOFFLINE_AGGREGATEINFO de base.</span><span class="sxs-lookup"><span data-stu-id="736f5-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="736f5-133">Pour plus d’informations, [voir MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="736f5-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="736f5-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="736f5-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="736f5-135">Doit être null.</span><span class="sxs-lookup"><span data-stu-id="736f5-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="736f5-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="736f5-136">See also</span></span>



[<span data-ttu-id="736f5-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="736f5-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="736f5-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="736f5-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

