---
title: IMAPIFormContainerResolveMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.ResolveMessageClass
api_type:
- COM
ms.assetid: 9ce13f11-5787-4ea5-a84f-b1e3824529ee
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: db4b8d99c960deb3de3d228b2bf9549738501bcc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576280"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="09dcd-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="09dcd-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="09dcd-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09dcd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09dcd-105">Résout une classe de message à sa forme dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="09dcd-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="09dcd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09dcd-106">Parameters</span></span>

 <span data-ttu-id="09dcd-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="09dcd-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="09dcd-108">[in] Chaîne qui nomme la classe de message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="09dcd-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="09dcd-109">Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.</span><span class="sxs-lookup"><span data-stu-id="09dcd-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="09dcd-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09dcd-110">_ulFlags_</span></span>
  
> <span data-ttu-id="09dcd-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue.</span><span class="sxs-lookup"><span data-stu-id="09dcd-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="09dcd-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="09dcd-112">The following flag can be set:</span></span>
    
<span data-ttu-id="09dcd-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="09dcd-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="09dcd-114">Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.</span><span class="sxs-lookup"><span data-stu-id="09dcd-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="09dcd-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="09dcd-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="09dcd-116">[out] Pointeur vers un pointeur vers l’objet d’informations de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="09dcd-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09dcd-117">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="09dcd-117">Return value</span></span>

<span data-ttu-id="09dcd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="09dcd-118">S_OK</span></span> 
  
> <span data-ttu-id="09dcd-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="09dcd-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="09dcd-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="09dcd-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="09dcd-121">La classe de message transmise dans le paramètre _szMessageClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans le conteneur du formulaire.</span><span class="sxs-lookup"><span data-stu-id="09dcd-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09dcd-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="09dcd-122">Remarks</span></span>

<span data-ttu-id="09dcd-123">Applications clientes appellent la méthode **IMAPIFormContainer::ResolveMessageClass** pour résoudre une classe de message à un formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="09dcd-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="09dcd-124">L’écran informations objet renvoyé dans le paramètre _ppforminfo_ fournit plus accès aux propriétés du formulaire avec la classe de message donné.</span><span class="sxs-lookup"><span data-stu-id="09dcd-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="09dcd-125">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="09dcd-125">Notes to callers</span></span>

<span data-ttu-id="09dcd-126">Pour résoudre une classe de message à un formulaire, passez le nom de la classe de message pour être résolu (par exemple, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="09dcd-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="09dcd-127">Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="09dcd-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="09dcd-128">L’identificateur de classe pour la classe de message résolu est renvoyée dans le cadre de l’objet d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="09dcd-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="09dcd-129">Ne pensez pas que l’identificateur de classe existe dans la bibliothèque OLE jusqu'à après l’appel de méthode le [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="09dcd-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09dcd-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="09dcd-130">MFCMAPI reference</span></span>

<span data-ttu-id="09dcd-131">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="09dcd-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09dcd-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="09dcd-132">**File**</span></span>|<span data-ttu-id="09dcd-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="09dcd-133">**Function**</span></span>|<span data-ttu-id="09dcd-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="09dcd-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09dcd-135">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="09dcd-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="09dcd-136">CFormContainerDlg::OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="09dcd-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="09dcd-137">MFCMAPI utilise la méthode **IMAPIFormContainer::ResolveMessageClass** pour localiser un formulaire qui est associé à une classe de message.</span><span class="sxs-lookup"><span data-stu-id="09dcd-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09dcd-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09dcd-138">See also</span></span>



[<span data-ttu-id="09dcd-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09dcd-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="09dcd-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="09dcd-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="09dcd-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="09dcd-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="09dcd-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09dcd-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

