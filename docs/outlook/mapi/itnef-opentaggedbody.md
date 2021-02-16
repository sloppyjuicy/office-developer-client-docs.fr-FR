---
title: ITnefOpenTaggedBody
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.OpenTaggedBody
api_type:
- COM
ms.assetid: 70d5b34c-85b3-4d1f-860e-2838947ba428
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348733"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="6a0bc-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="6a0bc-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="6a0bc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6a0bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6a0bc-105">Ouvre une interface de flux sur le texte d’un message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="6a0bc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a0bc-106">Parameters</span></span>

 <span data-ttu-id="6a0bc-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="6a0bc-107">_lpMessage_</span></span>
  
> <span data-ttu-id="6a0bc-108">[in] Pointeur vers le message auquel le flux est associé.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="6a0bc-109">Ce message ne doit pas nécessairement être le même message que celui transmis dans l’appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="6a0bc-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="6a0bc-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6a0bc-110">_ulFlags_</span></span>
  
> <span data-ttu-id="6a0bc-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’interface de flux est ouverte.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="6a0bc-112">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="6a0bc-112">The following flags can be set:</span></span>
    
<span data-ttu-id="6a0bc-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="6a0bc-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="6a0bc-114">Si une propriété n’existe pas dans le message actuel, elle doit être créée.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="6a0bc-115">Si la propriété existe, les données actuelles de la propriété doivent être remplacées par les données du flux TNEF (Transport-Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="6a0bc-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="6a0bc-116">Lorsqu’une implémentation définit l’MAPI_CREATE, elle doit également définir l’MAPI_MODIFY’indicateur.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="6a0bc-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6a0bc-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="6a0bc-118">Demande une autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-118">Requests read/write permission.</span></span> <span data-ttu-id="6a0bc-119">L’interface par défaut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-119">The default interface is read-only.</span></span> <span data-ttu-id="6a0bc-120">MAPI_MODIFY doit être définie chaque fois que MAPI_CREATE est définie.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="6a0bc-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="6a0bc-121">_lppStream_</span></span>
  
> <span data-ttu-id="6a0bc-122">[out] Pointeur vers un pointeur vers un objet de flux qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du message encapsulé transmis et qui prend en charge l’interface [IStream.](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream)</span><span class="sxs-lookup"><span data-stu-id="6a0bc-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6a0bc-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6a0bc-123">Return value</span></span>

<span data-ttu-id="6a0bc-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="6a0bc-124">S_OK</span></span> 
  
> <span data-ttu-id="6a0bc-125">L’appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a0bc-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a0bc-126">Remarks</span></span>

<span data-ttu-id="6a0bc-127">Les fournisseurs de transport, les fournisseurs de magasins de messages et les passerelles appellent la méthode **ITnef::OpenTaggedBody** pour ouvrir une interface de flux sur le texte d’un message encapsulé (c’est-à-dire, sur un objet TNEF).</span><span class="sxs-lookup"><span data-stu-id="6a0bc-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="6a0bc-128">Dans le cadre de son traitement, **OpenTaggedBody** insère ou pare les balises de pièce jointe qui indiquent la position des pièces jointes ou des objets OLE dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="6a0bc-129">Les balises de pièce jointe sont au format suivant :</span><span class="sxs-lookup"><span data-stu-id="6a0bc-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="6a0bc-130">**[[** _nom de la pièce_ jointe **:** _n dans_ **le nom** _du conteneur de pièces jointes_ **]]**</span><span class="sxs-lookup"><span data-stu-id="6a0bc-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="6a0bc-131">_le nom de la_ pièce jointe décrit l’objet pièce jointe ;  _n_ est un nombre qui identifie la pièce jointe qui fait partie d’une séquence, incrémentant à partir de la valeur transmise dans le paramètre  _lpKey_ de la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; et  _le nom du conteneur de_ pièces jointes décrit le composant physique où réside l’objet pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="6a0bc-132">**OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe là où un objet pièce jointe apparaît dans le texte.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="6a0bc-133">Le texte du message d’origine n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="6a0bc-134">Lorsqu’un message avec des balises est transmis à un flux, les balises sont vidées et les objets en pièce jointe sont déplacés à la position des balises dans le flux.</span><span class="sxs-lookup"><span data-stu-id="6a0bc-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a0bc-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a0bc-135">See also</span></span>



[<span data-ttu-id="6a0bc-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="6a0bc-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="6a0bc-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="6a0bc-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="6a0bc-138">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="6a0bc-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="6a0bc-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a0bc-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

