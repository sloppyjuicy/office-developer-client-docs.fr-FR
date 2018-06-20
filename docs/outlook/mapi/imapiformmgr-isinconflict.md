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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783796"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="27a4c-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="27a4c-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="27a4c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27a4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27a4c-105">Détermine si un formulaire peut gérer son propre conflits de message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="27a4c-106">Un message est en conflit si elle a été modifié simultanément par plusieurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="27a4c-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="27a4c-107">Cela peut se produire pour les messages dans les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="27a4c-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="27a4c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27a4c-108">Parameters</span></span>

 <span data-ttu-id="27a4c-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="27a4c-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="27a4c-110">[in] Pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) d’un message qui indique l’état actuel du message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="27a4c-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="27a4c-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="27a4c-112">[in] Masque de bits d’indicateurs défini par le client ou défini par le fournisseur copiées à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) d’un message qui fournit des informations supplémentaires sur l’état du message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="27a4c-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="27a4c-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="27a4c-114">[in] Chaîne qui nomme la classe de message du message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="27a4c-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="27a4c-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="27a4c-116">[in] Pointeur vers le dossier qui contient le message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="27a4c-117">Le paramètre _pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message).</span><span class="sxs-lookup"><span data-stu-id="27a4c-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="27a4c-118">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="27a4c-118">Return value</span></span>

<span data-ttu-id="27a4c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="27a4c-119">S_OK</span></span> 
  
> <span data-ttu-id="27a4c-120">Le formulaire ne gère pas les conflits de son propre message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="27a4c-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="27a4c-121">S_FALSE</span></span> 
  
> <span data-ttu-id="27a4c-122">Le formulaire gère son propre conflits de message ou le message pour lequel les informations a été passées n’est pas en conflit.</span><span class="sxs-lookup"><span data-stu-id="27a4c-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="27a4c-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="27a4c-123">Remarks</span></span>

<span data-ttu-id="27a4c-124">Visionneuses de formulaire appeler la méthode de **IMAPIFormMgr::IsInConflict** pour détecter si un formulaire particulier ne gère pas sa propre conflits de message.</span><span class="sxs-lookup"><span data-stu-id="27a4c-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="27a4c-125">**IsInConflict** vérifie les masques de bits dans les paramètres _ulMessageFlags_ et _ulMessageStatus_ de la présence d’un indicateur de conflit.</span><span class="sxs-lookup"><span data-stu-id="27a4c-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="27a4c-126">Si un conflit est défini, **IsInConflict** résout la classe de message transmise dans le paramètre _szMessageClass_ et renvoie S_OK si le formulaire ne gère pas son propre est en conflit.</span><span class="sxs-lookup"><span data-stu-id="27a4c-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="27a4c-127">**IsInConflict** renvoie S_FALSE si le formulaire gère son propre est en conflit.</span><span class="sxs-lookup"><span data-stu-id="27a4c-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="27a4c-128">Un formulaire qui ne gère pas sa propre conflits doit être ouverts à l’aide de la méthode [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) et ne peut pas réutiliser un objet de formulaire existant.</span><span class="sxs-lookup"><span data-stu-id="27a4c-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="27a4c-129">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="27a4c-129">Notes to callers</span></span>

<span data-ttu-id="27a4c-130">Applications clientes ont généralement à traiter les conflits lorsque les applications déplacement d’un message pour le message suivant ou précédent dans un dossier.</span><span class="sxs-lookup"><span data-stu-id="27a4c-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="27a4c-131">Si un message est en conflit, mais le serveur de formulaire pour ce message peut gérer des conflits, l’application cliente doit exécuter son code habituel pour afficher le message suivant ou précédent.</span><span class="sxs-lookup"><span data-stu-id="27a4c-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="27a4c-132">Si le serveur de formulaire ne peut pas gérer les conflits, l’application cliente doit continuer comme si elle n’a pas connaissance de la classe de message du message suivant ou précédent.</span><span class="sxs-lookup"><span data-stu-id="27a4c-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27a4c-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27a4c-133">See also</span></span>



[<span data-ttu-id="27a4c-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="27a4c-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="27a4c-135">Propriété canonique PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="27a4c-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="27a4c-136">Propriété canonique PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="27a4c-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="27a4c-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="27a4c-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

