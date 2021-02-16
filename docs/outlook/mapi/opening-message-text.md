---
title: Ouverture du texte d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407535"
---
# <a name="opening-message-text"></a><span data-ttu-id="3ee31-103">Ouverture du texte d’un message</span><span class="sxs-lookup"><span data-stu-id="3ee31-103">Opening message text</span></span>

<span data-ttu-id="3ee31-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ee31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ee31-105">Le texte d’un message est stocké dans sa propriété **\_ PR BODY** ou PR **\_ RTF \_ COMPRESSED.**</span><span class="sxs-lookup"><span data-stu-id="3ee31-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="3ee31-106">Pour plus d’informations, voir **PR \_ BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR \_ HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR \_ RTF \_ COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3ee31-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="3ee31-107">Si vous ouvrez le format RTF (Rich Text Format), ouvrez **la \_ RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="3ee31-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="3ee31-108">Si vous ne le faites pas, ouvrez **PR \_ BODY.**</span><span class="sxs-lookup"><span data-stu-id="3ee31-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="3ee31-109">Étant donné que le texte d’un message peut être grand, qu’il soit formaté ou non, utilisez **IMAPIProp::OpenProperty** pour ouvrir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3ee31-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="3ee31-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3ee31-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="3ee31-111">Pour afficher le texte d’un message formaté</span><span class="sxs-lookup"><span data-stu-id="3ee31-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="3ee31-112">Si vous utilisez une magasin de messages non RTF, comme indiqué par l’absence de l’indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)de la boutique :</span><span class="sxs-lookup"><span data-stu-id="3ee31-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="3ee31-113">Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer **PR_RTF_IN_SYNC** propriété.</span><span class="sxs-lookup"><span data-stu-id="3ee31-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="3ee31-114">Pour plus d’informations, voir [IMAPIProp::GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3ee31-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="3ee31-115">Appelez RTFSync pour synchroniser la propriété PR_BODY message avec la **PR_RTF_COMPRESSED** de message.</span><span class="sxs-lookup"><span data-stu-id="3ee31-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="3ee31-116">Pour plus d’informations, [voir RTFSync,](rtfsync.md) **PR_BODY** et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="3ee31-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="3ee31-117">Passez l’RTF_SYNC_BODY_CHANGED si l’appel de  récupération PR_RTF_IN_SYNC échoué parce que la propriété n’existe pas ou qu’elle est définie sur FALSE.</span><span class="sxs-lookup"><span data-stu-id="3ee31-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="3ee31-118">Si **RTFSync** a renvoyé TRUE, indiquant que des modifications ont été apportées, appelez la méthode **IMAPIProp::SaveChanges** du message pour les stocker définitivement.</span><span class="sxs-lookup"><span data-stu-id="3ee31-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="3ee31-119">Pour plus d’informations, [voir IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="3ee31-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="3ee31-120">Que vous utilisiez ou non une magasin de messages rtF :</span><span class="sxs-lookup"><span data-stu-id="3ee31-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="3ee31-121">Appelez **IMAPIProp::OpenProperty** pour ouvrir **PR_RTF_COMPRESSED** propriété.</span><span class="sxs-lookup"><span data-stu-id="3ee31-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="3ee31-122">Pour plus d’informations, [voir IMAPIProp::OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="3ee31-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="3ee31-123">Si **PR_RTF_COMPRESSED** n’est pas disponible, appelez **OpenProperty** pour ouvrir **PR_BODY** propriété.</span><span class="sxs-lookup"><span data-stu-id="3ee31-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="3ee31-124">Appelez la **fonction WrapCompressedRTFStream** pour créer une version non compressée des données RTF compressées, si disponible.</span><span class="sxs-lookup"><span data-stu-id="3ee31-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="3ee31-125">Pour plus d’informations, [voir WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="3ee31-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="3ee31-126">Copiez le texte formaté du flux à l’endroit approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="3ee31-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="3ee31-127">Pour afficher du texte de message simple</span><span class="sxs-lookup"><span data-stu-id="3ee31-127">To display plain message text</span></span>
  
1. <span data-ttu-id="3ee31-128">Appelez la méthode **IMAPIProp::GetProps** du message pour récupérer PR_BODY **propriété.**</span><span class="sxs-lookup"><span data-stu-id="3ee31-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="3ee31-129">Pour plus d’informations, [voir IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="3ee31-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="3ee31-130">Si **GetProps** renvoie une PT_ERROR pour le type de propriété dans la structure de valeurs de propriété ou MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode **IMAPIProp::OpenProperty** du message.</span><span class="sxs-lookup"><span data-stu-id="3ee31-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="3ee31-131">Passez **PR_BODY** en tant que balise de propriété et IID_IStream comme identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="3ee31-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="3ee31-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="3ee31-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="3ee31-133">Copiez le texte simple du flux à l’endroit approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="3ee31-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

