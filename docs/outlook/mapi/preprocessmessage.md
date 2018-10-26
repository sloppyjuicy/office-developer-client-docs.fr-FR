---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 878c3aaf22a6cf8a08c8234df41b671088c435c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584988"
---
# <a name="preprocessmessage"></a><span data-ttu-id="09dd4-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="09dd4-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="09dd4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09dd4-105">Définit une fonction qui pré-traite les contenus du message ou le format d’un message.</span><span class="sxs-lookup"><span data-stu-id="09dd4-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="09dd4-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="09dd4-106">Header file:</span></span>  <br/> |<span data-ttu-id="09dd4-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="09dd4-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="09dd4-108">Fonction implémentée par :</span><span class="sxs-lookup"><span data-stu-id="09dd4-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="09dd4-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="09dd4-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="09dd4-110">Fonction appelée par :</span><span class="sxs-lookup"><span data-stu-id="09dd4-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="09dd4-111">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="09dd4-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="09dd4-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09dd4-112">Parameters</span></span>

 <span data-ttu-id="09dd4-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="09dd4-113">_lpvSession_</span></span>
  
> <span data-ttu-id="09dd4-114">[in] Pointeur vers la session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="09dd4-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="09dd4-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="09dd4-115">_lpMessage_</span></span>
  
> <span data-ttu-id="09dd4-116">[in] Pointeur vers le message prétraitement.</span><span class="sxs-lookup"><span data-stu-id="09dd4-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="09dd4-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="09dd4-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="09dd4-118">[in] Pointeur vers le carnet d’adresses à partir de laquelle l’utilisateur doit sélectionner les destinataires du message.</span><span class="sxs-lookup"><span data-stu-id="09dd4-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="09dd4-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="09dd4-119">_lpFolder_</span></span>
  
> <span data-ttu-id="09dd4-120">[entrée, sortie] Pointeur vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="09dd4-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="09dd4-121">À l’entrée, le paramètre _lpFolder_ pointe vers le dossier qui contient les messages prétraitement.</span><span class="sxs-lookup"><span data-stu-id="09dd4-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="09dd4-122">Dans la sortie, _lpFolder_ pointe vers le dossier où les messages prétraités ont été placés.</span><span class="sxs-lookup"><span data-stu-id="09dd4-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="09dd4-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="09dd4-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="09dd4-124">[in] Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) , à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="09dd4-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="09dd4-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="09dd4-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="09dd4-126">[in] Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) , à utiliser pour allouer de la mémoire supplémentaire si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="09dd4-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="09dd4-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="09dd4-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="09dd4-128">[in] Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) , à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="09dd4-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="09dd4-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="09dd4-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="09dd4-130">[out] Pointeur vers le nombre de messages dans le tableau indiqué par le paramètre _lpppMessage_ .</span><span class="sxs-lookup"><span data-stu-id="09dd4-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="09dd4-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="09dd4-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="09dd4-132">[out] Pointeur vers un pointeur vers un tableau de pointeurs vers prétraités ou les messages générés dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="09dd4-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="09dd4-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="09dd4-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="09dd4-134">[out] Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, liste des destinataires détecté préprocesseur pour laquelle le message est remis.</span><span class="sxs-lookup"><span data-stu-id="09dd4-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="09dd4-135">Pour plus d’informations sur le contenu de cette liste, voir la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="09dd4-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="09dd4-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="09dd4-136">Return value</span></span>

<span data-ttu-id="09dd4-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="09dd4-137">S_OK</span></span>
  
> <span data-ttu-id="09dd4-138">Contenu du message ont été prétraité avec succès.</span><span class="sxs-lookup"><span data-stu-id="09dd4-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="09dd4-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="09dd4-139">Remarks</span></span>

<span data-ttu-id="09dd4-140">Un préprocesseur de message-fournisseur de transport peut représenter un indicateur de progression pendant le prétraitement du message.</span><span class="sxs-lookup"><span data-stu-id="09dd4-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="09dd4-141">Toutefois, il ne doit jamais présenter une boîte de dialogue solliciter l’utilisateur pendant le prétraitement du message.</span><span class="sxs-lookup"><span data-stu-id="09dd4-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="09dd4-142">Lorsqu’un préprocesseur ajoute des grandes quantités de données à un message sortant, certaines procédures.</span><span class="sxs-lookup"><span data-stu-id="09dd4-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="09dd4-143">Ce type de message peut être stocké dans une banque de messages sur le serveur, et le préprocesseur accéder à un magasin distant, beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="09dd4-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="09dd4-144">Pour éviter d’avoir à le faire, le préprocesseur doit avoir une option qui lui permet de stocker les données qui accepte une grande quantité d’espace dans une banque de messages locale et pour fournir une référence à cette banque locale dans le message.</span><span class="sxs-lookup"><span data-stu-id="09dd4-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="09dd4-145">Le préprocesseur ne doit pas libérer tous les objets initialement transmis à la fonction **PreprocessMessage** basé.</span><span class="sxs-lookup"><span data-stu-id="09dd4-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="09dd4-146">Avant le spouleur MAPI peut appeler une fonction **PreprocessMessage** , le fournisseur de transport doit avoir enregistré la fonction dans un appel à la méthode [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="09dd4-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="09dd4-147">Après avoir appelé une fonction **PreprocessMessage** , le spouleur ne peut pas continuer à envoyer un message jusqu'à ce que la fonction renvoie.</span><span class="sxs-lookup"><span data-stu-id="09dd4-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="09dd4-148">Le spouleur MAPI propriétaire de la tâche de soumission de messages.</span><span class="sxs-lookup"><span data-stu-id="09dd4-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="09dd4-149">Cela signifie que le message d’origine n’est jamais placé dans un tableau de pointeurs de message et qu’un appel aux méthodes **SubmitMessage** jamais.</span><span class="sxs-lookup"><span data-stu-id="09dd4-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="09dd4-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09dd4-150">See also</span></span>



[<span data-ttu-id="09dd4-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="09dd4-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="09dd4-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="09dd4-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="09dd4-153">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09dd4-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

