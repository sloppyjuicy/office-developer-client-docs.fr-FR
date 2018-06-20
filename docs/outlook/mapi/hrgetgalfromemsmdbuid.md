---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783542"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="9eca6-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="9eca6-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="9eca6-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9eca6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9eca6-105">Renvoie l’identificateur d’entrée du carnet d’adresses globale pour le service Exchange identifié par _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="9eca6-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="9eca6-106">L’identificateur d’entrée renvoyée doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9eca6-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9eca6-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="9eca6-107">Header file:</span></span>  <br/> |<span data-ttu-id="9eca6-108">abhelp.h</span><span class="sxs-lookup"><span data-stu-id="9eca6-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="9eca6-109">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="9eca6-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="9eca6-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="9eca6-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="9eca6-111">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="9eca6-111">Called by:</span></span>  <br/> |<span data-ttu-id="9eca6-112">Les applications clientes et des fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="9eca6-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="9eca6-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9eca6-113">Parameters</span></span>

 <span data-ttu-id="9eca6-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="9eca6-114">_pSess_</span></span>
  
> <span data-ttu-id="9eca6-115">[in] La session IMAPISession.</span><span class="sxs-lookup"><span data-stu-id="9eca6-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="9eca6-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="9eca6-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9eca6-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="9eca6-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="9eca6-118">[in] Le carnet d’adresses utilisée pour ouvrir l’identificateur d’entrée.</span><span class="sxs-lookup"><span data-stu-id="9eca6-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="9eca6-119">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="9eca6-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="9eca6-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="9eca6-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="9eca6-121">[in] Pointeur vers un **emsmdbUID** qui identifie la liste d’adresses globale du Service Exchange à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9eca6-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="9eca6-122">Si _pEmsmdbUID_ est NULL ou l’UID de zéro, cette fonction obtient la liste d’adresses globale héritée du Service Exchange.</span><span class="sxs-lookup"><span data-stu-id="9eca6-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="9eca6-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="9eca6-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="9eca6-124">[out] Pointeur vers le nombre d’octets de l’identificateur d’entrée de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="9eca6-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="9eca6-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="9eca6-125">_lppeid_</span></span>
  
> <span data-ttu-id="9eca6-126">[out] Pointeur vers l’identificateur d’entrée de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="9eca6-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="9eca6-127">Il doit être libéré à l’aide de [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="9eca6-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

