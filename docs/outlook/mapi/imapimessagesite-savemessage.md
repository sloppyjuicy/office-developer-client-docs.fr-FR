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
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572304"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="6a83d-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="6a83d-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="6a83d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a83d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a83d-105">Demandes d’enregistrer le message en cours.</span><span class="sxs-lookup"><span data-stu-id="6a83d-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="6a83d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a83d-106">Parameters</span></span>

<span data-ttu-id="6a83d-107">Aucun.</span><span class="sxs-lookup"><span data-stu-id="6a83d-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="6a83d-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a83d-108">Return value</span></span>

<span data-ttu-id="6a83d-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a83d-109">S_OK</span></span> 
  
> <span data-ttu-id="6a83d-110">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6a83d-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6a83d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a83d-111">Remarks</span></span>

<span data-ttu-id="6a83d-112">Formulaires appeler la méthode **IMAPIMessageSite::SaveMessage** pour demander qu’un message enregistré.</span><span class="sxs-lookup"><span data-stu-id="6a83d-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="6a83d-113">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6a83d-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6a83d-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6a83d-114">MFCMAPI reference</span></span>

<span data-ttu-id="6a83d-115">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6a83d-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6a83d-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6a83d-116">**File**</span></span>|<span data-ttu-id="6a83d-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6a83d-117">**Function**</span></span>|<span data-ttu-id="6a83d-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6a83d-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6a83d-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6a83d-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6a83d-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="6a83d-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="6a83d-121">MFCMAPI utilise la méthode **IMAPIMessageSite::SaveMessage** pour enregistrer le message.</span><span class="sxs-lookup"><span data-stu-id="6a83d-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6a83d-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a83d-122">See also</span></span>



[<span data-ttu-id="6a83d-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a83d-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6a83d-124">MFCMAPI en tant qu’exemple de code</span><span class="sxs-lookup"><span data-stu-id="6a83d-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6a83d-125">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="6a83d-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

