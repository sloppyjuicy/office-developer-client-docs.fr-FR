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
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572085"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="e4431-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="e4431-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="e4431-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4431-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4431-105">Crée une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e4431-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="e4431-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4431-106">Parameters</span></span>

 <span data-ttu-id="e4431-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e4431-107">_lpInterface_</span></span>
  
> <span data-ttu-id="e4431-108">[in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message.</span><span class="sxs-lookup"><span data-stu-id="e4431-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="e4431-109">Passant NULL entraîne une interface standard du message ou **IMessage**, renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e4431-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="e4431-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e4431-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e4431-111">[in] Masque de bits d’indicateurs qui contrôle la création de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e4431-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="e4431-112">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="e4431-112">The following flag can be set:</span></span>
    
<span data-ttu-id="e4431-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e4431-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e4431-114">Permet de **CreateAttach** renvoyer avec succès, éventuellement avant la pièce jointe est accessible au client appelant.</span><span class="sxs-lookup"><span data-stu-id="e4431-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="e4431-115">Si la pièce jointe n’est pas accessible, passer un appel suivant pour qu’il peut provoquer une erreur.</span><span class="sxs-lookup"><span data-stu-id="e4431-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="e4431-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="e4431-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="e4431-117">[out] Pointeur vers un numéro d’index qui identifie la pièce jointe nouvellement créée.</span><span class="sxs-lookup"><span data-stu-id="e4431-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="e4431-118">Ce numéro est valide uniquement lorsque le message est ouvert et la base de la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e4431-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="e4431-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="e4431-119">_lppAttach_</span></span>
  
> <span data-ttu-id="e4431-120">[out] Pointeur vers un pointeur vers l’objet d’ouvrir une pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e4431-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e4431-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e4431-121">Return value</span></span>

<span data-ttu-id="e4431-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e4431-122">S_OK</span></span> 
  
> <span data-ttu-id="e4431-123">La pièce jointe a été créée avec succès.</span><span class="sxs-lookup"><span data-stu-id="e4431-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e4431-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="e4431-124">Remarks</span></span>

<span data-ttu-id="e4431-125">La méthode **IMessage::CreateAttach** crée une pièce jointe d’un message.</span><span class="sxs-lookup"><span data-stu-id="e4431-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="e4431-126">La nouvelle pièce jointe et les propriétés qui sont définies, ne sont pas disponibles tant qu’un client a appelé méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) de la pièce jointe et de méthode de **IMAPIProp::SaveChanges** du message.</span><span class="sxs-lookup"><span data-stu-id="e4431-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="e4431-127">Le nombre de pièces jointes désigné par _lpulAttachmentNum_ est unique et valide uniquement dans le contexte du message.</span><span class="sxs-lookup"><span data-stu-id="e4431-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="e4431-128">Autrement dit, deux pièces jointes dans deux messages différents peuvent avoir le même nombre mais pas les deux pièces jointes dans le même message.</span><span class="sxs-lookup"><span data-stu-id="e4431-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e4431-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4431-129">See also</span></span>



[<span data-ttu-id="e4431-130">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e4431-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

