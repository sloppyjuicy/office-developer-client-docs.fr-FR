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
ms.openlocfilehash: bb4ff6a128b9fed29ff0be5325c21e5600389740
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787109"
---
# <a name="screlocnotifications"></a><span data-ttu-id="97e89-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="97e89-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="97e89-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97e89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97e89-105">Ajuste un pointeur au sein d’un tableau de notification d’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="97e89-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97e89-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="97e89-106">Header file:</span></span>  <br/> |<span data-ttu-id="97e89-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="97e89-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="97e89-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="97e89-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="97e89-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="97e89-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="97e89-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="97e89-110">Called by:</span></span>  <br/> |<span data-ttu-id="97e89-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="97e89-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="97e89-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97e89-112">Parameters</span></span>

 <span data-ttu-id="97e89-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="97e89-113">_cntf_</span></span>
  
> <span data-ttu-id="97e89-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="97e89-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="97e89-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="97e89-115">_rgntf_</span></span>
  
> <span data-ttu-id="97e89-116">[in] Pointeur vers le tableau des structures **NOTIFICATION** définition des notifications d’événement dans lequel un pointeur doit être ajustées.</span><span class="sxs-lookup"><span data-stu-id="97e89-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="97e89-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="97e89-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="97e89-118">[in] Pointeur vers l’adresse de base d’origine du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="97e89-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="97e89-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="97e89-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="97e89-120">[in] L’emplacement dans lequel **ScRelocNotifications** écrit la nouvelle adresse de base du tableau indiquée par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="97e89-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="97e89-121">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="97e89-121">_pcb_</span></span>
  
> <span data-ttu-id="97e89-122">[out] Pointeur vers la taille, en octets, du tableau indiquée par le paramètre _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="97e89-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97e89-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="97e89-123">Return value</span></span>

<span data-ttu-id="97e89-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="97e89-124">S_OK</span></span>
  
> <span data-ttu-id="97e89-125">Un pointeur ajusté avec succès.</span><span class="sxs-lookup"><span data-stu-id="97e89-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="97e89-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="97e89-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="97e89-127">Une notification non valide s’est produite.</span><span class="sxs-lookup"><span data-stu-id="97e89-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="97e89-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="97e89-128">Remarks</span></span>

<span data-ttu-id="97e89-129">Le paramètre de la _carte de circuits imprimés_ à la fonction **ScRelocNotifications** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="97e89-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="97e89-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="97e89-130">See also</span></span>



[<span data-ttu-id="97e89-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="97e89-131">ScRelocProps</span></span>](screlocprops.md)

