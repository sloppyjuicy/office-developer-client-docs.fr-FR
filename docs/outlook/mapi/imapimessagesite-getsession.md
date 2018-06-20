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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783844"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="c9a56-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="c9a56-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="c9a56-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9a56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9a56-105">Renvoie la session MAPI dans lequel le message en cours a été créé ou ouvert.</span><span class="sxs-lookup"><span data-stu-id="c9a56-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="c9a56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9a56-106">Parameters</span></span>

 <span data-ttu-id="c9a56-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="c9a56-107">_ppSession_</span></span>
  
> <span data-ttu-id="c9a56-108">[out] Pointeur vers un pointeur vers l’objet de session retourné.</span><span class="sxs-lookup"><span data-stu-id="c9a56-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c9a56-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c9a56-109">Return value</span></span>

<span data-ttu-id="c9a56-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c9a56-110">S_OK</span></span> 
  
> <span data-ttu-id="c9a56-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="c9a56-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="c9a56-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c9a56-112">S_FALSE</span></span> 
  
> <span data-ttu-id="c9a56-113">Aucune session n’existe pour le message en cours.</span><span class="sxs-lookup"><span data-stu-id="c9a56-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9a56-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c9a56-114">Remarks</span></span>

<span data-ttu-id="c9a56-115">Pour obtenir la liste des interfaces qui sont liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="c9a56-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c9a56-116">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c9a56-116">MFCMAPI reference</span></span>

<span data-ttu-id="c9a56-117">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c9a56-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c9a56-118">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="c9a56-118">**File**</span></span>|<span data-ttu-id="c9a56-119">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="c9a56-119">**Function**</span></span>|<span data-ttu-id="c9a56-120">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="c9a56-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c9a56-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c9a56-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c9a56-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="c9a56-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="c9a56-123">MFCMAPI utilise la méthode **IMAPIMessageSite::GetSession** pour renvoyer le pointeur de la session actuellement mis en cache, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="c9a56-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9a56-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9a56-124">See also</span></span>



[<span data-ttu-id="c9a56-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c9a56-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="c9a56-126">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="c9a56-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

