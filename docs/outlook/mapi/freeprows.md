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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438819"
---
# <a name="freeprows"></a><span data-ttu-id="2726f-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="2726f-103">FreeProws</span></span>

  
  
<span data-ttu-id="2726f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2726f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2726f-105">Détruit une structure [SRowSet](srowset.md) et libère de la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres.</span><span class="sxs-lookup"><span data-stu-id="2726f-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2726f-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="2726f-106">Header file:</span></span>  <br/> |<span data-ttu-id="2726f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="2726f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2726f-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="2726f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2726f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2726f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2726f-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="2726f-110">Called by:</span></span>  <br/> |<span data-ttu-id="2726f-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="2726f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="2726f-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2726f-112">Parameters</span></span>

 <span data-ttu-id="2726f-113">_PROWS_</span><span class="sxs-lookup"><span data-stu-id="2726f-113">_prows_</span></span>
  
> <span data-ttu-id="2726f-114">dans Pointeur vers la structure **SRowSet** à détruire.</span><span class="sxs-lookup"><span data-stu-id="2726f-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2726f-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2726f-115">Return value</span></span>

<span data-ttu-id="2726f-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2726f-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="2726f-117">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="2726f-117">Notes to callers</span></span>

<span data-ttu-id="2726f-118">Dans le cadre de son implémentation de **FreeProws**, MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer toutes les entrées de la structure **SRowSet** avant de libérer la structure complète.</span><span class="sxs-lookup"><span data-stu-id="2726f-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="2726f-119">Par conséquent, toutes ces entrées doivent avoir suivi les règles d'allocation pour la structure [SRowSet](srowset.md) , à l'aide d'un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque tableau et structure de membres.</span><span class="sxs-lookup"><span data-stu-id="2726f-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="2726f-120">Pour plus d'informations sur l'allocation de mémoire pour les structures **ADRLIST** et **SRowSet** , consultez la rubrique [Managing Memory for ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="2726f-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2726f-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2726f-121">MFCMAPI reference</span></span>

<span data-ttu-id="2726f-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="2726f-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2726f-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="2726f-123">**File**</span></span>|<span data-ttu-id="2726f-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="2726f-124">**Function**</span></span>|<span data-ttu-id="2726f-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="2726f-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2726f-126">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="2726f-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="2726f-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="2726f-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="2726f-128">MFCMAPI utilise la méthode **FreeProws** pour libérer une structure SRowSet contenant les lignes de la table en cours de traitement.</span><span class="sxs-lookup"><span data-stu-id="2726f-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2726f-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2726f-129">See also</span></span>



[<span data-ttu-id="2726f-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="2726f-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

