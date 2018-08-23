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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586164"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="18633-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="18633-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="18633-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18633-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18633-105">Ouvre un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="18633-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="18633-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="18633-106">Parameters</span></span>

 <span data-ttu-id="18633-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="18633-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="18633-108">[in] Un handle vers la fenêtre parent pour l’indicateur de progression est affichée pendant que le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="18633-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="18633-109">Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="18633-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="18633-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="18633-110">_ulFlags_</span></span>
  
> <span data-ttu-id="18633-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert.</span><span class="sxs-lookup"><span data-stu-id="18633-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="18633-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="18633-112">The following flag can be set:</span></span>
    
<span data-ttu-id="18633-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="18633-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="18633-114">Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="18633-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="18633-115">Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.</span><span class="sxs-lookup"><span data-stu-id="18633-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="18633-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="18633-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="18633-117">[in] Pointeur vers l’objet d’informations de formulaire qui est utilisée pour ouvrir le formulaire.</span><span class="sxs-lookup"><span data-stu-id="18633-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="18633-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="18633-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="18633-119">[in] Pointeur vers l’identificateur d’interface (IID) pour l’interface à renvoyer à partir de l’objet de formulaire qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="18633-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="18633-120">Le paramètre _refiidToAsk_ ne doit pas être NULL.</span><span class="sxs-lookup"><span data-stu-id="18633-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="18633-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="18633-121">_ppvObj_</span></span>
  
> <span data-ttu-id="18633-122">[out] Pointeur vers un pointeur vers l’interface retournée.</span><span class="sxs-lookup"><span data-stu-id="18633-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="18633-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="18633-123">Return value</span></span>

<span data-ttu-id="18633-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="18633-124">S_OK</span></span> 
  
> <span data-ttu-id="18633-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="18633-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="18633-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="18633-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="18633-127">L’interface demandée n’est pas pris en charge par l’objet de formulaire.</span><span class="sxs-lookup"><span data-stu-id="18633-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18633-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="18633-128">Remarks</span></span>

<span data-ttu-id="18633-129">Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::CreateForm** pour ouvrir un formulaire pour créer un nouveau message en fonction de la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="18633-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="18633-130">**CreateForm** ouvre le formulaire en créant une instance du serveur de formulaire pour ce formulaire comme décrit dans l’objet d’informations de formulaire donné.</span><span class="sxs-lookup"><span data-stu-id="18633-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="18633-131">Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) pour télécharger le code du formulaire sur le disque de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="18633-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="18633-132">Le paramètre _pfrminfoToActivate_ doit pointer sur un objet d’informations de formulaire qui a été correctement résolu.</span><span class="sxs-lookup"><span data-stu-id="18633-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="18633-133">Une fois que le formulaire a été ouvert, la visionneuse de formulaire appelant doit configurer un message à l’aide de l’interface [IPersistMessage](ipersistmessageiunknown.md) et permettre éventuellement configurer un contexte de vue pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="18633-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="18633-134">Pour plus d’informations, voir [lancement d’un serveur de formulaire](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="18633-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="18633-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="18633-135">MFCMAPI reference</span></span>

<span data-ttu-id="18633-136">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="18633-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="18633-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="18633-137">**File**</span></span>|<span data-ttu-id="18633-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="18633-138">**Function**</span></span>|<span data-ttu-id="18633-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="18633-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="18633-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="18633-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="18633-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="18633-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="18633-142">MFCMAPI utilise la méthode **IMAPIFormMgr::CreateForm** pour créer un formulaire avant de les afficher.</span><span class="sxs-lookup"><span data-stu-id="18633-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="18633-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18633-143">See also</span></span>



[<span data-ttu-id="18633-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="18633-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="18633-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18633-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="18633-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18633-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="18633-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="18633-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="18633-148">Lancement d’un serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="18633-148">Launching a Form Server</span></span>](launching-a-form-server.md)

