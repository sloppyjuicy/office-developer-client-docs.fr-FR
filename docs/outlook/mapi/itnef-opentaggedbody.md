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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 154d6e4a4e333f3a6165c3875bdcd57957ebf70c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348733"
---
# <a name="itnefopentaggedbody"></a><span data-ttu-id="03556-103">ITnef::OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="03556-103">ITnef::OpenTaggedBody</span></span>

  
  
<span data-ttu-id="03556-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03556-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03556-105">Ouvre une interface de flux sur le texte d'un message encapsulé.</span><span class="sxs-lookup"><span data-stu-id="03556-105">Opens a stream interface on the text of an encapsulated message.</span></span>
  
```cpp
HRESULT OpenTaggedBody(
  LPMESSAGE lpMessage,
  ULONG ulFlags,
  LPSTREAM FAR * lppStream
);
```

## <a name="parameters"></a><span data-ttu-id="03556-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="03556-106">Parameters</span></span>

 <span data-ttu-id="03556-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="03556-107">_lpMessage_</span></span>
  
> <span data-ttu-id="03556-108">dans Pointeur vers le message auquel le flux est associé.</span><span class="sxs-lookup"><span data-stu-id="03556-108">[in] A pointer to the message with which the stream is associated.</span></span> <span data-ttu-id="03556-109">Ce message ne doit pas obligatoirement être le même message que celui transmis dans l'appel à la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="03556-109">This message is not required to be the same message that is passed in the call to the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
 <span data-ttu-id="03556-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="03556-110">_ulFlags_</span></span>
  
> <span data-ttu-id="03556-111">dans Masque de des indicateurs qui contrôle la manière dont l'interface de flux est ouverte.</span><span class="sxs-lookup"><span data-stu-id="03556-111">[in] A bitmask of flags that controls how the stream interface is opened.</span></span> <span data-ttu-id="03556-112">Les indicateurs suivants peuvent être définis:</span><span class="sxs-lookup"><span data-stu-id="03556-112">The following flags can be set:</span></span>
    
<span data-ttu-id="03556-113">MAPI_CREATE</span><span class="sxs-lookup"><span data-stu-id="03556-113">MAPI_CREATE</span></span> 
  
> <span data-ttu-id="03556-114">Si une propriété n'existe pas dans le message actif, elle doit être créée.</span><span class="sxs-lookup"><span data-stu-id="03556-114">If a property does not exist in the current message, it should be created.</span></span> <span data-ttu-id="03556-115">Si la propriété existe, les données actuelles de la propriété doivent être remplacées par les données du flux TNEF (Transport-Neutral Encapsulation Format).</span><span class="sxs-lookup"><span data-stu-id="03556-115">If the property does exist, the current data in the property should be replaced with the data from the Transport-Neutral Encapsulation Format (TNEF) stream.</span></span> <span data-ttu-id="03556-116">Lorsqu'une implémentation définit l'indicateur MAPI_CREATE, elle doit également définir l'indicateur MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="03556-116">When an implementation sets the MAPI_CREATE flag, it should also set the MAPI_MODIFY flag.</span></span>
    
<span data-ttu-id="03556-117">MAPI_MODIFY</span><span class="sxs-lookup"><span data-stu-id="03556-117">MAPI_MODIFY</span></span> 
  
> <span data-ttu-id="03556-118">Demande une autorisation en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="03556-118">Requests read/write permission.</span></span> <span data-ttu-id="03556-119">L'interface par défaut est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03556-119">The default interface is read-only.</span></span> <span data-ttu-id="03556-120">MAPI_MODIFY doit être défini à chaque fois que MAPI_CREATE est défini.</span><span class="sxs-lookup"><span data-stu-id="03556-120">MAPI_MODIFY must be set whenever MAPI_CREATE is set.</span></span>
    
 <span data-ttu-id="03556-121">_lppStream_</span><span class="sxs-lookup"><span data-stu-id="03556-121">_lppStream_</span></span>
  
> <span data-ttu-id="03556-122">remarquer Pointeur vers un pointeur vers un objet Stream qui contient le texte de la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) du message encapsulé transmis et qui prend en charge l'interface [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) .</span><span class="sxs-lookup"><span data-stu-id="03556-122">[out] A pointer to a pointer to a stream object that contains the text from the **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) property of the passed-in encapsulated message and that supports the [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) interface.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03556-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="03556-123">Return value</span></span>

<span data-ttu-id="03556-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="03556-124">S_OK</span></span> 
  
> <span data-ttu-id="03556-125">L'appel a réussi et a renvoyé la ou les valeurs attendues.</span><span class="sxs-lookup"><span data-stu-id="03556-125">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03556-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="03556-126">Remarks</span></span>

<span data-ttu-id="03556-127">Les fournisseurs de transport, les fournisseurs de banques de messages et les passerelles appellent la méthode **ITnef:: OpenTaggedBody** pour ouvrir une interface de flux sur le texte d'un message encapsulé (c'est-à-dire sur un objet TNEF).</span><span class="sxs-lookup"><span data-stu-id="03556-127">Transport providers, message store providers, and gateways call the **ITnef::OpenTaggedBody** method to open a stream interface on the text of an encapsulated message (that is, on a TNEF object).</span></span> 
  
<span data-ttu-id="03556-128">Dans le cadre de son traitement, **OpenTaggedBody** insère ou analyse les balises de pièce jointe qui indiquent la position des pièces jointes ou des objets OLE dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="03556-128">As part of its processing, **OpenTaggedBody** either inserts or parses attachment tags that indicate the position of any attachments or OLE objects in the message text.</span></span> <span data-ttu-id="03556-129">Les balises de pièces jointes sont au format suivant:</span><span class="sxs-lookup"><span data-stu-id="03556-129">The attachment tags are in the following format:</span></span> 
  
 <span data-ttu-id="03556-130">**[[** _nom de la pièce jointe_ **:** _n_ **dans le nom du conteneur de** _pièces jointes_ **]]**</span><span class="sxs-lookup"><span data-stu-id="03556-130">**[[** _attachment name_ **:** _n_ **in** _attachment container name_ **]]**</span></span>
  
 <span data-ttu-id="03556-131">_nom_ de la pièce jointe décrit l'objet Attachment;  _n_ est un nombre qui identifie la pièce jointe qui fait partie d'une séquence, incrémentant à partir de la valeur transmise dans le paramètre _lpKey_ de la fonction [OpenTnefStream](opentnefstream.md) ou [OpenTnefStreamEx](opentnefstreamex.md) ; et _nom du conteneur de pièces jointes_ décrit le composant physique où réside l'objet pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="03556-131">_attachment name_ describes the attachment object;  _n_ is a number that identifies the attachment that is part of a sequence, incrementing from the value passed in the  _lpKey_ parameter of the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function; and  _attachment container name_ describes the physical component where the attachment object resides.</span></span> 
  
 <span data-ttu-id="03556-132">**OpenTaggedBody** lit le texte du message et insère une balise de pièce jointe à l'emplacement où un objet pièce jointe s'affichait à l'origine dans le texte.</span><span class="sxs-lookup"><span data-stu-id="03556-132">**OpenTaggedBody** reads out message text and inserts an attachment tag wherever an attachment object originally appeared in the text.</span></span> <span data-ttu-id="03556-133">Le texte du message d'origine n'est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="03556-133">The original message text is not changed.</span></span> 
  
<span data-ttu-id="03556-134">Lorsqu'un message comportant des balises est transmis à un objet Stream, les balises sont supprimées et les objets Attachment sont déplacés dans la position des balises dans le flux.</span><span class="sxs-lookup"><span data-stu-id="03556-134">When a message that has tags is passed to a stream, the tags are stripped out and the attachment objects are relocated in the position of the tags in the stream.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="03556-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="03556-135">See also</span></span>



[<span data-ttu-id="03556-136">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="03556-136">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="03556-137">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="03556-137">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="03556-138">Propriété canonique PidTagBody</span><span class="sxs-lookup"><span data-stu-id="03556-138">PidTagBody Canonical Property</span></span>](pidtagbody-canonical-property.md)
  
[<span data-ttu-id="03556-139">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="03556-139">ITnef : IUnknown</span></span>](itnefiunknown.md)

