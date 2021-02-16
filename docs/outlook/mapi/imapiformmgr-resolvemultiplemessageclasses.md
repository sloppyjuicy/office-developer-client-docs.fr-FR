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
ms.openlocfilehash: 515061c6c208008c4752e5ff2f23933a4c259c00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428017"
---
# <a name="imapiformmgrresolvemultiplemessageclasses"></a><span data-ttu-id="1b74a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="1b74a-103">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>

  
  
<span data-ttu-id="1b74a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b74a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b74a-105">Résout un groupe de classes de message dans leurs formulaires dans un conteneur de formulaires et renvoie un tableau d’objets d’informations de formulaire pour ces formulaires.</span><span class="sxs-lookup"><span data-stu-id="1b74a-105">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>
  
```cpp
HRESULT ResolveMultipleMessageClasses(
  LPSMESSAGECLASSARRAY pMsgClasses,
  ULONG ulFlags,
  LPMAPIFOLDER pFolderFocus,
  LPSMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="1b74a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b74a-106">Parameters</span></span>

 <span data-ttu-id="1b74a-107">_pMsgClasses_</span><span class="sxs-lookup"><span data-stu-id="1b74a-107">_pMsgClasses_</span></span>
  
> <span data-ttu-id="1b74a-108">[in] Pointeur vers un tableau qui contient les noms des classes de message à résoudre.</span><span class="sxs-lookup"><span data-stu-id="1b74a-108">[in] A pointer to an array that contains the names of the message classes to resolve.</span></span>
    
 <span data-ttu-id="1b74a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1b74a-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1b74a-110">[in] Masque de bits d’indicateurs qui contrôle la façon dont les classes de message sont résolues.</span><span class="sxs-lookup"><span data-stu-id="1b74a-110">[in] A bitmask of flags that controls how the message classes are resolved.</span></span> <span data-ttu-id="1b74a-111">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="1b74a-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1b74a-112">MAPIFORM_EXACTMATCH</span><span class="sxs-lookup"><span data-stu-id="1b74a-112">MAPIFORM_EXACTMATCH</span></span> 
  
> <span data-ttu-id="1b74a-113">Seules les chaînes de classe de message qui correspondent exactement doivent être résolues.</span><span class="sxs-lookup"><span data-stu-id="1b74a-113">Only message class strings that are an exact match should be resolved.</span></span>
    
<span data-ttu-id="1b74a-114">MAPIFORM_LOCALONLY</span><span class="sxs-lookup"><span data-stu-id="1b74a-114">MAPIFORM_LOCALONLY</span></span>
  
> <span data-ttu-id="1b74a-115">N’incluez pas les formulaires mis en cache.</span><span class="sxs-lookup"><span data-stu-id="1b74a-115">Do not include cached forms.</span></span>
    
 <span data-ttu-id="1b74a-116">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="1b74a-116">_pFolderFocus_</span></span>
  
> <span data-ttu-id="1b74a-117">[in] Pointeur vers le dossier qui contient le formulaire dont la classe de message est en cours de résolution.</span><span class="sxs-lookup"><span data-stu-id="1b74a-117">[in] A pointer to the folder that contains the form whose message class is being resolved.</span></span> <span data-ttu-id="1b74a-118">Le  _paramètre pFolderFocus_ peut être NULL.</span><span class="sxs-lookup"><span data-stu-id="1b74a-118">The  _pFolderFocus_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="1b74a-119">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="1b74a-119">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="1b74a-120">[out] Pointeur vers un pointeur vers un tableau d’objets d’informations de formulaire.</span><span class="sxs-lookup"><span data-stu-id="1b74a-120">[out] A pointer to a pointer to an array of form information objects.</span></span> <span data-ttu-id="1b74a-121">Si une visionneuse de formulaire transmet la valeur NULL dans le paramètre  _pMsgClasses,_ le paramètre  _ppfrminfoarray_ contient des objets d’informations de formulaire pour tous les formulaires dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="1b74a-121">If a form viewer passes NULL in the  _pMsgClasses_ parameter, the  _ppfrminfoarray_ parameter contains form information objects for all forms in the container.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b74a-122">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b74a-122">Return value</span></span>

<span data-ttu-id="1b74a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b74a-123">S_OK</span></span> 
  
> <span data-ttu-id="1b74a-124">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="1b74a-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b74a-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b74a-125">Remarks</span></span>

<span data-ttu-id="1b74a-126">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::ResolveMultipleMessageClasses** pour résoudre un groupe de classes de message en formulaires dans un conteneur de formulaires.</span><span class="sxs-lookup"><span data-stu-id="1b74a-126">Form viewers call the **IMAPIFormMgr::ResolveMultipleMessageClasses** method to resolve a group of message classes to forms within a form container.</span></span> <span data-ttu-id="1b74a-127">Le tableau des objets d’informations de formulaire renvoyés dans  _ppfrminfoarray_ fournit un accès supplémentaire à chacune des propriétés des formulaires.</span><span class="sxs-lookup"><span data-stu-id="1b74a-127">The array of form information objects returned in  _ppfrminfoarray_ provides further access to each of the forms' properties.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b74a-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="1b74a-128">Notes to callers</span></span>

<span data-ttu-id="1b74a-129">Pour résoudre un groupe de classes de message en formulaires, une visionneuse de formulaires transmet un tableau de noms de classes de messages à résoudre.</span><span class="sxs-lookup"><span data-stu-id="1b74a-129">To resolve a group of message classes to forms, a form viewer passes in an array of message class names to be resolved.</span></span> <span data-ttu-id="1b74a-130">Pour forcer la résolution à être exacte (c’est-à-dire pour empêcher la résolution à une classe de base de la classe de message lorsqu’un serveur de formulaires correspondant exactement n’est pas disponible), l’indicateur MAPIFORM_EXACTMATCH peut être transmis dans le paramètre _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="1b74a-130">To force the resolution to be exact (that is, to prevent resolution to a base class of the message class when an exactly matching form server is not available) the MAPIFORM_EXACTMATCH flag can be passed in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="1b74a-131">Les noms de classe de message sont toujours des chaînes ANSI, jamais Unicode.</span><span class="sxs-lookup"><span data-stu-id="1b74a-131">Message class names are always ANSI strings, never Unicode.</span></span>
  
<span data-ttu-id="1b74a-132">Si une classe de message ne peut pas être résolue en formulaire, la valeur NULL est renvoyée pour cette classe de message dans le tableau d’informations du formulaire.</span><span class="sxs-lookup"><span data-stu-id="1b74a-132">If a message class cannot be resolved to a form, NULL is returned for that message class in the form information array.</span></span> <span data-ttu-id="1b74a-133">Par conséquent, même si la méthode renvoie S_OK, les visionneuses de formulaires ne doivent pas fonctionner sur l’hypothèse que toutes les classes de message ont été correctement résolues.</span><span class="sxs-lookup"><span data-stu-id="1b74a-133">Therefore, even if the method returns S_OK, form viewers should not work on the assumption that all message classes have been successfully resolved.</span></span> <span data-ttu-id="1b74a-134">Au lieu de cela, les visionneuses de formulaire doivent vérifier les valeurs dans le tableau renvoyé.</span><span class="sxs-lookup"><span data-stu-id="1b74a-134">Instead, form viewers should check the values in the returned array.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b74a-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b74a-135">See also</span></span>



[<span data-ttu-id="1b74a-136">IMAPIFormMgr::ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="1b74a-136">IMAPIFormMgr::ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md)
  
[<span data-ttu-id="1b74a-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b74a-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

