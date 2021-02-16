---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439106"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="e3d1b-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="e3d1b-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="e3d1b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3d1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3d1b-105">Renvoie l’identificateur d’entrée du carnet d’adresses global pour le service Exchange identifié par  _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="e3d1b-106">L’identificateur d’entrée renvoyé doit être libéré à l’aide [de MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e3d1b-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3d1b-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="e3d1b-107">Header file:</span></span>  <br/> |<span data-ttu-id="e3d1b-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="e3d1b-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="e3d1b-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="e3d1b-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3d1b-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="e3d1b-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="e3d1b-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="e3d1b-111">Called by:</span></span>  <br/> |<span data-ttu-id="e3d1b-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="e3d1b-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="e3d1b-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e3d1b-113">Parameters</span></span>

 <span data-ttu-id="e3d1b-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="e3d1b-114">_pSess_</span></span>
  
> <span data-ttu-id="e3d1b-115">[in] IMAPISession connecté.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="e3d1b-116">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e3d1b-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="e3d1b-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="e3d1b-118">[in] Carnet d’adresses utilisé pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="e3d1b-119">Elle ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="e3d1b-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="e3d1b-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="e3d1b-121">[in] Pointeur vers **un emsmdbUID** qui identifie la LA GAL du service Exchange à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="e3d1b-122">Si  _pEmsmdbUID_ a la valeur NULL ou l’UID zéro, cette fonction obtient la LAL héritée du service Exchange.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="e3d1b-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="e3d1b-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="e3d1b-124">[out] Pointeur vers le nombre d’byte de l’identificateur d’entrée de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="e3d1b-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="e3d1b-125">_lppeid_</span></span>
  
> <span data-ttu-id="e3d1b-126">[out] Pointeur vers l’identificateur d’entrée de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="e3d1b-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="e3d1b-127">Cela doit être libéré à [l’aide de MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="e3d1b-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

