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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: a84698ccc132c750cbd071c05160117c40e352a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783833"
---
# <a name="imapiformmgrresolvemessageclass"></a><span data-ttu-id="def70-103">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="def70-103">IMAPIFormMgr::ResolveMessageClass</span></span>

  
  
<span data-ttu-id="def70-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="def70-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="def70-105">Associe une classe de message à sa forme au sein d’un conteneur de formulaire et renvoie un objet d’informations de formulaire pour ce formulaire.</span><span class="sxs-lookup"><span data-stu-id="def70-105">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>
  
```cpp
HRESULT ResolveMessageClass(
  LPCSTR szMsgClass,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIFORMINFO FAR * ppResult
);
```

## <a name="parameters"></a><span data-ttu-id="def70-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="def70-106">Parameters</span></span>

 <span data-ttu-id="def70-107">_szMsgClass_</span><span class="sxs-lookup"><span data-stu-id="def70-107">_szMsgClass_</span></span>
  
> <span data-ttu-id="def70-108">[in] Chaîne qui nomme la classe de message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="def70-108">[in] A string that names the message class being resolved.</span></span>
    
 <span data-ttu-id="def70-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="def70-109">_ulFlags_</span></span>
  
> <span data-ttu-id="def70-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont la classe de message est résolue.</span><span class="sxs-lookup"><span data-stu-id="def70-110">[in] A bitmask of flags that controls how the message class is resolved.</span></span> <span data-ttu-id="def70-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="def70-111">The following flag can be set:</span></span>
    
<span data-ttu-id="def70-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="def70-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="def70-113">Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.</span><span class="sxs-lookup"><span data-stu-id="def70-113">Only message class strings that are an exact match should be resolved.</span></span>
    
 <span data-ttu-id="def70-114">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="def70-114">_pFolderFocus_</span></span>
  
> <span data-ttu-id="def70-115">[in] Pointeur vers le dossier qui contient le message en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="def70-115">[in] A pointer to the folder that contains the message being resolved.</span></span> <span data-ttu-id="def70-116">Le paramètre _pFolderFocus_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="def70-116">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="def70-117">_ppResult_</span><span class="sxs-lookup"><span data-stu-id="def70-117">_ppResult_</span></span>
  
> <span data-ttu-id="def70-118">[out] Pointeur vers un pointeur vers un objet d’informations de formulaire renvoyé.</span><span class="sxs-lookup"><span data-stu-id="def70-118">[out] A pointer to a pointer to a returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="def70-119">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="def70-119">Return value</span></span>

<span data-ttu-id="def70-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="def70-120">S_OK</span></span> 
  
> <span data-ttu-id="def70-121">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="def70-121">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="def70-122">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="def70-122">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="def70-123">La classe de message transmise dans le paramètre _szMsgClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans la bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="def70-123">The message class passed in the  _szMsgClass_ parameter does not match the message class for any form in the form library.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="def70-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="def70-124">Remarks</span></span>

<span data-ttu-id="def70-125">Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::ResolveMessageClass** pour résoudre une classe de message à sa forme au sein d’un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="def70-125">Form viewers call the **IMAPIFormMgr::ResolveMessageClass** method to resolve a message class to its form within a form container.</span></span> <span data-ttu-id="def70-126">L’écran informations objet renvoyé dans le paramètre _ppResult_ fournit plus accès aux propriétés du formulaire avec la classe de message donné.</span><span class="sxs-lookup"><span data-stu-id="def70-126">The form information object returned in the  _ppResult_ parameter provides further access to the properties of the form that has the given message class.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="def70-127">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="def70-127">Notes to callers</span></span>

<span data-ttu-id="def70-128">Pour résoudre une classe de message à un formulaire, une visionneuse de formulaire transmet le nom de la classe de message pour être résolu, tels que « `IPM.HelpDesk.Software`».</span><span class="sxs-lookup"><span data-stu-id="def70-128">To resolve a message class to a form, a form viewer passes in the name of the message class to be resolved, such as " `IPM.HelpDesk.Software`".</span></span> <span data-ttu-id="def70-129">Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message lorsqu’un formulaire correspondant exactement serveur n'est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="def70-129">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available), the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="def70-130">Si le paramètre _pFolderFocus_ est NULL, le processus de résolution de classe de message ne recherche pas un conteneur de dossiers.</span><span class="sxs-lookup"><span data-stu-id="def70-130">If the  _pFolderFocus_ parameter is NULL, the message-class resolution process does not search a folder container.</span></span> 
  
<span data-ttu-id="def70-131">L’ordre des conteneurs recherché dépend de l’implémentation du fournisseur de bibliothèque de formulaires.</span><span class="sxs-lookup"><span data-stu-id="def70-131">The order of the containers searched depends on the implementation of the form library provider.</span></span> <span data-ttu-id="def70-132">Le fournisseur de bibliothèque de formulaires par défaut recherche tout d’abord le conteneur local, puis le conteneur de dossier pour le dossier dans le passé, le conteneur de formulaires personnels et, enfin, le conteneur de l’organisation.</span><span class="sxs-lookup"><span data-stu-id="def70-132">The default form library provider searches first the local container, then the folder container for the passed-in folder, the personal form container and, finally, the organization container.</span></span>
  
<span data-ttu-id="def70-133">Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.</span><span class="sxs-lookup"><span data-stu-id="def70-133">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="def70-134">L’identificateur de classe pour la classe de message résolu est renvoyée dans le cadre de l’objet d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="def70-134">The class identifier for the resolved message class is returned as part of the form information object.</span></span> <span data-ttu-id="def70-135">Une visionneuse de formulaire ne doit pas fonctionner sur en partant du principe que l’identificateur de classe existe dans la bibliothèque OLE jusqu'à une fois la visionneuse de formulaire a appelé la méthode [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) ou la méthode [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) .</span><span class="sxs-lookup"><span data-stu-id="def70-135">A form viewer should not work on the assumption that the class identifier exists in the OLE library until after the form viewer has called either the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method or the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="def70-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="def70-136">See also</span></span>



[<span data-ttu-id="def70-137">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="def70-137">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)
  
[<span data-ttu-id="def70-138">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="def70-138">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="def70-139">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="def70-139">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="def70-140">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="def70-140">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

