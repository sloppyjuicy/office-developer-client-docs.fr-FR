---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2d4100d9bcd1b086747d742d9636c4bf7a39f50b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321370"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="41490-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="41490-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="41490-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41490-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41490-105">Renvoie une interface du gestionnaire de formulaires, qu'un serveur de formulaires peut utiliser pour ouvrir un autre serveur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="41490-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="41490-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="41490-106">Parameters</span></span>

 <span data-ttu-id="41490-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="41490-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="41490-108">remarquer Pointeur vers un pointeur vers l'interface du gestionnaire de formulaires renvoyée.</span><span class="sxs-lookup"><span data-stu-id="41490-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="41490-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="41490-109">Return value</span></span>

<span data-ttu-id="41490-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="41490-110">S_OK</span></span> 
  
> <span data-ttu-id="41490-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="41490-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41490-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="41490-112">Remarks</span></span>

<span data-ttu-id="41490-113">Pour obtenir la liste des interfaces liées aux serveurs de formulaires, voir [MAPI Form interfaces](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="41490-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="41490-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="41490-114">MFCMAPI reference</span></span>

<span data-ttu-id="41490-115">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="41490-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="41490-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="41490-116">**File**</span></span>|<span data-ttu-id="41490-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="41490-117">**Function**</span></span>|<span data-ttu-id="41490-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="41490-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="41490-119">MyMAPIFormViewer. cpp</span><span class="sxs-lookup"><span data-stu-id="41490-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="41490-120">CMyMAPIFormViewer:: GetFormManager</span><span class="sxs-lookup"><span data-stu-id="41490-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="41490-121">MFCMAPI utilise la méthode **IMAPIMessageSite:: GetFormManager** pour appeler [MAPIOpenFormMgr](mapiopenformmgr.md) et renvoyer les résultats de cet appel.</span><span class="sxs-lookup"><span data-stu-id="41490-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41490-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="41490-122">See also</span></span>



[<span data-ttu-id="41490-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="41490-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="41490-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="41490-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="41490-125">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="41490-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="41490-126">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="41490-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

