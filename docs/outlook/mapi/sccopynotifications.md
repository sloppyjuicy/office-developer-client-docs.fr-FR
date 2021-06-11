---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435921"
---
# <a name="sccopynotifications"></a><span data-ttu-id="4ace0-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="4ace0-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="4ace0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ace0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ace0-105">Copie un groupe de notifications d’événements dans un seul bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ace0-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ace0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="4ace0-106">Header file:</span></span>  <br/> |<span data-ttu-id="4ace0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4ace0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4ace0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="4ace0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4ace0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4ace0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4ace0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="4ace0-110">Called by:</span></span>  <br/> |<span data-ttu-id="4ace0-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="4ace0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="4ace0-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="4ace0-112">Parameters</span></span>

 <span data-ttu-id="4ace0-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="4ace0-113">_cntf_</span></span>
  
> <span data-ttu-id="4ace0-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le _paramètre rgntf._</span><span class="sxs-lookup"><span data-stu-id="4ace0-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="4ace0-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="4ace0-115">_rgntf_</span></span>
  
> <span data-ttu-id="4ace0-116">[in] Pointeur vers un tableau de structures **DE NOTIFICATION** définissant les notifications d’événement à copier.</span><span class="sxs-lookup"><span data-stu-id="4ace0-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="4ace0-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="4ace0-117">_pvDst_</span></span>
  
> <span data-ttu-id="4ace0-118">[out] Pointeur vers les notifications renvoyées.</span><span class="sxs-lookup"><span data-stu-id="4ace0-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="4ace0-119">_pcb_</span><span class="sxs-lookup"><span data-stu-id="4ace0-119">_pcb_</span></span>
  
> <span data-ttu-id="4ace0-120">[out] Pointeur facultatif vers une variable où la taille, en octets, du tableau pointé par le paramètre  _rgntf_ est stockée.</span><span class="sxs-lookup"><span data-stu-id="4ace0-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="4ace0-121">Si la valeur n’est pas NULL, le _paramètre pcb_ est définie sur le nombre d’octets stockés dans le _paramètre pvDst._</span><span class="sxs-lookup"><span data-stu-id="4ace0-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4ace0-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4ace0-122">Return value</span></span>

<span data-ttu-id="4ace0-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="4ace0-123">S_OK</span></span>
  
> <span data-ttu-id="4ace0-124">Les notifications d’événement ont été correctement copiées.</span><span class="sxs-lookup"><span data-stu-id="4ace0-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="4ace0-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4ace0-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="4ace0-126">Une notification non valide a été rencontrée.</span><span class="sxs-lookup"><span data-stu-id="4ace0-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4ace0-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="4ace0-127">Remarks</span></span>

<span data-ttu-id="4ace0-128">Si null est transmis dans le  _paramètre pcb,_ aucune copie n’est effectuée ; Si une valeur non null est passée dans  _pcb,_ la fonction **ScCopyNotifications** copie la taille du tableau et du tableau lui-même dans un seul bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="4ace0-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="4ace0-129">Si _pcb n’est_ pas NULL, il est fixé au nombre d’octets stockés dans le _paramètre pvDst._</span><span class="sxs-lookup"><span data-stu-id="4ace0-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="4ace0-130">Le  _paramètre pvDst_ doit être suffisamment grand pour contenir la totalité du tableau.</span><span class="sxs-lookup"><span data-stu-id="4ace0-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

