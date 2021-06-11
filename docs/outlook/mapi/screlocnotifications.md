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
# <a name="screlocnotifications"></a><span data-ttu-id="0c976-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="0c976-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="0c976-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c976-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c976-105">Ajuste un pointeur dans un tableau de notifications d’événements spécifié.</span><span class="sxs-lookup"><span data-stu-id="0c976-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c976-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="0c976-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c976-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0c976-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0c976-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="0c976-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c976-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c976-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c976-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="0c976-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c976-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="0c976-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="0c976-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c976-112">Parameters</span></span>

 <span data-ttu-id="0c976-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="0c976-113">_cntf_</span></span>
  
> <span data-ttu-id="0c976-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="0c976-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="0c976-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="0c976-115">_rgntf_</span></span>
  
> <span data-ttu-id="0c976-116">[in] Pointeur vers le tableau de **structures DE NOTIFICATION** définissant les notifications d’événement dans lesquelles un pointeur doit être ajusté.</span><span class="sxs-lookup"><span data-stu-id="0c976-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="0c976-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="0c976-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="0c976-118">[in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="0c976-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="0c976-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="0c976-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="0c976-120">[in] Emplacement auquel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiqué par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="0c976-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="0c976-121">_pcb_</span><span class="sxs-lookup"><span data-stu-id="0c976-121">_pcb_</span></span>
  
> <span data-ttu-id="0c976-122">[out] Pointeur vers la taille, en octets, du tableau indiqué par le _paramètre pvBaseNew._</span><span class="sxs-lookup"><span data-stu-id="0c976-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c976-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0c976-123">Return value</span></span>

<span data-ttu-id="0c976-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c976-124">S_OK</span></span>
  
> <span data-ttu-id="0c976-125">Un pointeur a été ajusté avec succès.</span><span class="sxs-lookup"><span data-stu-id="0c976-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="0c976-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0c976-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="0c976-127">Une notification non valide a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="0c976-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c976-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c976-128">Remarks</span></span>

<span data-ttu-id="0c976-129">Le  _paramètre pcb_ de la **fonction ScRelocNotifications** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="0c976-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0c976-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c976-130">See also</span></span>



[<span data-ttu-id="0c976-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="0c976-131">ScRelocProps</span></span>](screlocprops.md)

