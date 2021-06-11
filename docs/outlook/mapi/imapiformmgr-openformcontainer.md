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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321636"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="dde79-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="dde79-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="dde79-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dde79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dde79-105">Ouvre une interface [IMAPIFormContainer](imapiformcontaineriunknown.md) pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="dde79-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="dde79-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="dde79-106">Parameters</span></span>

 <span data-ttu-id="dde79-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="dde79-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="dde79-108">[in] Une éumération HFRMREG qui indique la bibliothèque de formulaires à ouvrir (autrement dit, le conteneur de formulaire à ouvrir).</span><span class="sxs-lookup"><span data-stu-id="dde79-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="dde79-109">Une éumération HFRMREG est une éumération spécifique à un fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="dde79-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="dde79-110">Les valeurs HFRMREG possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="dde79-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="dde79-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="dde79-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="dde79-112">Conteneur de formulaires pratique.</span><span class="sxs-lookup"><span data-stu-id="dde79-112">A convenient form container.</span></span>
    
<span data-ttu-id="dde79-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="dde79-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="dde79-114">Conteneur de dossiers.</span><span class="sxs-lookup"><span data-stu-id="dde79-114">A folder container.</span></span> 
    
<span data-ttu-id="dde79-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="dde79-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="dde79-116">Conteneur de la magasin de messages par défaut.</span><span class="sxs-lookup"><span data-stu-id="dde79-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="dde79-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="dde79-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="dde79-118">Conteneur de formulaire local.</span><span class="sxs-lookup"><span data-stu-id="dde79-118">A local form container.</span></span> 
    
 <span data-ttu-id="dde79-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="dde79-119">_lpunk_</span></span>
  
> <span data-ttu-id="dde79-120">[in] Pointeur vers l’objet pour lequel l’interface est ouverte.</span><span class="sxs-lookup"><span data-stu-id="dde79-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="dde79-121">Le  _paramètre lpunk_ doit être **null,** sauf si la valeur du paramètre  _hfrmreg_ nécessite un pointeur d’objet.</span><span class="sxs-lookup"><span data-stu-id="dde79-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="dde79-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="dde79-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="dde79-123">[out] Pointeur vers un pointeur vers l’objet conteneur de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="dde79-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dde79-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dde79-124">Return value</span></span>

<span data-ttu-id="dde79-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="dde79-125">S_OK</span></span> 
  
> <span data-ttu-id="dde79-126">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dde79-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="dde79-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="dde79-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="dde79-128">L’objet pointé par  _lpunk_ ne prend pas en charge l’interface requise.</span><span class="sxs-lookup"><span data-stu-id="dde79-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="dde79-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="dde79-129">Remarks</span></span>

<span data-ttu-id="dde79-130">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::OpenFormContainer** pour ouvrir une interface **IMAPIFormContainer** pour un conteneur de formulaire spécifique.</span><span class="sxs-lookup"><span data-stu-id="dde79-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="dde79-131">Cette interface peut ensuite être utilisée pour installer et supprimer des formulaires dans un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="dde79-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dde79-132">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dde79-132">Notes to callers</span></span>

<span data-ttu-id="dde79-133">Si la valeur dans _hfrmreg_ est HFRMREG_FOLDER, l’identificateur d’interface utilisé dans _lpunk_ doit être non **null** et autoriser les appels de méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) à une interface [IMAPIFolder.](imapifolderimapicontainer.md)</span><span class="sxs-lookup"><span data-stu-id="dde79-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="dde79-134">Pour ouvrir le conteneur de formulaires local, vous devez utiliser un appel à la méthode **OpenFormContainer** ou à la fonction [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) ; vous ne pouvez pas utiliser [la méthode IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) pour permettre à l’utilisateur de sélectionner le conteneur de formulaire local.</span><span class="sxs-lookup"><span data-stu-id="dde79-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dde79-135">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dde79-135">MFCMAPI reference</span></span>

<span data-ttu-id="dde79-136">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dde79-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dde79-137">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="dde79-137">**File**</span></span>|<span data-ttu-id="dde79-138">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="dde79-138">**Function**</span></span>|<span data-ttu-id="dde79-139">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="dde79-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dde79-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dde79-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="dde79-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="dde79-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="dde79-142">MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire afin que le contenu du conteneur puisse être rendu.</span><span class="sxs-lookup"><span data-stu-id="dde79-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="dde79-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="dde79-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="dde79-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="dde79-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="dde79-145">MFCMAPI utilise la méthode **IMAPIFormMgr::OpenFormContainer** pour récupérer un conteneur de formulaire pour un dossier afin que le contenu du conteneur puisse être rendu.</span><span class="sxs-lookup"><span data-stu-id="dde79-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dde79-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dde79-146">See also</span></span>



[<span data-ttu-id="dde79-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="dde79-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="dde79-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="dde79-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="dde79-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="dde79-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="dde79-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dde79-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="dde79-151">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="dde79-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

