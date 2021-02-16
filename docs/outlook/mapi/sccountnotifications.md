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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437993"
---
# <a name="sccountnotifications"></a><span data-ttu-id="b14a0-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="b14a0-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="b14a0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b14a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b14a0-105">Détermine la taille, en octets, d’un tableau de notifications d’événements et valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="b14a0-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b14a0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="b14a0-106">Header file:</span></span>  <br/> |<span data-ttu-id="b14a0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b14a0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b14a0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="b14a0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b14a0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b14a0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b14a0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="b14a0-110">Called by:</span></span>  <br/> |<span data-ttu-id="b14a0-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="b14a0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="b14a0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b14a0-112">Parameters</span></span>

 <span data-ttu-id="b14a0-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="b14a0-113">_cntf_</span></span>
  
> <span data-ttu-id="b14a0-114">[in] Nombre de structures [DE NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="b14a0-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="b14a0-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="b14a0-115">_rgntf_</span></span>
  
> <span data-ttu-id="b14a0-116">[in] Pointeur vers le tableau des structures **DE NOTIFICATION** dont la taille doit être déterminée.</span><span class="sxs-lookup"><span data-stu-id="b14a0-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="b14a0-117">_pcb_</span><span class="sxs-lookup"><span data-stu-id="b14a0-117">_pcb_</span></span>
  
> <span data-ttu-id="b14a0-118">[out] Pointeur facultatif vers la taille, en octets, du tableau pointé par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="b14a0-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="b14a0-119">Si la valeur est NULL, **ScCountNotifications** valide le tableau des notifications.</span><span class="sxs-lookup"><span data-stu-id="b14a0-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b14a0-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b14a0-120">Return value</span></span>

<span data-ttu-id="b14a0-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b14a0-121">S_OK</span></span>
  
> <span data-ttu-id="b14a0-122">Le nombre a été déterminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="b14a0-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="b14a0-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b14a0-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="b14a0-124">Une notification non valide a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="b14a0-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b14a0-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="b14a0-125">Remarks</span></span>

<span data-ttu-id="b14a0-126">Si NULL est transmis dans le  _paramètre pcb,_ la **fonction ScCountNotifications** valide uniquement le tableau de notifications, mais aucun décompte n’est effectué . si une valeur non null est passée dans  _pcb_, **ScCountNotifications** détermine la taille du tableau et stocke la  _cause pcb_.</span><span class="sxs-lookup"><span data-stu-id="b14a0-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="b14a0-127">Le  _paramètre pcb_ doit être suffisamment grand pour contenir la totalité du tableau.</span><span class="sxs-lookup"><span data-stu-id="b14a0-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

