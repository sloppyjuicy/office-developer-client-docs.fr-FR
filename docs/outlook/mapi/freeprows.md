---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578023"
---
# <a name="freeprows"></a><span data-ttu-id="ba6dd-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="ba6dd-103">FreeProws</span></span>

  
  
<span data-ttu-id="ba6dd-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ba6dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ba6dd-105">Détruit une structure [SRowSet](srowset.md) et libère de la mémoire associée, y compris la mémoire allouée pour tous les tableaux membres et les structures.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ba6dd-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="ba6dd-106">Header file:</span></span>  <br/> |<span data-ttu-id="ba6dd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ba6dd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ba6dd-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="ba6dd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ba6dd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ba6dd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ba6dd-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="ba6dd-110">Called by:</span></span>  <br/> |<span data-ttu-id="ba6dd-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="ba6dd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="ba6dd-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba6dd-112">Parameters</span></span>

 <span data-ttu-id="ba6dd-113">_PROWS_</span><span class="sxs-lookup"><span data-stu-id="ba6dd-113">_prows_</span></span>
  
> <span data-ttu-id="ba6dd-114">[in] Pointeur vers la structure **SRowSet** destruction.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ba6dd-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ba6dd-115">Return value</span></span>

<span data-ttu-id="ba6dd-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ba6dd-117">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="ba6dd-117">Notes to callers</span></span>

<span data-ttu-id="ba6dd-118">Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de chaque entrée dans la structure **SRowSet** avant de libérer la structure complète.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="ba6dd-119">Par conséquent, toutes les entrées de ce type doivent avoir suivi les règles d’allocation de la structure [SRowSet](srowset.md) , à l’aide d’une personne [MAPIAllocateBuffer](mapiallocatebuffer.md) appeler pour chaque tableau de membres et de la structure.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="ba6dd-120">Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="ba6dd-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ba6dd-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ba6dd-121">MFCMAPI reference</span></span>

<span data-ttu-id="ba6dd-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ba6dd-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ba6dd-123">**File**</span></span>|<span data-ttu-id="ba6dd-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ba6dd-124">**Function**</span></span>|<span data-ttu-id="ba6dd-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ba6dd-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ba6dd-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ba6dd-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ba6dd-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="ba6dd-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="ba6dd-128">MFCMAPI utilise la méthode **FreeProws** pour libérer une structure SRowSet contenant les lignes de la table en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="ba6dd-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ba6dd-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba6dd-129">See also</span></span>



[<span data-ttu-id="ba6dd-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="ba6dd-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

