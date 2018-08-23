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
ms.openlocfilehash: 14964f367e3dbca484c4e1612b374a6a72ddf17b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593780"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="dc2f5-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="dc2f5-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="dc2f5-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dc2f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dc2f5-105">Ouvre une interface de flux sur le texte d’un message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="dc2f5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc2f5-106">Parameters</span></span>

 <span data-ttu-id="dc2f5-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="dc2f5-107">_lpMessage_</span></span>
  
> <span data-ttu-id="dc2f5-108">[in] Pointeur vers le message auquel l’objet stream est associé.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="dc2f5-109">Ce message n’est pas requis pour être le même message est passé dans l’appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="dc2f5-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="dc2f5-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dc2f5-110">_ulFlags_</span></span>
  
> <span data-ttu-id="dc2f5-111">[in] Masque de bits d’indicateurs qui contrôle la façon dont l’interface du flux est ouvert.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="dc2f5-112">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="dc2f5-112">The following flags can be set:</span></span>
    
<span data-ttu-id="dc2f5-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="dc2f5-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="dc2f5-114">Si une propriété n’existe pas dans le message en cours, il doit être créé.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="dc2f5-115">Si la propriété n’existe pas, les données actuelles de la propriété doivent être remplacées par les données à partir du flux de Transport-Neutral Encapsulation Format (TNEF).</span><span class="sxs-lookup"><span data-stu-id="dc2f5-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="dc2f5-116">Lorsqu’une implémentation définit l’indicateur MAPI_CREATE, il doit également affecter l’indicateur ne.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="dc2f5-117">N'</span><span class="sxs-lookup"><span data-stu-id="dc2f5-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="dc2f5-118">Demandes d’autorisation de lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-118">Requests read/write permission.</span></span> <span data-ttu-id="dc2f5-119">L’interface par défaut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-119">The default interface is read-only.</span></span> <span data-ttu-id="dc2f5-120">Ne doit être définie chaque fois que MAPI_CREATE est défini.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="dc2f5-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="dc2f5-121">_lppStream_</span></span>
  
> <span data-ttu-id="dc2f5-122">[out] Un pointeur vers un pointeur vers un objet stream qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du passé en encapsulé message et qui prend en charge l’interface [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="dc2f5-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/en-us/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dc2f5-123">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dc2f5-123">Return value</span></span>

<span data-ttu-id="dc2f5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc2f5-124">S_OK</span></span> 
  
> <span data-ttu-id="dc2f5-125">L’appel a réussi et renvoyé la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc2f5-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="dc2f5-126">Remarks</span></span>

<span data-ttu-id="dc2f5-127">Fournisseurs de transport, les fournisseurs de banque de message et passerelles appellent la méthode **ITnef::OpenTaggedBody** pour ouvrir une interface de flux sur le texte d’un message encapsulé (autrement dit, un TNEF d’objets).</span><span class="sxs-lookup"><span data-stu-id="dc2f5-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="dc2f5-128">Dans le cadre de son traitement, **OpenTaggedBody** insère ou analyse des balises de pièce jointe qui indiquent la position des pièces jointes ou les objets OLE dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="dc2f5-129">Les balises de pièce jointe sont dans le format suivant :</span><span class="sxs-lookup"><span data-stu-id="dc2f5-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="dc2f5-130">**[[** ** _nom de la pièce jointe_ **:** _n_ _nom de conteneur de pièce jointe_ ** **]]**</span><span class="sxs-lookup"><span data-stu-id="dc2f5-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="dc2f5-131">_nom de la pièce jointe_ décrit l’objet de pièce jointe ;  _n_ est un numéro qui identifie la pièce jointe qui fait partie d’une séquence, s’incrémentant à partir de la valeur passée dans le paramètre _lpKey_ du [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) fonction ; et _le nom de conteneur pièce jointe_ décrit le composant physique où réside l’objet attachment.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="dc2f5-132">**OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe partout où un objet attachment s’affichait dans le texte.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="dc2f5-133">Le texte du message d’origine n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="dc2f5-134">Lorsqu’un message qui comporte des balises est passé à un flux de données, les balises sont supprimés et les objets attachment sont déplacés dans la position des balises dans le flux.</span><span class="sxs-lookup"><span data-stu-id="dc2f5-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc2f5-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc2f5-135">See also</span></span>



[<span data-ttu-id="dc2f5-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="dc2f5-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="dc2f5-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="dc2f5-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="dc2f5-138">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="dc2f5-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="dc2f5-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dc2f5-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

