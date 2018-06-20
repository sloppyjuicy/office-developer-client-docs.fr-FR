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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 2e41701d3a739864b1eafc8001833b7df5c8908b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783991"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="2888c-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="2888c-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="2888c-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2888c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2888c-105">Termine la liste des destinataires d’un message, développer des listes de distribution particulier.</span><span class="sxs-lookup"><span data-stu-id="2888c-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2888c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2888c-106">Parameters</span></span>

 <span data-ttu-id="2888c-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="2888c-107">_lpMessage_</span></span>
  
> <span data-ttu-id="2888c-108">[in] Pointeur vers le message qui contient la liste des destinataires à traiter.</span><span class="sxs-lookup"><span data-stu-id="2888c-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="2888c-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="2888c-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="2888c-110">[out] Pointeur vers un masque de bits d’indicateurs qui contrôle le type de traitement qui se produit.</span><span class="sxs-lookup"><span data-stu-id="2888c-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="2888c-111">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="2888c-111">The following flags can be set:</span></span>
    
<span data-ttu-id="2888c-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="2888c-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="2888c-113">Le message doit être prétraités avant son envoi.</span><span class="sxs-lookup"><span data-stu-id="2888c-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="2888c-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="2888c-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="2888c-115">Le spouleur MAPI (plutôt que le fournisseur de transport dans lequel l’appelant est étroitement) doit envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="2888c-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2888c-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2888c-116">Return value</span></span>

<span data-ttu-id="2888c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="2888c-117">S_OK</span></span> 
  
> <span data-ttu-id="2888c-118">Liste des destinataires du message a été correctement traitée.</span><span class="sxs-lookup"><span data-stu-id="2888c-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2888c-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="2888c-119">Remarks</span></span>

<span data-ttu-id="2888c-120">La méthode **IMAPISupport::ExpandRecips** est implémentée pour les objets de prise en charge de fournisseur de magasin de message.</span><span class="sxs-lookup"><span data-stu-id="2888c-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="2888c-121">Fournisseurs de magasins message appeler **ExpandRecips** pour demander l’interface MAPI pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="2888c-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="2888c-122">Développez certaines listes de distribution personnelles aux destinataires d’un composant.</span><span class="sxs-lookup"><span data-stu-id="2888c-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="2888c-123">Remplacez tous les noms complets qui ont été modifiées par les noms d’origine.</span><span class="sxs-lookup"><span data-stu-id="2888c-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="2888c-124">Marquer des entrées en double.</span><span class="sxs-lookup"><span data-stu-id="2888c-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="2888c-125">Résoudre toutes les adresses uniques.</span><span class="sxs-lookup"><span data-stu-id="2888c-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="2888c-126">Vérifier si le message a besoin de prétraitement et, si c’est le cas, définie l’indicateur désignés par _lpulFlags_ à NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="2888c-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="2888c-127">**ExpandRecips** développe des listes de distribution dont le type de MAPIPDL adresse de messagerie.</span><span class="sxs-lookup"><span data-stu-id="2888c-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2888c-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="2888c-128">Notes to callers</span></span>

<span data-ttu-id="2888c-129">Appelez toujours **ExpandRecips** dans le cadre de votre processus de message.</span><span class="sxs-lookup"><span data-stu-id="2888c-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="2888c-130">Émettre un appel à **ExpandRecips** 1 de l’appelle d’abord dans votre implémentation de la méthode [IMessage::SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="2888c-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2888c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2888c-131">See also</span></span>



[<span data-ttu-id="2888c-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="2888c-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="2888c-133">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2888c-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

