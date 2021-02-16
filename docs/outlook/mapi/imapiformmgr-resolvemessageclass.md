---
title: IMAPIFormMgrResolveMessageClass
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMessageClass
api_type:
- COM
ms.assetid: c2af7516-3a97-4422-874d-b1e3a0d4f316
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: e99cff77fe872018722395c53c605e4d8fabfdde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426393"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="34cec-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="34cec-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="34cec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34cec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34cec-105">Résout une classe de message dans son formulaire dans un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="34cec-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="34cec-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34cec-106">Parameters</span></span>

 <span data-ttu-id="34cec-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="34cec-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="34cec-108">[in] Chaîne qui nomme la classe de message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="34cec-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="34cec-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="34cec-109">_ulFlags_</span></span>
  
> <span data-ttu-id="34cec-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue.</span><span class="sxs-lookup"><span data-stu-id="34cec-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="34cec-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="34cec-111">The following flag can be set:</span></span>
    
<span data-ttu-id="34cec-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="34cec-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="34cec-113">Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.</span><span class="sxs-lookup"><span data-stu-id="34cec-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="34cec-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="34cec-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="34cec-115">[in] Pointeur vers le dossier qui contient le message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="34cec-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="34cec-116">Le  _paramètre pFolderFocus_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="34cec-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="34cec-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="34cec-117">_ppResult_</span></span>
  
> <span data-ttu-id="34cec-118">[out] Pointeur vers un pointeur vers un objet d’informations de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="34cec-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34cec-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="34cec-119">Return value</span></span>

<span data-ttu-id="34cec-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="34cec-120">S_OK</span></span> 
  
> <span data-ttu-id="34cec-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="34cec-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="34cec-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="34cec-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="34cec-123">La classe de message transmise dans le paramètre  _szMsgClass_ ne correspond à la classe de message pour aucun formulaire de la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="34cec-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="34cec-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="34cec-124">Remarks</span></span>

<span data-ttu-id="34cec-125">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::ResolveMessageClass** pour résoudre une classe de message dans son formulaire dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="34cec-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="34cec-126">L’objet informations du formulaire renvoyé dans le  _paramètre ppResult_ fournit un accès supplémentaire aux propriétés du formulaire qui possède la classe de message donnée.</span><span class="sxs-lookup"><span data-stu-id="34cec-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="34cec-127">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="34cec-127">Notes to callers</span></span>

<span data-ttu-id="34cec-128">Pour résoudre une classe de message en formulaire, une visionneuse de formulaire transmet le nom de la classe de message à résoudre, tel que « `IPM.HelpDesk.Software` ».</span><span class="sxs-lookup"><span data-stu-id="34cec-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="34cec-129">Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message lorsqu’un serveur de formulaires correspondant exactement n’est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="34cec-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="34cec-130">Si le  _paramètre pFolderFocus_ est NULL, le processus de résolution de classe de message ne recherche pas un conteneur de dossiers.</span><span class="sxs-lookup"><span data-stu-id="34cec-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="34cec-131">L’ordre des conteneurs recherchés dépend de l’implémentation du fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="34cec-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="34cec-132">Le fournisseur de bibliothèque de formulaires par défaut recherche d’abord le conteneur local, puis le conteneur de dossiers pour le dossier transmis, le conteneur de formulaire personnel et, enfin, le conteneur d’organisation.</span><span class="sxs-lookup"><span data-stu-id="34cec-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="34cec-133">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="34cec-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="34cec-134">L’identificateur de classe pour la classe de message résolue est renvoyé dans le cadre de l’objet d’informations du formulaire.</span><span class="sxs-lookup"><span data-stu-id="34cec-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="34cec-135">Une visionneuse de formulaire ne doit pas fonctionner sur l’hypothèse que l’identificateur de classe existe dans la bibliothèque OLE tant que la visionneuse n’a pas appelé la méthode [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) ou [IMAPIFormMgr::CreateForm.](imapiformmgr-createform.md)</span><span class="sxs-lookup"><span data-stu-id="34cec-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="34cec-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34cec-136">See also</span></span>



[<span data-ttu-id="34cec-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="34cec-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="34cec-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="34cec-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="34cec-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="34cec-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="34cec-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34cec-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

