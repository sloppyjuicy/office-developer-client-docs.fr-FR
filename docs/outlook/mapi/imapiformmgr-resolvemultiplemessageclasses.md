---
title: IMAPIFormMgrResolveMultipleMessageClasses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.ResolveMultipleMessageClasses
api_type:
- COM
ms.assetid: d3cc6658-e46d-42dd-b1ac-65c88cfef8ca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 968be38e794793405aac15340a92ccd6d680498d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571695"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="309be-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="309be-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="309be-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="309be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="309be-105">Résout un groupe de classes de message à leurs formulaires dans un conteneur de formulaire et renvoie un tableau de formulaire objets des informations pour les formulaires.</span><span class="sxs-lookup"><span data-stu-id="309be-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="309be-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="309be-106">Parameters</span></span>

 <span data-ttu-id="309be-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="309be-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="309be-108">[in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre.</span><span class="sxs-lookup"><span data-stu-id="309be-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="309be-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="309be-109">_ulFlags_</span></span>
  
> <span data-ttu-id="309be-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolus.</span><span class="sxs-lookup"><span data-stu-id="309be-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="309be-111">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="309be-111">The following flag can be set:</span></span>
    
<span data-ttu-id="309be-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="309be-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="309be-113">Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.</span><span class="sxs-lookup"><span data-stu-id="309be-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="309be-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="309be-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="309be-115">N’incluez pas de formulaires mis en cache.</span><span class="sxs-lookup"><span data-stu-id="309be-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="309be-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="309be-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="309be-117">[in] Pointeur vers le dossier qui contient le formulaire dont la classe de message est résolue.</span><span class="sxs-lookup"><span data-stu-id="309be-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="309be-118">Le paramètre _pFolderFocus_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="309be-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="309be-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="309be-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="309be-120">[out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="309be-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="309be-121">Si une visionneuse de formulaire passe NULL dans le paramètre _pMsgClasses_ , le paramètre _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="309be-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="309be-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="309be-122">Return value</span></span>

<span data-ttu-id="309be-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="309be-123">S_OK</span></span> 
  
> <span data-ttu-id="309be-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="309be-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="309be-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="309be-125">Remarks</span></span>

<span data-ttu-id="309be-126">Visionneuses de formulaire appellent la méthode **IMAPIFormMgr::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message pour des formulaires dans un conteneur de formulaire.</span><span class="sxs-lookup"><span data-stu-id="309be-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="309be-127">Le tableau d’objets formulaire renvoyé dans _ppfrminfoarray_ fournit davantage l’accès à chacune des propriétés des formulaires.</span><span class="sxs-lookup"><span data-stu-id="309be-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="309be-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="309be-128">Notes to callers</span></span>

<span data-ttu-id="309be-129">Pour résoudre un groupe de classes de message aux formulaires, une visionneuse de formulaire transmet dans un tableau de résolution des noms de classe de message.</span><span class="sxs-lookup"><span data-stu-id="309be-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="309be-130">Pour forcer la résolution à être exact (autrement dit, pour empêcher la résolution à une classe de base de la classe de message lorsqu’un formulaire correspondant exactement serveur n'est pas disponible) l’indicateur MAPIFORM_EXACTMATCH peut être passé dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="309be-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="309be-131">Noms de classe de message sont toujours des chaînes ANSI, Unicode jamais.</span><span class="sxs-lookup"><span data-stu-id="309be-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="309be-132">Si une classe de message ne peut pas être résolue à un formulaire, NULL est renvoyé pour cette classe de message dans le tableau d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="309be-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="309be-133">Par conséquent, même si la méthode renvoie S_OK, les visionneuses de formulaire devraient fonctionner pas sur l’hypothèse que toutes les classes de message ont été correctement résolus.</span><span class="sxs-lookup"><span data-stu-id="309be-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="309be-134">Au lieu de cela, les visionneuses de formulaire doivent vérifier les valeurs dans le tableau retourné.</span><span class="sxs-lookup"><span data-stu-id="309be-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="309be-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="309be-135">See also</span></span>



[<span data-ttu-id="309be-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="309be-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="309be-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="309be-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

