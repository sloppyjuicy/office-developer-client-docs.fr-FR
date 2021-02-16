---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412687"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="771cf-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="771cf-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="771cf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="771cf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="771cf-105">Renvoie la session MAPI dans laquelle le message actuel a été créé ou ouvert.</span><span class="sxs-lookup"><span data-stu-id="771cf-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="771cf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="771cf-106">Parameters</span></span>

 <span data-ttu-id="771cf-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="771cf-107">_ppSession_</span></span>
  
> <span data-ttu-id="771cf-108">[out] Pointeur vers un pointeur vers l’objet de session renvoyé.</span><span class="sxs-lookup"><span data-stu-id="771cf-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="771cf-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="771cf-109">Return value</span></span>

<span data-ttu-id="771cf-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="771cf-110">S_OK</span></span> 
  
> <span data-ttu-id="771cf-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="771cf-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="771cf-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="771cf-112">S_FALSE</span></span> 
  
> <span data-ttu-id="771cf-113">Il n’existe aucune session pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="771cf-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="771cf-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="771cf-114">Remarks</span></span>

<span data-ttu-id="771cf-115">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [INTERFACES DE FORMULAIRE MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="771cf-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="771cf-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="771cf-116">MFCMAPI reference</span></span>

<span data-ttu-id="771cf-117">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="771cf-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="771cf-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="771cf-118">**File**</span></span>|<span data-ttu-id="771cf-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="771cf-119">**Function**</span></span>|<span data-ttu-id="771cf-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="771cf-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="771cf-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="771cf-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="771cf-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="771cf-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="771cf-123">MFCMAPI utilise la méthode **IMAPIMessageSite::GetSession** pour renvoyer le pointeur de session actuellement mis en cache, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="771cf-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="771cf-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="771cf-124">See also</span></span>



[<span data-ttu-id="771cf-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="771cf-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="771cf-126">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="771cf-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

