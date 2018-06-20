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
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787083"
---
# <a name="sccountnotifications"></a><span data-ttu-id="98e81-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="98e81-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="98e81-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="98e81-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="98e81-105">Détermine la taille, en octets, d’un tableau de notifications d’événements et valide la mémoire associée au tableau.</span><span class="sxs-lookup"><span data-stu-id="98e81-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="98e81-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="98e81-106">Header file:</span></span>  <br/> |<span data-ttu-id="98e81-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="98e81-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="98e81-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="98e81-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="98e81-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="98e81-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="98e81-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="98e81-110">Called by:</span></span>  <br/> |<span data-ttu-id="98e81-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="98e81-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="98e81-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="98e81-112">Parameters</span></span>

 <span data-ttu-id="98e81-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="98e81-113">_cntf_</span></span>
  
> <span data-ttu-id="98e81-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="98e81-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="98e81-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="98e81-115">_rgntf_</span></span>
  
> <span data-ttu-id="98e81-116">[in] Pointeur vers le tableau des structures **NOTIFICATION** dont la taille est déterminée.</span><span class="sxs-lookup"><span data-stu-id="98e81-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="98e81-117">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="98e81-117">_pcb_</span></span>
  
> <span data-ttu-id="98e81-118">[out] Pointeur facultatif à la taille, en octets, du tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="98e81-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="98e81-119">Si la valeur NULL, **ScCountNotifications** valide le tableau des notifications.</span><span class="sxs-lookup"><span data-stu-id="98e81-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98e81-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="98e81-120">Return value</span></span>

<span data-ttu-id="98e81-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="98e81-121">S_OK</span></span>
  
> <span data-ttu-id="98e81-122">Count a été correctement déterminé.</span><span class="sxs-lookup"><span data-stu-id="98e81-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="98e81-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98e81-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="98e81-124">Une notification non valide s’est produite.</span><span class="sxs-lookup"><span data-stu-id="98e81-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98e81-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="98e81-125">Remarks</span></span>

<span data-ttu-id="98e81-126">Si NULL est indiqué dans le paramètre de la _carte de circuit imprimé_ , la fonction **ScCountNotifications** valide uniquement le tableau des notifications, mais aucun décompte n’effectué ; Si une valeur non nulle est passée dans une _carte de circuit imprimé_, **ScCountNotifications** détermine la taille du tableau et stocke la cause la _carte de circuit imprimé_.</span><span class="sxs-lookup"><span data-stu-id="98e81-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="98e81-127">Le paramètre de la _carte de circuit imprimé_ doit être suffisant pour contenir l’intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="98e81-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

