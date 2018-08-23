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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583966"
---
# <a name="screlocnotifications"></a><span data-ttu-id="893db-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="893db-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="893db-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="893db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="893db-105">Ajuste un pointeur au sein d’un tableau de notification d’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="893db-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="893db-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="893db-106">Header file:</span></span>  <br/> |<span data-ttu-id="893db-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="893db-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="893db-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="893db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="893db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="893db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="893db-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="893db-110">Called by:</span></span>  <br/> |<span data-ttu-id="893db-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="893db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="893db-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="893db-112">Parameters</span></span>

 <span data-ttu-id="893db-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="893db-113">_cntf_</span></span>
  
> <span data-ttu-id="893db-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="893db-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="893db-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="893db-115">_rgntf_</span></span>
  
> <span data-ttu-id="893db-116">[in] Pointeur vers le tableau des structures **NOTIFICATION** définition des notifications d’événement dans lequel un pointeur doit être ajustées.</span><span class="sxs-lookup"><span data-stu-id="893db-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="893db-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="893db-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="893db-118">[in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="893db-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="893db-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="893db-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="893db-120">[in] L’emplacement dans lequel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="893db-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="893db-121">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="893db-121">_pcb_</span></span>
  
> <span data-ttu-id="893db-122">[out] Pointeur vers la taille, en octets, du tableau indiquée par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="893db-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="893db-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="893db-123">Return value</span></span>

<span data-ttu-id="893db-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="893db-124">S_OK</span></span>
  
> <span data-ttu-id="893db-125">Un pointeur ajusté avec succès.</span><span class="sxs-lookup"><span data-stu-id="893db-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="893db-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="893db-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="893db-127">Une notification non valide s’est produite.</span><span class="sxs-lookup"><span data-stu-id="893db-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="893db-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="893db-128">Remarks</span></span>

<span data-ttu-id="893db-129">Le paramètre de la _carte de circuits imprimés_ à la fonction **ScRelocNotifications** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="893db-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="893db-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="893db-130">See also</span></span>



[<span data-ttu-id="893db-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="893db-131">ScRelocProps</span></span>](screlocprops.md)

