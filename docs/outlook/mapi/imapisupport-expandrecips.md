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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 105219fe430cd8746c3aa6cf5cd90629d5f72080
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316526"
---
# <a name="imapisupportexpandrecips"></a><span data-ttu-id="3d514-103">IMAPISupport::ExpandRecips</span><span class="sxs-lookup"><span data-stu-id="3d514-103">IMAPISupport::ExpandRecips</span></span>

  
  
<span data-ttu-id="3d514-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d514-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d514-105">Complète la liste de destinataires d'un message, en développant des listes de distribution particulières.</span><span class="sxs-lookup"><span data-stu-id="3d514-105">Completes a message's recipient list, expanding particular distribution lists.</span></span>
  
```cpp
HRESULT ExpandRecips(
  LPMESSAGE lpMessage,
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="3d514-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d514-106">Parameters</span></span>

 <span data-ttu-id="3d514-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="3d514-107">_lpMessage_</span></span>
  
> <span data-ttu-id="3d514-108">dans Pointeur vers le message dont la liste de destinataires doit être traitée.</span><span class="sxs-lookup"><span data-stu-id="3d514-108">[in] A pointer to the message that has the recipient list to be processed.</span></span>
    
 <span data-ttu-id="3d514-109">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="3d514-109">_lpulFlags_</span></span>
  
> <span data-ttu-id="3d514-110">remarquer Pointeur vers un masque de des indicateurs qui contrôle le type de traitement qui se produit.</span><span class="sxs-lookup"><span data-stu-id="3d514-110">[out] A pointer to a bitmask of flags that controls the type of processing that occurs.</span></span> <span data-ttu-id="3d514-111">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="3d514-111">The following flags can be set:</span></span>
    
<span data-ttu-id="3d514-112">NEEDS_PREPROCESSING</span><span class="sxs-lookup"><span data-stu-id="3d514-112">NEEDS_PREPROCESSING</span></span> 
  
> <span data-ttu-id="3d514-113">Le message doit être prétraité avant d'être envoyé.</span><span class="sxs-lookup"><span data-stu-id="3d514-113">The message needs to be preprocessed before it is sent.</span></span>
    
<span data-ttu-id="3d514-114">NEEDS_SPOOLER</span><span class="sxs-lookup"><span data-stu-id="3d514-114">NEEDS_SPOOLER</span></span> 
  
> <span data-ttu-id="3d514-115">Le spouleur MAPI (plutôt que le fournisseur de transport auquel l'appelant est étroitement couplé) doit envoyer le message.</span><span class="sxs-lookup"><span data-stu-id="3d514-115">The MAPI spooler (rather than the transport provider to which the caller is tightly coupled) must send the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3d514-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d514-116">Return value</span></span>

<span data-ttu-id="3d514-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d514-117">S_OK</span></span> 
  
> <span data-ttu-id="3d514-118">La liste des destinataires du message a été traitée avec succès.</span><span class="sxs-lookup"><span data-stu-id="3d514-118">The message's recipient list was successfully processed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d514-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d514-119">Remarks</span></span>

<span data-ttu-id="3d514-120">La méthode **IMAPISupport:: ExpandRecips** est implémentée pour les objets de prise en charge du fournisseur de banque de messages.</span><span class="sxs-lookup"><span data-stu-id="3d514-120">The **IMAPISupport::ExpandRecips** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="3d514-121">Les fournisseurs de banques de messages appellent **ExpandRecips** pour inviter MAPI à effectuer les tâches suivantes:</span><span class="sxs-lookup"><span data-stu-id="3d514-121">Message store providers call **ExpandRecips** to prompt MAPI to perform the following tasks:</span></span> 
  
- <span data-ttu-id="3d514-122">Développez certaines listes de distribution personnelle vers leurs destinataires de composants.</span><span class="sxs-lookup"><span data-stu-id="3d514-122">Expand certain personal distribution lists to their component recipients.</span></span>
    
- <span data-ttu-id="3d514-123">Remplacez tous les noms d'affichage qui ont été modifiés par les noms d'origine.</span><span class="sxs-lookup"><span data-stu-id="3d514-123">Replace all display names that have been changed with the original names.</span></span>
    
- <span data-ttu-id="3d514-124">Marquez toutes les entrées en double.</span><span class="sxs-lookup"><span data-stu-id="3d514-124">Mark any duplicate entries.</span></span>
    
- <span data-ttu-id="3d514-125">Résoudre toutes les adresses ponctuelles.</span><span class="sxs-lookup"><span data-stu-id="3d514-125">Resolve all one-off addresses.</span></span> 
    
- <span data-ttu-id="3d514-126">Vérifiez si le message doit être prétraité et, si c'est le cas, définissez l'indicateur désigné par _lpulFlags_ sur NEEDS_PREPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="3d514-126">Check whether the message needs preprocessing and, if it does, set the flag pointed to by  _lpulFlags_ to NEEDS_PREPROCESSING.</span></span> 
    
 <span data-ttu-id="3d514-127">**ExpandRecips** développe toutes les listes de distribution dont le type d'adresse de messagerie est MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="3d514-127">**ExpandRecips** expands any distribution lists that have the messaging address type of MAPIPDL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d514-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3d514-128">Notes to callers</span></span>

<span data-ttu-id="3d514-129">Appelez toujours **ExpandRecips** dans le cadre de votre traitement de message.</span><span class="sxs-lookup"><span data-stu-id="3d514-129">Always call **ExpandRecips** as part of your message processing.</span></span> <span data-ttu-id="3d514-130">Appelez **ExpandRecips** l'un des premiers appels dans votre implémentation de la méthode [IMessage: SubmitMessage](imessage-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="3d514-130">Make a call to **ExpandRecips** one of the first calls in your [IMessage::SubmitMessage](imessage-submitmessage.md) method implementation.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3d514-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d514-131">See also</span></span>



[<span data-ttu-id="3d514-132">IMessage::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="3d514-132">IMessage::SubmitMessage</span></span>](imessage-submitmessage.md)
  
[<span data-ttu-id="3d514-133">IMAPISupport : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d514-133">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

