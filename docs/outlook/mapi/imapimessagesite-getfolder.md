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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ea95ea4efbbf50e5551a27eb81fe5d5ab3b73948
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783825"
---
# <a name="imapimessagesitegetfolder"></a><span data-ttu-id="e9933-103">IMAPIMessageSite::GetFolder</span><span class="sxs-lookup"><span data-stu-id="e9933-103">IMAPIMessageSite::GetFolder</span></span>

  
  
<span data-ttu-id="e9933-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9933-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9933-105">Renvoie le dossier dans lequel le message en cours a été créé ou ouvert, si un tel dossier existe.</span><span class="sxs-lookup"><span data-stu-id="e9933-105">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span> <span data-ttu-id="e9933-106">Cette méthode renvoie la valeur NULL dans le paramètre _ppFolder_ pour les messages incorporés, qui ne sont pas stockées directement dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="e9933-106">This method returns NULL in the  _ppFolder_ parameter for embedded messages, which are not stored directly in a folder.</span></span> 
  
```cpp
HRESULT GetFolder(
  LPMAPIFOLDER FAR * ppFolder
);
```

## <a name="parameters"></a><span data-ttu-id="e9933-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9933-107">Parameters</span></span>

 <span data-ttu-id="e9933-108">_ppFolder_</span><span class="sxs-lookup"><span data-stu-id="e9933-108">_ppFolder_</span></span>
  
> <span data-ttu-id="e9933-109">[out] Pointeur vers un pointeur vers le dossier renvoyé.</span><span class="sxs-lookup"><span data-stu-id="e9933-109">[out] A pointer to a pointer to the returned folder.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e9933-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e9933-110">Return value</span></span>

<span data-ttu-id="e9933-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="e9933-111">S_OK</span></span> 
  
> <span data-ttu-id="e9933-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="e9933-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="e9933-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="e9933-113">S_FALSE</span></span> 
  
> <span data-ttu-id="e9933-114">Aucun dossier n’existe pour le message.</span><span class="sxs-lookup"><span data-stu-id="e9933-114">No folder exists for the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9933-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e9933-115">Remarks</span></span>

<span data-ttu-id="e9933-116">Pour obtenir la liste des interfaces qui sont liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="e9933-116">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e9933-117">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e9933-117">MFCMAPI reference</span></span>

<span data-ttu-id="e9933-118">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e9933-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e9933-119">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="e9933-119">**File**</span></span>|<span data-ttu-id="e9933-120">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="e9933-120">**Function**</span></span>|<span data-ttu-id="e9933-121">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="e9933-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e9933-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="e9933-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="e9933-123">CMyMAPIFormViewer::GetFolder</span><span class="sxs-lookup"><span data-stu-id="e9933-123">CMyMAPIFormViewer::GetFolder</span></span>  <br/> |<span data-ttu-id="e9933-124">MFCMAPI utilise la méthode **IMAPIMessageSite::GetFolder** pour renvoyer le pointeur actuellement mis en cache dans le dossier spécifié.</span><span class="sxs-lookup"><span data-stu-id="e9933-124">MFCMAPI uses the **IMAPIMessageSite::GetFolder** method to return the currently cached pointer to the specified folder.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9933-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9933-125">See also</span></span>



[<span data-ttu-id="e9933-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9933-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="e9933-127">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="e9933-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e9933-128">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="e9933-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

