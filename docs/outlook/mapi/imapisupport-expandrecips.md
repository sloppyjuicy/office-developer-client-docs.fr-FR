---
title: IMAPISupportExpandRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ExpandRecips
api_type:
- COM
ms.assetid: 78edd549-d557-489a-85f5-adfb5c44a7d4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411245"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="579c4-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="579c4-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="579c4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="579c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="579c4-105">Complète la liste des destinataires d’un message, en développe des listes de distribution particulières.</span><span class="sxs-lookup"><span data-stu-id="579c4-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="579c4-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="579c4-106">Parameters</span></span>

 <span data-ttu-id="579c4-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="579c4-107">_lpMessage_</span></span>
  
> <span data-ttu-id="579c4-108">[in] Pointeur vers le message dont la liste des destinataires doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="579c4-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="579c4-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="579c4-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="579c4-110">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle le type de traitement qui se produit.</span><span class="sxs-lookup"><span data-stu-id="579c4-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="579c4-111">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="579c4-111">The following flags can be set:</span></span>
    
<span data-ttu-id="579c4-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="579c4-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="579c4-113">Le message doit être prétraité avant d’être envoyé.</span><span class="sxs-lookup"><span data-stu-id="579c4-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="579c4-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="579c4-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="579c4-115">Lepooler MAPI (plutôt que le fournisseur de transport auquel l’appelant est étroitement associé) doit envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="579c4-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="579c4-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="579c4-116">Return value</span></span>

<span data-ttu-id="579c4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="579c4-117">S_OK</span></span> 
  
> <span data-ttu-id="579c4-118">La liste des destinataires du message a été traitée avec succès.</span><span class="sxs-lookup"><span data-stu-id="579c4-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="579c4-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="579c4-119">Remarks</span></span>

<span data-ttu-id="579c4-120">La **méthode IMAPISupport::ExpandRecips est** implémentée pour les objets de prise en charge du fournisseur de magasins de messages.</span><span class="sxs-lookup"><span data-stu-id="579c4-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="579c4-121">Les fournisseurs de magasins de messages **appellent ExpandRecips** pour demander à MAPI d’effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="579c4-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="579c4-122">Développez certaines listes de distribution personnelles pour les destinataires de leurs composants.</span><span class="sxs-lookup"><span data-stu-id="579c4-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="579c4-123">Remplacez tous les noms d’affichage qui ont été modifiés par les noms d’origine.</span><span class="sxs-lookup"><span data-stu-id="579c4-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="579c4-124">Marquez les entrées en double.</span><span class="sxs-lookup"><span data-stu-id="579c4-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="579c4-125">Résolvez toutes les adresses à une seule adresse.</span><span class="sxs-lookup"><span data-stu-id="579c4-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="579c4-126">Vérifiez si le message doit être prétraité et, si c’est le cas, définissez l’indicateur pointé par  _lpulFlags_ sur NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="579c4-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="579c4-127">**ExpandRecips développe toutes** les listes de distribution qui ont le type d’adresse de messagerie MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="579c4-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="579c4-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="579c4-128">Notes to callers</span></span>

<span data-ttu-id="579c4-129">Appelez **toujours ExpandRecips dans le** cadre du traitement de vos messages.</span><span class="sxs-lookup"><span data-stu-id="579c4-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="579c4-130">Appelez **ExpandRecips l’un** des premiers appels dans l’implémentation de votre méthode [IMessage::SubmitMessage.](imessage-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="579c4-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="579c4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="579c4-131">See also</span></span>



[<span data-ttu-id="579c4-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="579c4-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="579c4-133">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="579c4-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

