---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 64031725e06a949464e7bfabb0a2f114d325470e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783805"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="6fe3e-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6fe3e-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="6fe3e-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6fe3e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6fe3e-105">Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="6fe3e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6fe3e-106">Parameters</span></span>

 <span data-ttu-id="6fe3e-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="6fe3e-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="6fe3e-108">[in] Énumération HFRMREG indiquant la bibliothèque de formulaires pour ouvrir (autrement dit, le conteneur de formulaire à ouvrir).</span><span class="sxs-lookup"><span data-stu-id="6fe3e-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="6fe3e-109">Énumération HFRMREG est une énumération qui est spécifique à un fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="6fe3e-110">Les valeurs HFRMREG possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="6fe3e-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="6fe3e-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6fe3e-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="6fe3e-112">Un conteneur pratique de formulaire.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-112">A convenient form container.</span></span>
    
<span data-ttu-id="6fe3e-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="6fe3e-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="6fe3e-114">Un conteneur de dossiers.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-114">A folder container.</span></span> 
    
<span data-ttu-id="6fe3e-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="6fe3e-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="6fe3e-116">Conteneur pour la banque de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="6fe3e-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6fe3e-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="6fe3e-118">Conteneur formulaire local.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-118">A local form container.</span></span> 
    
 <span data-ttu-id="6fe3e-119">_lpUnk_</span><span class="sxs-lookup"><span data-stu-id="6fe3e-119">_lpunk_</span></span>
  
> <span data-ttu-id="6fe3e-120">[in] Pointeur vers l’objet pour lequel l’interface est ouvert.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="6fe3e-121">Le paramètre _lpunk_ doit être **null** , sauf si la valeur pour le paramètre _hfrmreg_ nécessite un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="6fe3e-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="6fe3e-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="6fe3e-123">[out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fe3e-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="6fe3e-124">Return value</span></span>

<span data-ttu-id="6fe3e-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fe3e-125">S_OK</span></span> 
  
> <span data-ttu-id="6fe3e-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6fe3e-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="6fe3e-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="6fe3e-128">L’objet vers lequel pointé _lpunk_ ne prend pas en charge l’interface requise.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6fe3e-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="6fe3e-129">Remarks</span></span>

<span data-ttu-id="6fe3e-130">Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="6fe3e-131">Cette interface puis peut être utilisée pour l’installation dans et la suppression de formulaires à partir d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6fe3e-132">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="6fe3e-132">Notes to callers</span></span>

<span data-ttu-id="6fe3e-133">Si la valeur de _hfrmreg_ est HFRMREG_FOLDER, l’identificateur d’interface utilisé dans _lpunk_ doit être non **null** et doit autoriser les appels de méthode [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) vers une interface [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="6fe3e-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="6fe3e-134">Pour ouvrir le conteneur de formulaire local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; Vous ne pouvez pas utiliser la méthode [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l’utilisateur sélectionner le conteneur de formulaire local.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fe3e-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6fe3e-135">MFCMAPI reference</span></span>

<span data-ttu-id="6fe3e-136">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fe3e-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="6fe3e-137">**File**</span></span>|<span data-ttu-id="6fe3e-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="6fe3e-138">**Function**</span></span>|<span data-ttu-id="6fe3e-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="6fe3e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fe3e-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6fe3e-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6fe3e-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6fe3e-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="6fe3e-142">MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire afin que le contenu du conteneur peut être affiché.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="6fe3e-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6fe3e-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="6fe3e-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6fe3e-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="6fe3e-145">MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire pour un dossier afin que le contenu du conteneur peut être affiché.</span><span class="sxs-lookup"><span data-stu-id="6fe3e-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fe3e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fe3e-146">See also</span></span>



[<span data-ttu-id="6fe3e-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="6fe3e-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="6fe3e-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="6fe3e-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="6fe3e-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6fe3e-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="6fe3e-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fe3e-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="6fe3e-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="6fe3e-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

