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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593353"
---
# <a name="sccopynotifications"></a><span data-ttu-id="8b1c1-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="8b1c1-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="8b1c1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b1c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b1c1-105">Copie un groupe de notifications d’événements dans un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8b1c1-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="8b1c1-106">Header file:</span></span>  <br/> |<span data-ttu-id="8b1c1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8b1c1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8b1c1-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="8b1c1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8b1c1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8b1c1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8b1c1-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="8b1c1-110">Called by:</span></span>  <br/> |<span data-ttu-id="8b1c1-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="8b1c1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="8b1c1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b1c1-112">Parameters</span></span>

 <span data-ttu-id="8b1c1-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="8b1c1-113">_cntf_</span></span>
  
> <span data-ttu-id="8b1c1-114">[in] Nombre de structures [NOTIFICATION](notification.md) dans le tableau indiqué par le paramètre _rgntf_ .</span><span class="sxs-lookup"><span data-stu-id="8b1c1-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="8b1c1-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="8b1c1-115">_rgntf_</span></span>
  
> <span data-ttu-id="8b1c1-116">[in] Pointeur vers un tableau de structures **NOTIFICATION** définissant les notifications d’événements à copier.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="8b1c1-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="8b1c1-117">_pvDst_</span></span>
  
> <span data-ttu-id="8b1c1-118">[out] Pointeur vers les notifications retournées.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="8b1c1-119">_carte de circuit imprimé_</span><span class="sxs-lookup"><span data-stu-id="8b1c1-119">_pcb_</span></span>
  
> <span data-ttu-id="8b1c1-120">[out] Facultatif pointeur vers une variable dont la taille, en octets, du tableau indiquée par le paramètre _rgntf_ est stockée.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="8b1c1-121">Si ce n’est pas NULL, le paramètre de la _carte de circuits imprimés_ est défini sur le nombre d’octets stocké dans le paramètre _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="8b1c1-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8b1c1-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8b1c1-122">Return value</span></span>

<span data-ttu-id="8b1c1-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b1c1-123">S_OK</span></span>
  
> <span data-ttu-id="8b1c1-124">Notifications d’événement ont été copiées avec succès.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="8b1c1-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8b1c1-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="8b1c1-126">Une notification non valide s’est produite.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b1c1-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="8b1c1-127">Remarks</span></span>

<span data-ttu-id="8b1c1-128">Si NULL est indiqué dans le paramètre de la _carte de circuits imprimés_ , aucune copie n’est effectuée ; Si une valeur non nulle est passée dans une _carte de circuit imprimé_, la fonction **ScCopyNotifications** copie la taille du tableau et le tableau lui-même dans un bloc de mémoire.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="8b1c1-129">Si la _carte de circuits imprimés_ n’est pas NULL, elle est définie pour le nombre d’octets stocké dans le paramètre _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="8b1c1-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="8b1c1-130">Le paramètre _pvDst_ doit être suffisant pour contenir l’intégralité du tableau.</span><span class="sxs-lookup"><span data-stu-id="8b1c1-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

