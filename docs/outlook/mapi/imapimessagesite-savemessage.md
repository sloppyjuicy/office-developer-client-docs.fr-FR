---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417104"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="9f3a8-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="9f3a8-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="9f3a8-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f3a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f3a8-105">Demande que le message actuel soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="9f3a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f3a8-106">Parameters</span></span>

<span data-ttu-id="9f3a8-107">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="9f3a8-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9f3a8-108">Return value</span></span>

<span data-ttu-id="9f3a8-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f3a8-109">S_OK</span></span> 
  
> <span data-ttu-id="9f3a8-110">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9f3a8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="9f3a8-111">Remarks</span></span>

<span data-ttu-id="9f3a8-112">Les formulaires appellent la méthode **IMAPIMessageSite::SaveMessage** pour demander qu’un message soit enregistré.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="9f3a8-113">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form Interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="9f3a8-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9f3a8-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9f3a8-114">MFCMAPI reference</span></span>

<span data-ttu-id="9f3a8-115">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9f3a8-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="9f3a8-116">**File**</span></span>|<span data-ttu-id="9f3a8-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="9f3a8-117">**Function**</span></span>|<span data-ttu-id="9f3a8-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="9f3a8-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9f3a8-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="9f3a8-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="9f3a8-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="9f3a8-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="9f3a8-121">MFCMAPI utilise la **méthode IMAPIMessageSite::SaveMessage** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="9f3a8-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9f3a8-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f3a8-122">See also</span></span>



[<span data-ttu-id="9f3a8-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f3a8-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="9f3a8-124">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="9f3a8-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="9f3a8-125">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="9f3a8-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

