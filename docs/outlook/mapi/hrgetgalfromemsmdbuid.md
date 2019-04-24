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
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347830"
---
# <a name="hrgetgalfromemsmdbuid"></a><span data-ttu-id="845f9-103">HrGetGALFromEmsmdbUID</span><span class="sxs-lookup"><span data-stu-id="845f9-103">HrGetGALFromEmsmdbUID</span></span>

  
  
<span data-ttu-id="845f9-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="845f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="845f9-105">Renvoie l'identificateur d'entrée du carnet d'adresses global pour le service Exchange identifié par _pEmsmdbUID_.</span><span class="sxs-lookup"><span data-stu-id="845f9-105">Returns the entry identifier of the global address book for the Exchange service identified by  _pEmsmdbUID_.</span></span> <span data-ttu-id="845f9-106">L'identificateur d'entrée retourné doit être libéré à l'aide de [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="845f9-106">The returned entry identifier should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="845f9-107">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="845f9-107">Header file:</span></span>  <br/> |<span data-ttu-id="845f9-108">abhelp. h</span><span class="sxs-lookup"><span data-stu-id="845f9-108">abhelp.h</span></span>  <br/> |
|<span data-ttu-id="845f9-109">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="845f9-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="845f9-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="845f9-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="845f9-111">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="845f9-111">Called by:</span></span>  <br/> |<span data-ttu-id="845f9-112">Applications clientes et fournisseurs de services</span><span class="sxs-lookup"><span data-stu-id="845f9-112">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a><span data-ttu-id="845f9-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="845f9-113">Parameters</span></span>

 <span data-ttu-id="845f9-114">_pSess_</span><span class="sxs-lookup"><span data-stu-id="845f9-114">_pSess_</span></span>
  
> <span data-ttu-id="845f9-115">dans Le IMAPISession connecté.</span><span class="sxs-lookup"><span data-stu-id="845f9-115">[in] The logged on IMAPISession.</span></span> <span data-ttu-id="845f9-116">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="845f9-116">It cannot be NULL.</span></span>
    
 <span data-ttu-id="845f9-117">_pAddrBook_</span><span class="sxs-lookup"><span data-stu-id="845f9-117">_pAddrBook_</span></span>
  
> <span data-ttu-id="845f9-118">dans Carnet d'adresses utilisé pour ouvrir l'identificateur d'entrée.</span><span class="sxs-lookup"><span data-stu-id="845f9-118">[in] The address book used to open the entry identifier.</span></span> <span data-ttu-id="845f9-119">Il ne peut pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="845f9-119">It cannot be NULL.</span></span>
    
 <span data-ttu-id="845f9-120">_pEmsmdbUID_</span><span class="sxs-lookup"><span data-stu-id="845f9-120">_pEmsmdbUID_</span></span>
  
> <span data-ttu-id="845f9-121">dans Pointeur vers un **emsmdbUID** qui identifie la liste d'adresses globale du service Exchange à récupérer.</span><span class="sxs-lookup"><span data-stu-id="845f9-121">[in] A pointer to an **emsmdbUID** that identifies the GAL of the Exchange Service to be retrieved.</span></span> <span data-ttu-id="845f9-122">Si _pEmsmdbUID_ est null ou zéro uid, cette fonction obtient la lag héritée du service Exchange.</span><span class="sxs-lookup"><span data-stu-id="845f9-122">If  _pEmsmdbUID_ is NULL or the zero UID, this function gets the legacy GAL of the Exchange Service.</span></span> 
    
 <span data-ttu-id="845f9-123">_lpcbeid_</span><span class="sxs-lookup"><span data-stu-id="845f9-123">_lpcbeid_</span></span>
  
> <span data-ttu-id="845f9-124">remarquer Pointeur vers le nombre d'octets de l'identificateur d'entrée de la liste d'adresses globale.</span><span class="sxs-lookup"><span data-stu-id="845f9-124">[out] A pointer to the byte count of the entry identifier of the global address list.</span></span>
    
 <span data-ttu-id="845f9-125">_lppeid_</span><span class="sxs-lookup"><span data-stu-id="845f9-125">_lppeid_</span></span>
  
> <span data-ttu-id="845f9-126">remarquer Pointeur vers l'identificateur d'entrée de la liste d'adresses globale.</span><span class="sxs-lookup"><span data-stu-id="845f9-126">[out] A pointer to the entry identifier of the global address list.</span></span> <span data-ttu-id="845f9-127">Cela doit être libéré à l'aide de [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="845f9-127">This should be freed using [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
    

