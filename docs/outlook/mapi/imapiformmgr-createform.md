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
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="f77a3-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="f77a3-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="f77a3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f77a3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f77a3-105">Ouvre un formulaire pour créer un message basé sur la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="f77a3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f77a3-106">Parameters</span></span>

 <span data-ttu-id="f77a3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f77a3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f77a3-108">dans Handle de la fenêtre parente de l'indicateur de progression qui est affiché pendant l'ouverture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="f77a3-109">Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="f77a3-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="f77a3-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f77a3-110">_ulFlags_</span></span>
  
> <span data-ttu-id="f77a3-111">dans Masque de des indicateurs qui contrôle le mode d'ouverture du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="f77a3-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="f77a3-112">The following flag can be set:</span></span>
    
<span data-ttu-id="f77a3-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="f77a3-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="f77a3-114">Affiche une interface utilisateur pour fournir l'État ou inviter l'utilisateur à fournir des informations supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="f77a3-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="f77a3-115">Si cet indicateur n'est pas défini, aucune interface utilisateur n'est affichée.</span><span class="sxs-lookup"><span data-stu-id="f77a3-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="f77a3-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="f77a3-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="f77a3-117">dans Pointeur vers l'objet d'informations de formulaire qui est utilisé pour ouvrir le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="f77a3-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="f77a3-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="f77a3-119">dans Pointeur vers l'identificateur d'interface (IID) de l'interface à renvoyer pour l'objet Form qui a été créé.</span><span class="sxs-lookup"><span data-stu-id="f77a3-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="f77a3-120">Le paramètre _refiidToAsk_ ne doit pas être null.</span><span class="sxs-lookup"><span data-stu-id="f77a3-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="f77a3-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="f77a3-121">_ppvObj_</span></span>
  
> <span data-ttu-id="f77a3-122">remarquer Pointeur vers un pointeur vers l'interface renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f77a3-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f77a3-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f77a3-123">Return value</span></span>

<span data-ttu-id="f77a3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="f77a3-124">S_OK</span></span> 
  
> <span data-ttu-id="f77a3-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="f77a3-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f77a3-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="f77a3-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="f77a3-127">L'interface demandée n'est pas prise en charge par l'objet Form.</span><span class="sxs-lookup"><span data-stu-id="f77a3-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f77a3-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="f77a3-128">Remarks</span></span>

<span data-ttu-id="f77a3-129">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: CreateForm** pour ouvrir un formulaire afin de créer un nouveau message basé sur la classe de message du formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="f77a3-130">**CreateForm** ouvre le formulaire en créant une instance du serveur de formulaires pour ce formulaire, comme décrit dans l'objet d'information de formulaire donné.</span><span class="sxs-lookup"><span data-stu-id="f77a3-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="f77a3-131">Si nécessaire, **CreateForm** appelle la méthode [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) pour télécharger le code du serveur de formulaire sur le disque de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f77a3-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="f77a3-132">Le paramètre _pfrminfoToActivate_ doit pointer vers un objet d'informations de formulaire qui a été résolu correctement.</span><span class="sxs-lookup"><span data-stu-id="f77a3-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="f77a3-133">Une fois le formulaire ouvert, l'afficheur de formulaire appelant doit configurer un message à l'aide de l'interface [IPersistMessage](ipersistmessageiunknown.md) et éventuellement configurer un contexte d'affichage pour le formulaire.</span><span class="sxs-lookup"><span data-stu-id="f77a3-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="f77a3-134">Pour plus d'informations, reportez-vous à [la rubrique lancement d'un serveur de formulaires](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="f77a3-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f77a3-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="f77a3-135">MFCMAPI reference</span></span>

<span data-ttu-id="f77a3-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f77a3-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f77a3-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="f77a3-137">**File**</span></span>|<span data-ttu-id="f77a3-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="f77a3-138">**Function**</span></span>|<span data-ttu-id="f77a3-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="f77a3-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f77a3-140">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="f77a3-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f77a3-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="f77a3-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="f77a3-142">MFCMAPI utilise la méthode **IMAPIFormMgr:: CreateForm** pour créer un formulaire avant de l'afficher.</span><span class="sxs-lookup"><span data-stu-id="f77a3-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f77a3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f77a3-143">See also</span></span>



[<span data-ttu-id="f77a3-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="f77a3-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="f77a3-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f77a3-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="f77a3-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f77a3-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="f77a3-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="f77a3-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="f77a3-148">Lancement d'un serveur de formulaire</span><span class="sxs-lookup"><span data-stu-id="f77a3-148">Launching a Form Server</span></span>](launching-a-form-server.md)

