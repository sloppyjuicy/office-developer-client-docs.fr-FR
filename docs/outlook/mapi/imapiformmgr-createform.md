---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419848"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="6d9f2-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="6d9f2-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="6d9f2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d9f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d9f2-105">Ouvre un formulaire pour créer un message basé sur la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="6d9f2-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6d9f2-106">Parameters</span></span>

 <span data-ttu-id="6d9f2-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6d9f2-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="6d9f2-108">[in] Poignée vers la fenêtre parente de l’indicateur de progression qui s’affiche pendant l’ouverture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="6d9f2-109">Le _paramètre ulUIParam_ est ignoré, sauf si l’MAPI_DIALOG est définie dans le _paramètre ulFlags._</span><span class="sxs-lookup"><span data-stu-id="6d9f2-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6d9f2-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6d9f2-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6d9f2-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="6d9f2-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="6d9f2-112">The following flag can be set:</span></span>
    
<span data-ttu-id="6d9f2-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6d9f2-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="6d9f2-114">Affiche une interface utilisateur pour fournir un état ou invite l’utilisateur à fournir plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="6d9f2-115">Si cet indicateur n’est pas définie, aucune interface utilisateur n’est affichée.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="6d9f2-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="6d9f2-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="6d9f2-117">[in] Pointeur vers l’objet d’informations du formulaire utilisé pour ouvrir le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="6d9f2-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="6d9f2-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="6d9f2-119">[in] Pointeur vers l’identificateur d’interface (IID) de l’interface à retourner pour l’objet de formulaire qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="6d9f2-120">Le  _paramètre refiidToAsk_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="6d9f2-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="6d9f2-121">_ppvObj_</span></span>
  
> <span data-ttu-id="6d9f2-122">[out] Pointeur vers un pointeur vers l’interface renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6d9f2-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6d9f2-123">Return value</span></span>

<span data-ttu-id="6d9f2-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6d9f2-124">S_OK</span></span> 
  
> <span data-ttu-id="6d9f2-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6d9f2-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="6d9f2-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="6d9f2-127">L’interface demandée n’est pas prise en charge par l’objet formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6d9f2-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d9f2-128">Remarks</span></span>

<span data-ttu-id="6d9f2-129">Les visionneuses de formulaire appellent la méthode **IMAPIFormMgr::CreateForm** pour ouvrir un formulaire afin de créer un message basé sur la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="6d9f2-130">**CreateForm** ouvre le formulaire en créant une instance du serveur de formulaire pour ce formulaire, comme décrit dans l’objet d’informations du formulaire donné.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="6d9f2-131">Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) pour télécharger le code du serveur de formulaire sur le disque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="6d9f2-132">Le  _paramètre pfrminfoToActivate_ doit pointer vers un objet d’informations de formulaire qui a été correctement résolu.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="6d9f2-133">Une fois le formulaire ouvert, la visionneuse de formulaire appelant doit configurer un message à l’aide de l’interface [IPersistMessage](ipersistmessageiunknown.md) et peut éventuellement configurer un contexte d’affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="6d9f2-134">Pour plus d’informations, voir [Lancement d’un serveur de formulaires.](launching-a-form-server.md)</span><span class="sxs-lookup"><span data-stu-id="6d9f2-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6d9f2-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6d9f2-135">MFCMAPI reference</span></span>

<span data-ttu-id="6d9f2-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6d9f2-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6d9f2-137">**File**</span></span>|<span data-ttu-id="6d9f2-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6d9f2-138">**Function**</span></span>|<span data-ttu-id="6d9f2-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6d9f2-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6d9f2-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="6d9f2-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="6d9f2-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="6d9f2-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="6d9f2-142">MFCMAPI utilise la **méthode IMAPIFormMgr::CreateForm** pour créer un formulaire avant de l’afficher.</span><span class="sxs-lookup"><span data-stu-id="6d9f2-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6d9f2-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6d9f2-143">See also</span></span>



[<span data-ttu-id="6d9f2-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="6d9f2-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="6d9f2-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6d9f2-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="6d9f2-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6d9f2-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="6d9f2-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6d9f2-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6d9f2-148">Lancement d’un serveur de formulaires</span><span class="sxs-lookup"><span data-stu-id="6d9f2-148">Launching a Form Server</span></span>](launching-a-form-server.md)

