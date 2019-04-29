---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410468"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="38be1-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="38be1-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="38be1-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38be1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38be1-105">Renvoie la Banque de messages qui contient le message actif, si ce type de magasin existe.</span><span class="sxs-lookup"><span data-stu-id="38be1-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="38be1-106">Cette méthode renvoie la valeur NULL dans le paramètre _ppStore_ pour les messages incorporés, qui sont stockés dans un autre message au lieu d'être directement dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="38be1-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="38be1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="38be1-107">Parameters</span></span>

 <span data-ttu-id="38be1-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="38be1-108">_ppStore_</span></span>
  
> <span data-ttu-id="38be1-109">remarquer Pointeur vers un pointeur vers la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="38be1-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38be1-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="38be1-110">Return value</span></span>

<span data-ttu-id="38be1-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="38be1-111">S_OK</span></span> 
  
> <span data-ttu-id="38be1-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="38be1-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="38be1-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="38be1-113">S_FALSE</span></span> 
  
> <span data-ttu-id="38be1-114">Il n'existe pas de magasin qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="38be1-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38be1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="38be1-115">Remarks</span></span>

<span data-ttu-id="38be1-116">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="38be1-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="38be1-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38be1-117">MFCMAPI reference</span></span>

<span data-ttu-id="38be1-118">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="38be1-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38be1-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="38be1-119">**File**</span></span>|<span data-ttu-id="38be1-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="38be1-120">**Function**</span></span>|<span data-ttu-id="38be1-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="38be1-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38be1-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="38be1-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="38be1-123">CMyMAPIFormViewer:: GetStore</span><span class="sxs-lookup"><span data-stu-id="38be1-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="38be1-124">MFCMAPI utilise la méthode **IMAPIMessageSite:: GetStore** pour obtenir le pointeur actuellement en cache sur la Banque spécifiée, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="38be1-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38be1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38be1-125">See also</span></span>



[<span data-ttu-id="38be1-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38be1-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="38be1-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="38be1-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="38be1-128">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="38be1-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

