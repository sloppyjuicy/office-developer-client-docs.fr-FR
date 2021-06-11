---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417670"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="53f18-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="53f18-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="53f18-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53f18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53f18-105">Crée une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="53f18-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="53f18-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="53f18-106">Parameters</span></span>

 <span data-ttu-id="53f18-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="53f18-107">_lpInterface_</span></span>
  
> <span data-ttu-id="53f18-108">[in] Pointeur vers l’identificateur d’interface (IID) représentant l’interface à utiliser pour accéder au message.</span><span class="sxs-lookup"><span data-stu-id="53f18-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="53f18-109">La transmission de null entraîne le retour de l’interface standard du message, **ou IMessage.**</span><span class="sxs-lookup"><span data-stu-id="53f18-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="53f18-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="53f18-110">_ulFlags_</span></span>
  
> <span data-ttu-id="53f18-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont la pièce jointe est créée.</span><span class="sxs-lookup"><span data-stu-id="53f18-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="53f18-112">L’indicateur suivant peut être définie :</span><span class="sxs-lookup"><span data-stu-id="53f18-112">The following flag can be set:</span></span>
    
<span data-ttu-id="53f18-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="53f18-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="53f18-114">Permet à **CreateAttach de** renvoyer correctement, éventuellement avant que la pièce jointe soit entièrement accessible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="53f18-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="53f18-115">Si la pièce jointe n’est pas accessible, un appel ultérieur peut entraîner une erreur.</span><span class="sxs-lookup"><span data-stu-id="53f18-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="53f18-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="53f18-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="53f18-117">[out] Pointeur vers un numéro d’index identifiant la pièce jointe nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="53f18-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="53f18-118">Ce numéro n’est valide que lorsque le message est ouvert et constitue la base de la propriété PR_ATTACH_NUM **(** [PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="53f18-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="53f18-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="53f18-119">_lppAttach_</span></span>
  
> <span data-ttu-id="53f18-120">[out] Pointeur vers un pointeur vers l’objet pièce jointe ouvert.</span><span class="sxs-lookup"><span data-stu-id="53f18-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="53f18-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53f18-121">Return value</span></span>

<span data-ttu-id="53f18-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="53f18-122">S_OK</span></span> 
  
> <span data-ttu-id="53f18-123">La pièce jointe a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="53f18-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53f18-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="53f18-124">Remarks</span></span>

<span data-ttu-id="53f18-125">La **méthode IMessage::CreateAttach** crée une pièce jointe sur un message.</span><span class="sxs-lookup"><span data-stu-id="53f18-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="53f18-126">La nouvelle pièce jointe et les propriétés qui lui sont définies ne sont pas disponibles tant qu’un client n’a pas appelé la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la pièce jointe et la méthode **IMAPIProp::SaveChanges** du message.</span><span class="sxs-lookup"><span data-stu-id="53f18-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="53f18-127">Le numéro de pièce jointe pointé par  _lpulAttachmentNum_ est unique et valide uniquement dans le contexte du message.</span><span class="sxs-lookup"><span data-stu-id="53f18-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="53f18-128">Autrement dit, deux pièces jointes dans deux messages différents peuvent avoir le même nombre, alors que deux pièces jointes dans le même message ne le peuvent pas.</span><span class="sxs-lookup"><span data-stu-id="53f18-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="53f18-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53f18-129">See also</span></span>



[<span data-ttu-id="53f18-130">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="53f18-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

