---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576546"
---
# <a name="freepadrlist"></a><span data-ttu-id="fb3a6-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="fb3a6-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="fb3a6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb3a6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb3a6-105">Détruit une structure [ADRLIST](adrlist.md) et libère de la mémoire associée, y compris la mémoire allouée pour tous les tableaux membres et les structures.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb3a6-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="fb3a6-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb3a6-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="fb3a6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="fb3a6-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="fb3a6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fb3a6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fb3a6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fb3a6-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="fb3a6-110">Called by:</span></span>  <br/> |<span data-ttu-id="fb3a6-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="fb3a6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="fb3a6-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb3a6-112">Parameters</span></span>

 <span data-ttu-id="fb3a6-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="fb3a6-113">_padrlist_</span></span>
  
> <span data-ttu-id="fb3a6-114">[in] Pointeur vers la structure **ADRLIST** destruction.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb3a6-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fb3a6-115">Return value</span></span>

<span data-ttu-id="fb3a6-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="fb3a6-117">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="fb3a6-117">Notes to callers</span></span>

<span data-ttu-id="fb3a6-118">Dans le cadre de son implémentation de **FreePadrlist**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de chaque entrée dans la structure **ADRLIST** avant de libérer la structure complète.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="fb3a6-119">Par conséquent, toutes les entrées de ce type doivent avoir suivi les règles d’allocation de la structure [ADRLIST](adrlist.md) , à l’aide d’une personne [MAPIAllocateBuffer](mapiallocatebuffer.md) appeler pour chaque tableau de membres et de la structure.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="fb3a6-120">Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="fb3a6-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fb3a6-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fb3a6-121">MFCMAPI reference</span></span>

<span data-ttu-id="fb3a6-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fb3a6-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="fb3a6-123">**File**</span></span>|<span data-ttu-id="fb3a6-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="fb3a6-124">**Function**</span></span>|<span data-ttu-id="fb3a6-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="fb3a6-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb3a6-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fb3a6-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fb3a6-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="fb3a6-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="fb3a6-128">MFCMAPI utilise la méthode **FreePadrlist** pour libérer une structure ADRLIST qui a été conçue pour ajouter une adresse unique à un message.</span><span class="sxs-lookup"><span data-stu-id="fb3a6-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fb3a6-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb3a6-129">See also</span></span>



[<span data-ttu-id="fb3a6-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="fb3a6-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

