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
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783848"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="a2d9f-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="a2d9f-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="a2d9f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2d9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2d9f-105">Renvoie une interface du Gestionnaire de formulaire un serveur de formulaire peut utiliser pour ouvrir un autre serveur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="a2d9f-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="a2d9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2d9f-106">Parameters</span></span>

 <span data-ttu-id="a2d9f-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="a2d9f-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="a2d9f-108">[out] Pointeur vers un pointeur vers l’interface du Gestionnaire de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="a2d9f-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2d9f-109">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a2d9f-109">Return value</span></span>

<span data-ttu-id="a2d9f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a2d9f-110">S_OK</span></span> 
  
> <span data-ttu-id="a2d9f-111">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="a2d9f-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a2d9f-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2d9f-112">Remarks</span></span>

<span data-ttu-id="a2d9f-113">Pour obtenir la liste des interfaces liées aux serveurs de formulaire, voir [Interfaces de formulaire MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="a2d9f-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a2d9f-114">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="a2d9f-114">MFCMAPI reference</span></span>

<span data-ttu-id="a2d9f-115">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a2d9f-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a2d9f-116">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="a2d9f-116">**File**</span></span>|<span data-ttu-id="a2d9f-117">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="a2d9f-117">**Function**</span></span>|<span data-ttu-id="a2d9f-118">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="a2d9f-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2d9f-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="a2d9f-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="a2d9f-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="a2d9f-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="a2d9f-121">MFCMAPI utilise la méthode **IMAPIMessageSite::GetFormManager** pour appeler [MAPIOpenFormMgr](mapiopenformmgr.md) et renvoyer les résultats de cet appel.</span><span class="sxs-lookup"><span data-stu-id="a2d9f-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2d9f-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2d9f-122">See also</span></span>



[<span data-ttu-id="a2d9f-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="a2d9f-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="a2d9f-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2d9f-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="a2d9f-125">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="a2d9f-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="a2d9f-126">Interfaces de formulaire MAPI</span><span class="sxs-lookup"><span data-stu-id="a2d9f-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

