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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351379"
---
# <a name="preprocessmessage"></a><span data-ttu-id="230ac-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="230ac-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="230ac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="230ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="230ac-105">Définit une fonction qui prétraite le contenu des messages ou le format d'un message.</span><span class="sxs-lookup"><span data-stu-id="230ac-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="230ac-106">Fichier d’en-tête :</span><span class="sxs-lookup"><span data-stu-id="230ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="230ac-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="230ac-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="230ac-108">Fonction définie implémentée par:</span><span class="sxs-lookup"><span data-stu-id="230ac-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="230ac-109">Fournisseurs de transport</span><span class="sxs-lookup"><span data-stu-id="230ac-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="230ac-110">Fonction définie appelée par:</span><span class="sxs-lookup"><span data-stu-id="230ac-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="230ac-111">Spouleur MAPI</span><span class="sxs-lookup"><span data-stu-id="230ac-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="230ac-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="230ac-112">Parameters</span></span>

 <span data-ttu-id="230ac-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="230ac-113">_lpvSession_</span></span>
  
> <span data-ttu-id="230ac-114">dans Pointeur vers la session à utiliser.</span><span class="sxs-lookup"><span data-stu-id="230ac-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="230ac-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="230ac-115">_lpMessage_</span></span>
  
> <span data-ttu-id="230ac-116">dans Pointeur vers le message à prétraiter.</span><span class="sxs-lookup"><span data-stu-id="230ac-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="230ac-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="230ac-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="230ac-118">dans Pointeur vers le carnet d'adresses à partir duquel l'utilisateur doit sélectionner des destinataires pour le message.</span><span class="sxs-lookup"><span data-stu-id="230ac-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="230ac-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="230ac-119">_lpFolder_</span></span>
  
> <span data-ttu-id="230ac-120">[in, out] Pointeur vers un dossier.</span><span class="sxs-lookup"><span data-stu-id="230ac-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="230ac-121">Lors de l'entrée, le paramètre _lpFolder_ pointe vers le dossier qui contient les messages à prétraiter.</span><span class="sxs-lookup"><span data-stu-id="230ac-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="230ac-122">Lors de la sortie, _lpFolder_ pointe vers le dossier où les messages prétraités ont été placés.</span><span class="sxs-lookup"><span data-stu-id="230ac-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="230ac-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="230ac-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="230ac-124">dans Pointeur vers la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) à utiliser pour allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="230ac-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="230ac-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="230ac-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="230ac-126">dans Pointeur vers la fonction [MAPIAllocateMore](mapiallocatemore.md) à utiliser pour allouer de la mémoire supplémentaire lorsque cela est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="230ac-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="230ac-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="230ac-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="230ac-128">dans Pointeur vers la fonction [MAPIFreeBuffer](mapifreebuffer.md) à utiliser pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="230ac-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="230ac-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="230ac-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="230ac-130">remarquer Pointeur vers le nombre de messages dans le tableau vers lequel pointe le paramètre _lpppMessage_ .</span><span class="sxs-lookup"><span data-stu-id="230ac-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="230ac-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="230ac-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="230ac-132">remarquer Pointeur vers un pointeur vers un tableau de pointeurs vers des messages prétraités ou générés.</span><span class="sxs-lookup"><span data-stu-id="230ac-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="230ac-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="230ac-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="230ac-134">remarquer Pointeur vers une structure [ADRLIST](adrlist.md) renvoyée facultative, répertoriant les destinataires détectés par le préprocesseur pour lesquels le message ne peut pas être remis.</span><span class="sxs-lookup"><span data-stu-id="230ac-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="230ac-135">Pour plus d'informations sur le contenu de cette liste, voir la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) .</span><span class="sxs-lookup"><span data-stu-id="230ac-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="230ac-136">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="230ac-136">Return value</span></span>

<span data-ttu-id="230ac-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="230ac-137">S_OK</span></span>
  
> <span data-ttu-id="230ac-138">Le contenu du message a été prétraité avec succès.</span><span class="sxs-lookup"><span data-stu-id="230ac-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="230ac-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="230ac-139">Remarks</span></span>

<span data-ttu-id="230ac-140">Un préprocesseur de message de fournisseur de transport peut présenter un indicateur de progression pendant le prétraitement des messages.</span><span class="sxs-lookup"><span data-stu-id="230ac-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="230ac-141">Toutefois, il ne doit jamais présenter une boîte de dialogue demandant l'interaction de l'utilisateur pendant le prétraitement des messages.</span><span class="sxs-lookup"><span data-stu-id="230ac-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="230ac-142">Lorsqu'un préprocesseur ajoute de grandes quantités de données à un message sortant, certaines procédures doivent être suivies.</span><span class="sxs-lookup"><span data-stu-id="230ac-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="230ac-143">Ce type de message peut être stocké dans une banque de messages basée sur un serveur, ce qui oblige le préprocesseur à accéder à un magasin distant, une procédure qui prend du temps.</span><span class="sxs-lookup"><span data-stu-id="230ac-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="230ac-144">Pour éviter cela, le préprocesseur doit disposer d'une option permettant de stocker des données qui occupent beaucoup d'espace dans une banque de messages locale et de fournir une référence à cette banque locale dans le message.</span><span class="sxs-lookup"><span data-stu-id="230ac-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="230ac-145">Le préprocesseur ne doit pas libérer les objets transmis à l'origine à la fonction **PreprocessMessage** .</span><span class="sxs-lookup"><span data-stu-id="230ac-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="230ac-146">Avant que le spouleur MAPI puisse appeler une fonction **PreprocessMessage** , le fournisseur de transport doit avoir inscrit la fonction dans un appel à la méthode [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) .</span><span class="sxs-lookup"><span data-stu-id="230ac-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="230ac-147">Après l'appel d'une fonction **PreprocessMessage** , le spouleur ne peut pas continuer à envoyer un message tant que la fonction n'est pas renvoyée.</span><span class="sxs-lookup"><span data-stu-id="230ac-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="230ac-148">Le spouleur MAPI est propriétaire de la tâche d'envoi de messages.</span><span class="sxs-lookup"><span data-stu-id="230ac-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="230ac-149">Cela signifie que le message d'origine n'est jamais placé dans un tableau de pointeurs de message et qu'un appel aux méthodes **SubmitMessage** n'est jamais requis.</span><span class="sxs-lookup"><span data-stu-id="230ac-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="230ac-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="230ac-150">See also</span></span>



[<span data-ttu-id="230ac-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="230ac-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="230ac-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="230ac-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="230ac-153">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="230ac-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

