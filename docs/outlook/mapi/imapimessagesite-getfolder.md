---
title: IMAPIMessageSiteGetFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFolder
api_type:
- COM
ms.assetid: 9f4b4147-ed98-47cb-a799-ddf028f8e826
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 24461099877af683109c8627eacd22a657d6e156
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430566"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="5353c-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="5353c-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="5353c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5353c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5353c-105">Renvoie le dossier dans lequel le message actif a été créé ou ouvert, si ce dossier existe.</span><span class="sxs-lookup"><span data-stu-id="5353c-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="5353c-106">Cette méthode renvoie NULL dans le paramètre _ppFolder_ pour les messages incorporés, qui ne sont pas stockés directement dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="5353c-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="5353c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5353c-107">Parameters</span></span>

 <span data-ttu-id="5353c-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="5353c-108">_ppFolder_</span></span>
  
> <span data-ttu-id="5353c-109">remarquer Pointeur vers un pointeur vers le dossier renvoyé.</span><span class="sxs-lookup"><span data-stu-id="5353c-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5353c-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5353c-110">Return value</span></span>

<span data-ttu-id="5353c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5353c-111">S_OK</span></span> 
  
> <span data-ttu-id="5353c-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="5353c-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="5353c-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="5353c-113">S_FALSE</span></span> 
  
> <span data-ttu-id="5353c-114">Il n'existe aucun dossier pour le message.</span><span class="sxs-lookup"><span data-stu-id="5353c-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5353c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5353c-115">Remarks</span></span>

<span data-ttu-id="5353c-116">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="5353c-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5353c-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5353c-117">MFCMAPI reference</span></span>

<span data-ttu-id="5353c-118">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5353c-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5353c-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5353c-119">**File**</span></span>|<span data-ttu-id="5353c-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5353c-120">**Function**</span></span>|<span data-ttu-id="5353c-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5353c-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5353c-122">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="5353c-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="5353c-123">CMyMAPIFormViewer:: GetFolder</span><span class="sxs-lookup"><span data-stu-id="5353c-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="5353c-124">MFCMAPI utilise la méthode **IMAPIMessageSite:: GetFolder** pour renvoyer le pointeur actuellement en cache vers le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="5353c-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5353c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5353c-125">See also</span></span>



[<span data-ttu-id="5353c-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5353c-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="5353c-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5353c-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="5353c-128">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="5353c-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

