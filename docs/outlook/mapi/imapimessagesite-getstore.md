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
ms.openlocfilehash: 1f4e6c49ca1c537f78ccce708c4a0b00f81ad7e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567929"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="87552-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="87552-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="87552-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87552-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87552-105">Renvoie la banque de messages qui contient le message en cours, si une banque de ce type existe.</span><span class="sxs-lookup"><span data-stu-id="87552-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="87552-106">Cette méthode retourne NULL dans le paramètre _ppStore_ pour les messages incorporés, qui sont stockés dans un autre message au lieu de directement dans une banque de messages.</span><span class="sxs-lookup"><span data-stu-id="87552-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="87552-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="87552-107">Parameters</span></span>

 <span data-ttu-id="87552-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="87552-108">_ppStore_</span></span>
  
> <span data-ttu-id="87552-109">[out] Pointeur vers un pointeur vers la banque de messages.</span><span class="sxs-lookup"><span data-stu-id="87552-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87552-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="87552-110">Return value</span></span>

<span data-ttu-id="87552-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="87552-111">S_OK</span></span> 
  
> <span data-ttu-id="87552-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="87552-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="87552-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="87552-113">S_FALSE</span></span> 
  
> <span data-ttu-id="87552-114">Il n’existe aucune banque qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="87552-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="87552-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="87552-115">Remarks</span></span>

<span data-ttu-id="87552-116">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="87552-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87552-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87552-117">MFCMAPI reference</span></span>

<span data-ttu-id="87552-118">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="87552-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87552-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="87552-119">**File**</span></span>|<span data-ttu-id="87552-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="87552-120">**Function**</span></span>|<span data-ttu-id="87552-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="87552-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87552-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="87552-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="87552-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="87552-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="87552-124">MFCMAPI utilise la méthode **IMAPIMessageSite::GetStore** pour obtenir le pointeur actuellement mis en cache dans le magasin spécifié, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="87552-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87552-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87552-125">See also</span></span>



[<span data-ttu-id="87552-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87552-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="87552-127">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="87552-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="87552-128">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="87552-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

