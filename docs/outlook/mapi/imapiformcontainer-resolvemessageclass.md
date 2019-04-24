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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c0954d6f8b14b4088ece2ac276b045b6c163ed98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342160"
---
# <a name="imapiformcontainerresolvemessageclass"></a><span data-ttu-id="ed712-103">IMAPIFormContainer::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ed712-103">IMAPIFormContainer::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="ed712-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ed712-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ed712-105">Résout une classe de message en son formulaire dans un conteneur de formulaire et renvoie un objet d'informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="ed712-105">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMessageClass,
  ULONG ulFlags,
  LPMAPIFORMINFO FAR * ppforminfo
);
```

## <a name="parameters"></a><span data-ttu-id="ed712-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ed712-106">Parameters</span></span>

 <span data-ttu-id="ed712-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="ed712-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="ed712-108">dans Chaîne qui nomme la classe de message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="ed712-108">[in] A string that names the message class being resolved.</span></span> <span data-ttu-id="ed712-109">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="ed712-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
 <span data-ttu-id="ed712-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed712-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ed712-111">dans Masque de des indicateurs qui contrôle la manière dont la classe de message est résolue.</span><span class="sxs-lookup"><span data-stu-id="ed712-111">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="ed712-112">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="ed712-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ed712-113">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="ed712-113">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="ed712-114">Seules les chaînes de classe de message correspondant à une correspondance exacte doivent être résolues.</span><span class="sxs-lookup"><span data-stu-id="ed712-114">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="ed712-115">_ppforminfo_</span><span class="sxs-lookup"><span data-stu-id="ed712-115">_ppforminfo_</span></span>
  
> <span data-ttu-id="ed712-116">remarquer Pointeur vers un pointeur vers l'objet d'informations de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="ed712-116">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ed712-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ed712-117">Return value</span></span>

<span data-ttu-id="ed712-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed712-118">S_OK</span></span> 
  
> <span data-ttu-id="ed712-119">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ed712-119">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ed712-120">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ed712-120">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ed712-121">La classe de message passée dans le paramètre _szMessageClass_ ne correspond pas à la classe de message d'un formulaire dans le conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ed712-121">The message class passed in the  _szMessageClass_ parameter does not match the message class for any form in the form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ed712-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="ed712-122">Remarks</span></span>

<span data-ttu-id="ed712-123">Les applications clientes appellent la méthode **IMAPIFormContainer:: ResolveMessageClass** pour résoudre une classe de message en un formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ed712-123">Client applications call the **IMAPIFormContainer::ResolveMessageClass** method to resolve a message class to a form within a form container.</span></span> <span data-ttu-id="ed712-124">L'objet d'informations de formulaire renvoyé dans le paramètre _ppforminfo_ fournit un accès supplémentaire aux propriétés du formulaire avec la classe de message donnée.</span><span class="sxs-lookup"><span data-stu-id="ed712-124">The form information object returned in the  _ppforminfo_ parameter provides further access to the properties of the form with the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ed712-125">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="ed712-125">Notes to callers</span></span>

<span data-ttu-id="ed712-126">Pour résoudre une classe de message en formulaire, transmettez le nom de la classe de message à résoudre (par exemple, `IPM.HelpDesk.Software`).</span><span class="sxs-lookup"><span data-stu-id="ed712-126">To resolve a message class to a form, pass in the name of the message class to be resolved (for example,  `IPM.HelpDesk.Software`).</span></span> <span data-ttu-id="ed712-127">Pour forcer la résolution de façon exacte (autrement dit, pour empêcher la résolution d'une classe de base de la classe de message), l'indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ed712-127">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="ed712-128">L'identificateur de classe pour la classe de message résolue est renvoyé dans le cadre de l'objet d'informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="ed712-128">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="ed712-129">Ne partez pas du principe que l'identificateur de classe existe dans la bibliothèque OLE jusqu'à ce que vous appeliez la méthode [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) ou [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="ed712-129">Do not assume that the class identifier exists in the OLE library until after you call either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) or [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ed712-130">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ed712-130">MFCMAPI reference</span></span>

<span data-ttu-id="ed712-131">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed712-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ed712-132">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="ed712-132">**File**</span></span>|<span data-ttu-id="ed712-133">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="ed712-133">**Function**</span></span>|<span data-ttu-id="ed712-134">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="ed712-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ed712-135">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="ed712-135">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="ed712-136">CFormContainerDlg:: OnResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="ed712-136">CFormContainerDlg::OnResolveMessageClass</span></span>  <br/> |<span data-ttu-id="ed712-137">MFCMAPI utilise la méthode **IMAPIFormContainer:: ResolveMessageClass** pour localiser un formulaire associé à une classe de message.</span><span class="sxs-lookup"><span data-stu-id="ed712-137">MFCMAPI uses the **IMAPIFormContainer::ResolveMessageClass** method to locate a form that is associated with a message class.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ed712-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed712-138">See also</span></span>



[<span data-ttu-id="ed712-139">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ed712-139">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="ed712-140">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="ed712-140">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="ed712-141">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ed712-141">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="ed712-142">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ed712-142">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)

