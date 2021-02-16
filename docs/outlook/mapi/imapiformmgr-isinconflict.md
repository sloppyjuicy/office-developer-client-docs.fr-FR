---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412883"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="53ccf-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="53ccf-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="53ccf-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53ccf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53ccf-105">Détermine si un formulaire peut gérer ses propres conflits de messages.</span><span class="sxs-lookup"><span data-stu-id="53ccf-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="53ccf-106">Un message est en conflit s’il a été modifié simultanément par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="53ccf-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="53ccf-107">Cela peut se produire pour les messages dans les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="53ccf-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="53ccf-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53ccf-108">Parameters</span></span>

 <span data-ttu-id="53ccf-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="53ccf-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="53ccf-110">[in] Pointeur vers un masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un message qui indique l’état actuel du message.</span><span class="sxs-lookup"><span data-stu-id="53ccf-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="53ccf-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="53ccf-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="53ccf-112">[in] Masque de bits d’indicateurs définis par le client ou par un fournisseur copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) d’un message qui fournit des informations supplémentaires sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="53ccf-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="53ccf-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="53ccf-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="53ccf-114">[in] Chaîne qui nomme la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="53ccf-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="53ccf-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="53ccf-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="53ccf-116">[in] Pointeur vers le dossier qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="53ccf-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="53ccf-117">Le  _paramètre pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message).</span><span class="sxs-lookup"><span data-stu-id="53ccf-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="53ccf-118">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53ccf-118">Return value</span></span>

<span data-ttu-id="53ccf-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="53ccf-119">S_OK</span></span> 
  
> <span data-ttu-id="53ccf-120">Le formulaire ne gère pas ses propres conflits de messages.</span><span class="sxs-lookup"><span data-stu-id="53ccf-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="53ccf-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="53ccf-121">S_FALSE</span></span> 
  
> <span data-ttu-id="53ccf-122">Le formulaire gère ses propres conflits de messages, ou le message pour lequel les informations ont été transmises n’est pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="53ccf-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53ccf-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="53ccf-123">Remarks</span></span>

<span data-ttu-id="53ccf-124">Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr::IsInConflict** pour découvrir si un formulaire particulier ne gère pas ses propres conflits de messages.</span><span class="sxs-lookup"><span data-stu-id="53ccf-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="53ccf-125">**IsInConflict** vérifie la présence d’un indicateur de conflit dans les paramètres _ulMessageFlags_ et _ulMessageStatus._</span><span class="sxs-lookup"><span data-stu-id="53ccf-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="53ccf-126">Si un indicateur de conflit est définie, **IsInConflict** résout la classe de message transmise dans le paramètre  _szMessageClass_ et renvoie S_OK si le formulaire ne gère pas ses propres conflits.</span><span class="sxs-lookup"><span data-stu-id="53ccf-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="53ccf-127">**IsInConflict** renvoie S_FALSE si le formulaire gère ses propres conflits.</span><span class="sxs-lookup"><span data-stu-id="53ccf-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="53ccf-128">Un formulaire qui ne gère pas ses propres conflits doit être ouvert à l’aide de la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) et ne peut pas réutiliser un objet de formulaire existant.</span><span class="sxs-lookup"><span data-stu-id="53ccf-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="53ccf-129">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="53ccf-129">Notes to callers</span></span>

<span data-ttu-id="53ccf-130">Les applications clientes doivent généralement gérer les conflits lorsque les applications sont passées d’un message au message suivant ou précédent d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="53ccf-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="53ccf-131">Si un message est en conflit, mais que le serveur de formulaires de ce message peut gérer les conflits, l’application cliente doit exécuter son code habituel pour afficher le message suivant ou précédent.</span><span class="sxs-lookup"><span data-stu-id="53ccf-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="53ccf-132">Si le serveur de formulaires ne peut pas gérer les conflits, l’application cliente doit continuer comme si elle n’avait pas connaissance de la classe de message du message suivant ou précédent.</span><span class="sxs-lookup"><span data-stu-id="53ccf-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53ccf-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53ccf-133">See also</span></span>



[<span data-ttu-id="53ccf-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="53ccf-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="53ccf-135">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="53ccf-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="53ccf-136">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="53ccf-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="53ccf-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="53ccf-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

