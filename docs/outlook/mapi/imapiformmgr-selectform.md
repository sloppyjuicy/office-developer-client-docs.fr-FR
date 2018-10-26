---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 3c6242c9a926341908cb86645a8ea8586a9ca598
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586353"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="62db3-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="62db3-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="62db3-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62db3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62db3-105">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et renvoie un objet d’informations de formulaire qui décrit ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="62db3-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="62db3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62db3-106">Parameters</span></span>

 <span data-ttu-id="62db3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="62db3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="62db3-108">[in] Handle vers la fenêtre parente de la boîte de dialogue qui s’affiche.</span><span class="sxs-lookup"><span data-stu-id="62db3-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="62db3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="62db3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="62db3-110">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé.</span><span class="sxs-lookup"><span data-stu-id="62db3-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="62db3-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="62db3-111">The following flag can be set:</span></span>
    
<span data-ttu-id="62db3-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="62db3-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="62db3-113">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="62db3-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="62db3-114">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="62db3-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="62db3-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="62db3-115">_pszTitle_</span></span>
  
> <span data-ttu-id="62db3-116">[in] Pointeur vers une chaîne qui contient la légende de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="62db3-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="62db3-117">Si le paramètre _pszTitle_ est NULL, le fournisseur de bibliothèque formulaire fournit une légende par défaut.</span><span class="sxs-lookup"><span data-stu-id="62db3-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="62db3-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="62db3-118">_pfld_</span></span>
  
> <span data-ttu-id="62db3-119">[in] Pointeur vers le dossier à partir desquels sélectionner le formulaire.</span><span class="sxs-lookup"><span data-stu-id="62db3-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="62db3-120">Si le paramètre _pfld_ est NULL, le formulaire peut être sélectionné à partir du conteneur de formulaire local, personnel ou organisation.</span><span class="sxs-lookup"><span data-stu-id="62db3-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="62db3-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="62db3-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="62db3-122">[out] Pointeur vers un pointeur vers l’objet d’informations de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="62db3-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="62db3-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="62db3-123">Return value</span></span>

<span data-ttu-id="62db3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="62db3-124">S_OK</span></span> 
  
> <span data-ttu-id="62db3-125">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="62db3-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="62db3-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="62db3-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="62db3-127">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="62db3-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="62db3-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="62db3-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="62db3-129">L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="62db3-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="62db3-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="62db3-130">Remarks</span></span>

<span data-ttu-id="62db3-131">Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::SelectForm** à présent premier une boîte de dialogue qui permet à l’utilisateur de sélectionner un formulaire et puis pour récupérer un objet d’informations de formulaire qui décrit le formulaire sélectionné.</span><span class="sxs-lookup"><span data-stu-id="62db3-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="62db3-132">La boîte de dialogue contraint l’utilisateur de sélectionner un seul formulaire.</span><span class="sxs-lookup"><span data-stu-id="62db3-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="62db3-133">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="62db3-133">Notes to callers</span></span>

<span data-ttu-id="62db3-134">La boîte de dialogue **SelectForm** n’affiche que les formulaires qui ne sont pas masqués (autrement dit, désactivez les formulaires qui disposent de leurs propriétés masquées).</span><span class="sxs-lookup"><span data-stu-id="62db3-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="62db3-135">Si une visionneuse de formulaire transmet l’indicateur MAPI_UNICODE dans le paramètre _ulFlags_ , toutes les chaînes sont en Unicode.</span><span class="sxs-lookup"><span data-stu-id="62db3-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="62db3-136">Fournisseurs de bibliothèques de formulaires qui ne prennent pas en charge les chaînes Unicode doivent renvoyer MAPI_E_BAD_CHARWIDTH si MAPI_UNICODE est passé.</span><span class="sxs-lookup"><span data-stu-id="62db3-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="62db3-137">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="62db3-137">MFCMAPI reference</span></span>

<span data-ttu-id="62db3-138">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="62db3-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="62db3-139">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="62db3-139">**File**</span></span>|<span data-ttu-id="62db3-140">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="62db3-140">**Function**</span></span>|<span data-ttu-id="62db3-141">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="62db3-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62db3-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="62db3-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="62db3-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="62db3-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="62db3-144">MFCMAPI utilise la méthode **IMAPIFormMgr::SelectForm** pour sélectionner un formulaire et envoyer des informations sur le formulaire à un ou plusieurs journaux.</span><span class="sxs-lookup"><span data-stu-id="62db3-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="62db3-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62db3-145">See also</span></span>



[<span data-ttu-id="62db3-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62db3-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="62db3-147">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="62db3-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

