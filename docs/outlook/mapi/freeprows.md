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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783371"
---
# <a name="freeprows"></a><span data-ttu-id="79942-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="79942-103">FreeProws</span></span>

  
  
<span data-ttu-id="79942-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="79942-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="79942-105">Détruit une structure [SRowSet](srowset.md) et libère de la mémoire associée, y compris la mémoire allouée pour tous les tableaux membres et les structures.</span><span class="sxs-lookup"><span data-stu-id="79942-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79942-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="79942-106">Header file:</span></span>  <br/> |<span data-ttu-id="79942-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="79942-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="79942-108">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="79942-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="79942-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="79942-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="79942-110">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="79942-110">Called by:</span></span>  <br/> |<span data-ttu-id="79942-111">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="79942-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="79942-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79942-112">Parameters</span></span>

 <span data-ttu-id="79942-113">_PROWS_</span><span class="sxs-lookup"><span data-stu-id="79942-113">_prows_</span></span>
  
> <span data-ttu-id="79942-114">[in] Pointeur vers la structure **SRowSet** destruction.</span><span class="sxs-lookup"><span data-stu-id="79942-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="79942-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="79942-115">Return value</span></span>

<span data-ttu-id="79942-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="79942-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="79942-117">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="79942-117">Notes to callers</span></span>

<span data-ttu-id="79942-118">Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer de chaque entrée dans la structure **SRowSet** avant de libérer la structure complète.</span><span class="sxs-lookup"><span data-stu-id="79942-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="79942-119">Par conséquent, toutes les entrées de ce type doivent avoir suivi les règles d’allocation de la structure [SRowSet](srowset.md) , à l’aide d’une personne [MAPIAllocateBuffer](mapiallocatebuffer.md) appeler pour chaque tableau de membres et de la structure.</span><span class="sxs-lookup"><span data-stu-id="79942-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="79942-120">Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , voir [Gestion de la mémoire ADRLIST des Structures SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="79942-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="79942-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="79942-121">MFCMAPI reference</span></span>

<span data-ttu-id="79942-122">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="79942-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="79942-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="79942-123">**File**</span></span>|<span data-ttu-id="79942-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="79942-124">**Function**</span></span>|<span data-ttu-id="79942-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="79942-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="79942-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="79942-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="79942-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="79942-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="79942-128">MFCMAPI utilise la méthode **FreeProws** pour libérer une structure SRowSet contenant les lignes de la table en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="79942-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="79942-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79942-129">See also</span></span>



[<span data-ttu-id="79942-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="79942-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

