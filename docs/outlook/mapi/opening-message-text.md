---
title: Ouverture du texte d’un message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e37fc9d8-433b-41b4-84f2-42a952063f35
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 305b0534f828ea72c1e116fd38fb8f578062e32e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348579"
---
# <a name="opening-message-text"></a><span data-ttu-id="1c8ff-103">Ouverture du texte d’un message</span><span class="sxs-lookup"><span data-stu-id="1c8ff-103">Opening message text</span></span>

<span data-ttu-id="1c8ff-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c8ff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c8ff-105">Le texte d'un message est stocké dans sa **propriété\_PR Body** ou sa propriété **\_\_Compressed PR** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-105">The text of a message is stored either in its **PR\_BODY** property or **PR\_RTF\_COMPRESSED** property.</span></span> <span data-ttu-id="1c8ff-106">Pour plus d'informations, reportez-vous à la rubrique **\_PR Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_html** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR\_Rich RTF\_compressé** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-106">For more information, see **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR\_RTF\_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="1c8ff-107">Si vous prenez en charge le format RTF (Rich Text Format), ouvrez **PR\_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-107">If you support the Rich Text Format (RTF), open **PR\_RTF_COMPRESSED**.</span></span> <span data-ttu-id="1c8ff-108">Si vous ne prenez pas en charge le format RTF, ouvrez le **\_corps du message**.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-108">If you do not support RTF, open **PR\_BODY**.</span></span> <span data-ttu-id="1c8ff-109">Étant donné que le texte d'un message peut être volumineux, qu'il soit ou non mis en forme, utilisez **IMAPIProp:: OpenProperty** pour ouvrir ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-109">Because the text of a message can be large regardless of whether or not it is formatted, use **IMAPIProp::OpenProperty** to open these properties.</span></span> <span data-ttu-id="1c8ff-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-110">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
  
### <a name="to-display-formatted-message-text"></a><span data-ttu-id="1c8ff-111">Pour afficher le texte du message mis en forme</span><span class="sxs-lookup"><span data-stu-id="1c8ff-111">To display formatted message text</span></span>
  
1. <span data-ttu-id="1c8ff-112">Si vous utilisez une banque de messages non compatible avec le format RTF, comme indiqué par l'absence de l'indicateur STORE_RTF_OK dans la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque:</span><span class="sxs-lookup"><span data-stu-id="1c8ff-112">If you are using a non-RTF aware message store, as indicated by the absence of the STORE_RTF_OK flag in the store's **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
    
    1. <span data-ttu-id="1c8ff-113">Appelez la méthode **IMAPIProp:: GetProps** pour récupérer la propriété **PR_RTF_IN_SYNC** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-113">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_RTF_IN_SYNC** property.</span></span> <span data-ttu-id="1c8ff-114">Pour plus d'informations, voir [IMAPIProp:: GetProps](imapiprop-getprops.md) et **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-114">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md) and **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)).</span></span>
        
    2. <span data-ttu-id="1c8ff-115">Appelez RTFSync pour synchroniser la propriété PR_BODY du message avec la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-115">Call RTFSync to synchronize the message's PR_BODY property with the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1c8ff-116">Pour plus d'informations, voir [RTFSync](rtfsync.md), **PR_BODY**et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-116">For more information, see [RTFSync](rtfsync.md), **PR_BODY**, and **PR_RTF_COMPRESSED**.</span></span> <span data-ttu-id="1c8ff-117">TransMettez l'indicateur RTF_SYNC_BODY_CHANGED si l'appel de récupération de **PR_RTF_IN_SYNC** a échoué car la propriété n'existe pas ou est définie sur false.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-117">Pass the RTF_SYNC_BODY_CHANGED flag if the call to retrieve **PR_RTF_IN_SYNC** failed because the property does not exist or it is set to FALSE.</span></span> 
        
    3. <span data-ttu-id="1c8ff-118">Si **RTFSync** a renvoyé la valeur true, ce qui indique que des modifications ont été apportées, appelez la méthode **IMAPIProp:: SaveChanges** pour les stocker définitivement.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-118">If **RTFSync** returned TRUE — indicating that changes were made — call the message's **IMAPIProp::SaveChanges** method to permanently store them.</span></span> <span data-ttu-id="1c8ff-119">Pour plus d'informations, voir [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-119">For more information, see [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span>
    
2. <span data-ttu-id="1c8ff-120">Que vous utilisiez ou non une banque de messages prenant en charge le format RTF:</span><span class="sxs-lookup"><span data-stu-id="1c8ff-120">Regardless of whether or not you are using an RTF-aware message store:</span></span>
    
    1. <span data-ttu-id="1c8ff-121">Appelez **IMAPIProp:: OpenProperty** pour ouvrir la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-121">Call **IMAPIProp::OpenProperty** to open the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1c8ff-122">Pour plus d'informations, voir [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) et **PR_RTF_COMPRESSED**.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-122">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and **PR_RTF_COMPRESSED**.</span></span>
        
    2. <span data-ttu-id="1c8ff-123">Si **PR_RTF_COMPRESSED** n'est pas disponible, appelez **OpenProperty** pour ouvrir la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-123">If **PR_RTF_COMPRESSED** is not available, call **OpenProperty** to open the **PR_BODY** property.</span></span> 
        
    3. <span data-ttu-id="1c8ff-124">Appelez la fonction **WrapCompressedRTFStream** pour créer une version non compressée des données RTF compressées, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-124">Call the **WrapCompressedRTFStream** function to create an uncompressed version of the compressed RTF data, if available.</span></span> <span data-ttu-id="1c8ff-125">Pour plus d'informations, consultez la rubrique [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-125">For more information, see [WrapCompressedRTFStream](wrapcompressedrtfstream.md).</span></span>
        
    4. <span data-ttu-id="1c8ff-126">Copiez le texte mis en forme à partir du flux vers l'emplacement approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-126">Copy the formatted text from the stream to the appropriate place in the message form.</span></span> 
    
### <a name="to-display-plain-message-text"></a><span data-ttu-id="1c8ff-127">Pour afficher le texte d'un message brut</span><span class="sxs-lookup"><span data-stu-id="1c8ff-127">To display plain message text</span></span>
  
1. <span data-ttu-id="1c8ff-128">Appelez la méthode **IMAPIProp:: GetProps** pour récupérer la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="1c8ff-128">Call the message's **IMAPIProp::GetProps** method to retrieve the **PR_BODY** property.</span></span> <span data-ttu-id="1c8ff-129">Pour plus d'informations, voir [IMAPIProp:: GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-129">For more information, see [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
    
2. <span data-ttu-id="1c8ff-130">Si **GetProps** renvoie soit PT_ERROR pour le type de propriété dans la structure de la valeur de la propriété, soit MAPI_E_NOT_ENOUGH_MEMORY, appelez la méthode **IMAPIProp:: OpenProperty** du message.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-130">If **GetProps** returns either PT_ERROR for the property type in the property value structure or MAPI_E_NOT_ENOUGH_MEMORY, call the message's **IMAPIProp::OpenProperty** method.</span></span> <span data-ttu-id="1c8ff-131">TransMettez **PR_BODY** comme balise de propriété et IID_IStream comme identificateur d'interface.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-131">Pass **PR_BODY** as the property tag and IID_IStream as the interface identifier.</span></span> <span data-ttu-id="1c8ff-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="1c8ff-132">For more information, see [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span>
    
3. <span data-ttu-id="1c8ff-133">Copiez le texte brut du flux vers l'emplacement approprié dans le formulaire de message.</span><span class="sxs-lookup"><span data-stu-id="1c8ff-133">Copy the plain text from the stream to the appropriate place in the message form.</span></span> 
    

