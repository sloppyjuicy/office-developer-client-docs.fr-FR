---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784757"
---
# <a name="mapiofflinecreateinfo"></a><span data-ttu-id="6e27a-103">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="6e27a-103">MAPIOFFLINE_CREATEINFO</span></span>

  
  
<span data-ttu-id="6e27a-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e27a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e27a-105">Cette structure est utilisée avec [HrCreateOfflineObj](hrcreateofflineobj.md).</span><span class="sxs-lookup"><span data-stu-id="6e27a-105">This structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="6e27a-106">Membres</span><span class="sxs-lookup"><span data-stu-id="6e27a-106">Members</span></span>

 <span data-ttu-id="6e27a-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="6e27a-107">**ulSize**</span></span>
  
> <span data-ttu-id="6e27a-108">La taille de structure.</span><span class="sxs-lookup"><span data-stu-id="6e27a-108">The size of structure.</span></span>
    
 <span data-ttu-id="6e27a-109">**ulCreateFlags**</span><span class="sxs-lookup"><span data-stu-id="6e27a-109">**ulCreateFlags**</span></span>
  
> <span data-ttu-id="6e27a-110">Il doit être 0.</span><span class="sxs-lookup"><span data-stu-id="6e27a-110">It must be 0.</span></span>
    
 <span data-ttu-id="6e27a-111">**pwszProfileName**</span><span class="sxs-lookup"><span data-stu-id="6e27a-111">**pwszProfileName**</span></span>
  
> <span data-ttu-id="6e27a-112">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="6e27a-112">The name of the profile.</span></span>
    
 <span data-ttu-id="6e27a-113">**ulCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6e27a-113">**ulCapabilities**</span></span>
  
> <span data-ttu-id="6e27a-114">Masque de bits des indicateurs de capacité suivants.</span><span class="sxs-lookup"><span data-stu-id="6e27a-114">A bit mask of the following capability flags.</span></span>
    
|||
|:-----|:-----|
|<span data-ttu-id="6e27a-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="6e27a-115">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>  <br/> |<span data-ttu-id="6e27a-116">L’objet en mode hors connexion est capable de passer en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6e27a-116">The offline object is capable of going offline.</span></span>  <br/> |
|<span data-ttu-id="6e27a-117">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="6e27a-117">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>  <br/> |<span data-ttu-id="6e27a-118">L’objet en mode hors connexion est capable de passer en ligne.</span><span class="sxs-lookup"><span data-stu-id="6e27a-118">The offline object is capable of going online.</span></span>  <br/> |
   
 <span data-ttu-id="6e27a-119">**pGUID**</span><span class="sxs-lookup"><span data-stu-id="6e27a-119">**pGUID**</span></span>
  
> <span data-ttu-id="6e27a-120">Pointeur vers un GUID qui sert à identifier de manière unique ce type d’objet en mode hors connexion à partir d’autres objets en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6e27a-120">Pointer to a GUID that is used to uniquely identify this type of offline object from other offline objects.</span></span> <span data-ttu-id="6e27a-121">GUID_GlobalState fait référence à l’objet en mode hors connexion global qui les objets peuvent utiliser en tant qu’objet parent.</span><span class="sxs-lookup"><span data-stu-id="6e27a-121">GUID_GlobalState refers to the global offline object that objects can use as a parent object.</span></span>
    
 <span data-ttu-id="6e27a-122">**pInstance**</span><span class="sxs-lookup"><span data-stu-id="6e27a-122">**pInstance**</span></span>
  
> <span data-ttu-id="6e27a-123">Pointeur vers un GUID qui identifie de manière unique cet objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6e27a-123">Pointer to GUID that uniquely identifies this offline object.</span></span> <span data-ttu-id="6e27a-124">Il est utilisé pour clarifier cette objets en mode hors connexion à partir d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="6e27a-124">It is used to disambiguate this offline objects from other objects.</span></span>
    
 <span data-ttu-id="6e27a-125">**pParent**</span><span class="sxs-lookup"><span data-stu-id="6e27a-125">**pParent**</span></span>
  
> <span data-ttu-id="6e27a-126">Pointeur vers l’objet en mode hors connexion qui est le parent de cet objet en mode hors connexion et dont les modifications hérite de cet objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6e27a-126">Pointer to offline object that is the parent of this offline object and whose changes this offline object will inherit.</span></span>
    
 <span data-ttu-id="6e27a-127">**pMAPISupport**</span><span class="sxs-lookup"><span data-stu-id="6e27a-127">**pMAPISupport**</span></span>
  
>  <span data-ttu-id="6e27a-128">Identifie l’objet de prise en charge MAPI que qui utilisera cet objet en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="6e27a-128">Identifies the MAPI support object that that will use this offline object.</span></span> <span data-ttu-id="6e27a-129">Par exemple, si cet objet en mode hors connexion est utilisé pour suivre un magasin hors connexion et l’état en ligne, puis il est les magasins de prendre en charge objet.</span><span class="sxs-lookup"><span data-stu-id="6e27a-129">For example, if this offline object is used to keep track of a store's offline and online state, then this is the stores support object.</span></span> <span data-ttu-id="6e27a-130">Toutefois, s’il s’agit d’un objet en mode hors connexion pour un objet avec aucun objet de prise en charge qu’il peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="6e27a-130">However, if this is an offline object for an object with no support object then it can be NULL.</span></span> 
    
 <span data-ttu-id="6e27a-131">**pAggregateInfo**</span><span class="sxs-lookup"><span data-stu-id="6e27a-131">**pAggregateInfo**</span></span>
  
> <span data-ttu-id="6e27a-132">Pointeur vers une structure MAPIOFFLINE_AGGREGATEINFO.</span><span class="sxs-lookup"><span data-stu-id="6e27a-132">A pointer to a MAPIOFFLINE_AGGREGATEINFO structure.</span></span> <span data-ttu-id="6e27a-133">Pour plus d’informations, voir [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span><span class="sxs-lookup"><span data-stu-id="6e27a-133">For more information, see [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).</span></span>
    
 <span data-ttu-id="6e27a-134">**pConnectInfo**</span><span class="sxs-lookup"><span data-stu-id="6e27a-134">**pConnectInfo**</span></span>
  
> <span data-ttu-id="6e27a-135">Doit être null.</span><span class="sxs-lookup"><span data-stu-id="6e27a-135">Must be null.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6e27a-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e27a-136">See also</span></span>



[<span data-ttu-id="6e27a-137">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="6e27a-137">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="6e27a-138">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="6e27a-138">MAPIOFFLINE_AGGREGATEINFO</span></span>](mapioffline_aggregateinfo.md)

