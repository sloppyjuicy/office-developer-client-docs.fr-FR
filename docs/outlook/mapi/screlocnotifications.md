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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415200"
---
# <a name="screlocnotifications"></a><span data-ttu-id="e2100-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="e2100-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="e2100-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2100-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2100-105">Ajuste un pointeur dans un tableau de notification d'événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2100-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e2100-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e2100-106">Header file:</span></span>  <br/> |<span data-ttu-id="e2100-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="e2100-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e2100-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e2100-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e2100-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e2100-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e2100-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e2100-110">Called by:</span></span>  <br/> |<span data-ttu-id="e2100-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e2100-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="e2100-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2100-112">Parameters</span></span>

 <span data-ttu-id="e2100-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="e2100-113">_cntf_</span></span>
  
> <span data-ttu-id="e2100-114">dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="e2100-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="e2100-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="e2100-115">_rgntf_</span></span>
  
> <span data-ttu-id="e2100-116">dans Pointeur vers le tableau de structures de **notification** définissant des notifications d'événement dans lesquelles un pointeur doit être ajusté.</span><span class="sxs-lookup"><span data-stu-id="e2100-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="e2100-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="e2100-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="e2100-118">dans Pointeur vers l'adresse de base d'origine du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="e2100-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="e2100-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="e2100-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="e2100-120">dans Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="e2100-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="e2100-121">_circuits_</span><span class="sxs-lookup"><span data-stu-id="e2100-121">_pcb_</span></span>
  
> <span data-ttu-id="e2100-122">remarquer Pointeur vers la taille, en octets, du tableau indiqué par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="e2100-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e2100-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2100-123">Return value</span></span>

<span data-ttu-id="e2100-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2100-124">S_OK</span></span>
  
> <span data-ttu-id="e2100-125">Un pointeur a été ajusté avec succès.</span><span class="sxs-lookup"><span data-stu-id="e2100-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="e2100-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e2100-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="e2100-127">Une notification incorrecte a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="e2100-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e2100-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2100-128">Remarks</span></span>

<span data-ttu-id="e2100-129">Le paramètre _PCB_ de la fonction **ScRelocNotifications** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="e2100-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e2100-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2100-130">See also</span></span>



[<span data-ttu-id="e2100-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="e2100-131">ScRelocProps</span></span>](screlocprops.md)

