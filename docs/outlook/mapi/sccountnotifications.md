---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351370"
---
# <a name="sccountnotifications"></a><span data-ttu-id="43dd6-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="43dd6-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="43dd6-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43dd6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43dd6-105">Détermine la taille, en octets, d'un tableau de notifications d'événements et valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="43dd6-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="43dd6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="43dd6-106">Header file:</span></span>  <br/> |<span data-ttu-id="43dd6-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="43dd6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="43dd6-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="43dd6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="43dd6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="43dd6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="43dd6-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="43dd6-110">Called by:</span></span>  <br/> |<span data-ttu-id="43dd6-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="43dd6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="43dd6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43dd6-112">Parameters</span></span>

 <span data-ttu-id="43dd6-113">_CNTF_</span><span class="sxs-lookup"><span data-stu-id="43dd6-113">_cntf_</span></span>
  
> <span data-ttu-id="43dd6-114">dans Nombre de structures de [notification](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="43dd6-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="43dd6-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="43dd6-115">_rgntf_</span></span>
  
> <span data-ttu-id="43dd6-116">dans Pointeur vers le tableau de structures de **notification** dont la taille doit être déterminée.</span><span class="sxs-lookup"><span data-stu-id="43dd6-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="43dd6-117">_circuits_</span><span class="sxs-lookup"><span data-stu-id="43dd6-117">_pcb_</span></span>
  
> <span data-ttu-id="43dd6-118">remarquer Pointeur facultatif vers la taille, en octets, du tableau désigné par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="43dd6-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="43dd6-119">Si la valeur est NULL, **ScCountNotifications** valide le tableau de notifications.</span><span class="sxs-lookup"><span data-stu-id="43dd6-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="43dd6-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="43dd6-120">Return value</span></span>

<span data-ttu-id="43dd6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="43dd6-121">S_OK</span></span>
  
> <span data-ttu-id="43dd6-122">Le nombre a été déterminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="43dd6-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="43dd6-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="43dd6-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="43dd6-124">Une notification incorrecte a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="43dd6-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43dd6-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="43dd6-125">Remarks</span></span>

<span data-ttu-id="43dd6-126">Si NULL est transmis dans le paramètre _PCB_ , la fonction **ScCountNotifications** valide uniquement le tableau des notifications, mais aucun décompte n'est réalisé; Si une valeur non null est transmise dans _PCB_, **ScCountNotifications** détermine la taille du tableau et stocke la cause de la _PCB_.</span><span class="sxs-lookup"><span data-stu-id="43dd6-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="43dd6-127">Le paramètre _PCB_ doit être assez grand pour contenir l'intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="43dd6-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

