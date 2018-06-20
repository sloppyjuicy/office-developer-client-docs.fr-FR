---
title: Texte du message d’ouverture
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ad3499cc1ff3bd8b633fa48173ab8455d5d8d124
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784935"
---
# <a name="opening-message-text"></a><span data-ttu-id="b3c4d-103">Texte du message d’ouverture</span><span class="sxs-lookup"><span data-stu-id="b3c4d-103">Opening message text</span></span>

<span data-ttu-id="b3c4d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3c4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3c4d-105">Le texte d’un message est stocké dans son **PR\_corps** propriété ou **PR\_RTF\_compressés** propriété.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="b3c4d-106">Pour plus d’informations, voir **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), et **PR\_RTF\_compressés** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="b3c4d-107">Si vous prenez en charge le Format de texte enrichi (RTF), ouvrez **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="b3c4d-108">Si vous ne prennent pas en charge les RTF, ouvrez **PR\_BODY**.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="b3c4d-109">Le texte d’un message pouvant être volumineux, quel que soit ou non mis en forme, utilisez **IMAPIProp::OpenProperty** pour ouvrir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="b3c4d-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="b3c4d-111">Pour afficher le texte du message mis en forme</span><span class="sxs-lookup"><span data-stu-id="b3c4d-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="b3c4d-112">Si vous utilisez une banque de messages connaissance non RTF, comme indiqué par l’absence de l’indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la banque :</span><span class="sxs-lookup"><span data-stu-id="b3c4d-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="b3c4d-113">Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer la propriété **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="b3c4d-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="b3c4d-114">Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="b3c4d-115">Appelez RTFSync pour synchroniser la propriété du message PR_BODY avec la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="b3c4d-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="b3c4d-116">Pour plus d’informations, voir [RTFSync](rtfsync.md) **PR_BODY**et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="b3c4d-117">Passe le RTF_SYNC_BODY_CHANGED signale si l’appel à récupérer **PR_RTF_IN_SYNC** a échoué, car la propriété n’existe pas ou qu’il est défini sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="b3c4d-118">Si **RTFSync** renvoie la valeur TRUE, indiquant que les modifications ont été apportées, appeler la méthode de **IMAPIProp::SaveChanges** du message pour les stocker définitivement.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="b3c4d-119">Pour plus d’informations, voir [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="b3c4d-120">Quel que soit ou non, vous utilisez un message au format RTF prenant en charge stocker :</span><span class="sxs-lookup"><span data-stu-id="b3c4d-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="b3c4d-121">Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="b3c4d-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="b3c4d-122">Pour plus d’informations, voir [IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="b3c4d-123">Si **PR_RTF_COMPRESSED** n’est pas disponible, appelez **OpenProperty** pour ouvrir la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="b3c4d-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="b3c4d-124">Appelez la fonction **WrapCompressedRTFStream** pour créer une version non compressée des données au format RTF compressées, si elle est disponible.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="b3c4d-125">Pour plus d’informations, voir [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="b3c4d-126">Copiez le texte mis en forme à partir du flux à l’emplacement approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="b3c4d-127">Pour afficher le texte du message brut</span><span class="sxs-lookup"><span data-stu-id="b3c4d-127">To display plain message text</span></span>
  
1. <span data-ttu-id="b3c4d-128">Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="b3c4d-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="b3c4d-129">Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="b3c4d-130">Si **GetProps** renvoie soit PT_ERROR pour le type de propriété dans la structure de valeur de propriété ou d’un MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode de **IMAPIProp::OpenProperty** du message.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="b3c4d-131">Transmettez **PR_BODY** , ainsi que la balise de propriété IID_IStream l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="b3c4d-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="b3c4d-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="b3c4d-133">Copiez le texte brut à partir du flux à l’emplacement approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="b3c4d-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

