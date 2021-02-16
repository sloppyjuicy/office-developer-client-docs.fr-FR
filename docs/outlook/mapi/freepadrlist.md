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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408641"
---
# <a name="freepadrlist"></a><span data-ttu-id="cafe0-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="cafe0-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="cafe0-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cafe0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cafe0-105">Détruit une structure [ADRLIST](adrlist.md) et libère la mémoire associée, y compris la mémoire allouée à tous les tableaux et structures membres.</span><span class="sxs-lookup"><span data-stu-id="cafe0-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cafe0-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="cafe0-106">Header file:</span></span>  <br/> |<span data-ttu-id="cafe0-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="cafe0-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="cafe0-108">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="cafe0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="cafe0-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="cafe0-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="cafe0-110">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="cafe0-110">Called by:</span></span>  <br/> |<span data-ttu-id="cafe0-111">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="cafe0-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="cafe0-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cafe0-112">Parameters</span></span>

 <span data-ttu-id="cafe0-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="cafe0-113">_padrlist_</span></span>
  
> <span data-ttu-id="cafe0-114">[in] Pointeur vers la structure **ADRLIST** à détruire.</span><span class="sxs-lookup"><span data-stu-id="cafe0-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="cafe0-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cafe0-115">Return value</span></span>

<span data-ttu-id="cafe0-116">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cafe0-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="cafe0-117">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="cafe0-117">Notes to callers</span></span>

<span data-ttu-id="cafe0-118">Dans le cadre de son implémentation de **FreePadrlist,** MAPI appelle la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer chaque entrée dans la structure **ADRLIST** avant de libérer la structure complète.</span><span class="sxs-lookup"><span data-stu-id="cafe0-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="cafe0-119">Par conséquent, toutes ces entrées doivent avoir suivi les règles d’allocation pour la structure [ADRLIST,](adrlist.md) à l’aide d’un appel [MAPIAllocateBuffer](mapiallocatebuffer.md) individuel pour chaque matrice et structure de membre.</span><span class="sxs-lookup"><span data-stu-id="cafe0-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="cafe0-120">Pour plus d’informations sur l’allocation de mémoire pour les structures **ADRLIST** et **SRowSet,** voir [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="cafe0-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cafe0-121">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="cafe0-121">MFCMAPI reference</span></span>

<span data-ttu-id="cafe0-122">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="cafe0-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cafe0-123">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="cafe0-123">**File**</span></span>|<span data-ttu-id="cafe0-124">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="cafe0-124">**Function**</span></span>|<span data-ttu-id="cafe0-125">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="cafe0-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cafe0-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="cafe0-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="cafe0-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="cafe0-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="cafe0-128">MFCMAPI utilise la **méthode FreePadrlist** pour libérer une structure ADRLIST qui a été conçue pour ajouter une adresse à un message.</span><span class="sxs-lookup"><span data-stu-id="cafe0-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cafe0-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cafe0-129">See also</span></span>



[<span data-ttu-id="cafe0-130">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="cafe0-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

