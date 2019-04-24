---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360710"
---
# <a name="screlocnotifications"></a><span data-ttu-id="caa52-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="caa52-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="caa52-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="caa52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="caa52-105">Ajuste un pointeur dans un tableau de notification d'événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="caa52-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="caa52-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="caa52-106">Header file:</span></span>  <br/> |<span data-ttu-id="caa52-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="caa52-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="caa52-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="caa52-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="caa52-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="caa52-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="caa52-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="caa52-110">Called by:</span></span>  <br/> |<span data-ttu-id="caa52-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="caa52-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="caa52-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="caa52-112">Parameters</span></span>

 <span data-ttu-id="caa52-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="caa52-113">_cntf_</span></span>
  
> <span data-ttu-id="caa52-114">dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="caa52-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="caa52-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="caa52-115">_rgntf_</span></span>
  
> <span data-ttu-id="caa52-116">dans Pointeur vers le tableau de structures de **notification** définissant des notifications d'événement dans lesquelles un pointeur doit être ajusté.</span><span class="sxs-lookup"><span data-stu-id="caa52-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="caa52-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="caa52-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="caa52-118">dans Pointeur vers l'adresse de base d'origine du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="caa52-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="caa52-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="caa52-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="caa52-120">dans Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="caa52-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="caa52-121">_circuits_</span><span class="sxs-lookup"><span data-stu-id="caa52-121">_pcb_</span></span>
  
> <span data-ttu-id="caa52-122">remarquer Pointeur vers la taille, en octets, du tableau indiqué par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="caa52-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="caa52-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="caa52-123">Return value</span></span>

<span data-ttu-id="caa52-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="caa52-124">S_OK</span></span>
  
> <span data-ttu-id="caa52-125">Un pointeur a été ajusté avec succès.</span><span class="sxs-lookup"><span data-stu-id="caa52-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="caa52-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="caa52-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="caa52-127">Une notification incorrecte a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="caa52-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="caa52-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="caa52-128">Remarks</span></span>

<span data-ttu-id="caa52-129">Le paramètre _PCB_ de la fonction **ScRelocNotifications** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="caa52-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="caa52-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="caa52-130">See also</span></span>



[<span data-ttu-id="caa52-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="caa52-131">ScRelocProps</span></span>](screlocprops.md)

