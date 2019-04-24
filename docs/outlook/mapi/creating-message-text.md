---
title: Création d’un texte de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5b4a4107d6326a61f50a4023ebc2538f699224b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335719"
---
# <a name="creating-message-text"></a><span data-ttu-id="59798-103">Création d’un texte de message</span><span class="sxs-lookup"><span data-stu-id="59798-103">Creating message text</span></span>

<span data-ttu-id="59798-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59798-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59798-105">Bien que certains messages soient constitués de rien de plus qu'une liste de destinataires et d'une ligne d'objet, le contenu de la plupart des messages, en particulier IPM. Remarque les messages, y compris le texte.</span><span class="sxs-lookup"><span data-stu-id="59798-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="59798-106">Le texte du message peut être brut ou mis en forme et stocké dans trois propriétés: **PR\_Body** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_html** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59798-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="59798-107">Si votre client est en texte brut, définissez **PR\_Body**.</span><span class="sxs-lookup"><span data-stu-id="59798-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="59798-108">Si vous prenez en charge le texte mis en forme au format RTF (Rich Text Format), définissez **PR_RTF_COMPRESSED** uniquement ou **PR_RTF_COMPRESSED** et **PR\_Body**, selon le fournisseur de banque de messages que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="59798-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="59798-109">Lorsqu'un client compatible RTF utilise un magasin de messages compatible avec le format RTF, il définit **PR_RTF_COMPRESSED** uniquement.</span><span class="sxs-lookup"><span data-stu-id="59798-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="59798-110">Lorsqu'un client compatible RTF utilise un magasin de messages non compatible RTF, il définit les deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="59798-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="59798-111">Si votre client prend en charge le format HTML, définissez la propriété **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="59798-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="59798-112">Déterminer si votre magasin de messages prend en charge le format RTF</span><span class="sxs-lookup"><span data-stu-id="59798-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="59798-113">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="59798-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="59798-114">Vérifiez le bit STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="59798-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="59798-115">Si STORE_RTF_OK est défini, le fournisseur de banque de messages prend en charge le texte RTF.</span><span class="sxs-lookup"><span data-stu-id="59798-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="59798-116">S'il n'est pas défini, le fournisseur de banque de messages prend en charge uniquement le texte brut.</span><span class="sxs-lookup"><span data-stu-id="59798-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="59798-117">Déterminer si votre magasin de messages prend en charge le format HTML</span><span class="sxs-lookup"><span data-stu-id="59798-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="59798-118">Appelez la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) de la Banque de messages pour extraire la propriété **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="59798-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="59798-119">Vérifiez le bit STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="59798-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="59798-120">Si STORE_HTML_OK est défini, le fournisseur de banque de messages prend en charge le texte HTML.</span><span class="sxs-lookup"><span data-stu-id="59798-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="59798-121">Définir PR\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="59798-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="59798-122">Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_RTF_COMPRESSED** , en spécifiant IID_IStream comme identificateur d'interface et en définissant l'indicateur MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="59798-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="59798-123">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en transmettant l'indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est défini dans la propriété **PR_STORE_SUPPORT_MASK** de la Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="59798-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="59798-124">Libérez le flux d'origine en appelant sa méthode \* \* IUnknown:: Release \* \*.</span><span class="sxs-lookup"><span data-stu-id="59798-124">Release the original stream by calling its \*\* IUnknown::Release \*\* method.</span></span> 
    
4. <span data-ttu-id="59798-125">Appelez soit \* \* IStream:: Write \* \* ou **IStream:: CopyTo** pour écrire le texte du message dans le flux renvoyé à partir de **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="59798-125">Call either \*\* IStream::Write \*\* or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="59798-126">Appelez les méthodes **Commit** et **Release** sur le flux renvoyé par la méthode **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="59798-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="59798-127">À ce stade, si le fournisseur de banque de messages prend en charge le format RTF, vous avez réalisé tout ce qui est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="59798-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="59798-128">Vous pouvez dépendre du fournisseur de banque de messages pour gérer la synchronisation du contenu et de la mise en forme du message et pour créer la propriété **PR\_Body** si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="59798-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="59798-129">Les banques de messages prenant en charge le format RTF appellent [RTFSync](rtfsync.md) pour gérer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="59798-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="59798-130">Si l'indicateur\_SYNC_BODY_CHANGED RTF est défini sur true, le fournisseur recalcule la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="59798-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="59798-131">Si votre fournisseur de banque de messages ne prend pas en charge le format RTF, vous devez également ajouter du contenu de message non RTF en définissant la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="59798-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="59798-132">Définir PR_HTML</span><span class="sxs-lookup"><span data-stu-id="59798-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="59798-133">Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec l'interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="59798-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="59798-134">Appelez **IStream:: Write** pour écrire les données de texte du message dans le flux renvoyé à partir de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="59798-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="59798-135">Appelez **IStream:: Commit** et **IUnknown:: Release** sur le flux pour valider les modifications et libérer sa mémoire.</span><span class="sxs-lookup"><span data-stu-id="59798-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="59798-136">Définir PR_BODY</span><span class="sxs-lookup"><span data-stu-id="59798-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="59798-137">Appelez la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec l'interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="59798-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="59798-138">Appelez **IStream:: Write** pour écrire les données de texte du message dans le flux renvoyé à partir de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="59798-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="59798-139">Appelez la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="59798-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="59798-140">Étant donné qu'il s'agit d'un nouveau message, définissez les indicateurs RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que la version au format RTF et texte brut du texte du message a changé.</span><span class="sxs-lookup"><span data-stu-id="59798-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="59798-141">**RTFSync** définit plusieurs propriétés connexes requises par le fournisseur de banque de messages, telles que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), et les écrit dans le message.</span><span class="sxs-lookup"><span data-stu-id="59798-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="59798-142">Appelez **IStream:: Commit** et **IUnknown:: Release** sur le flux pour valider les modifications et libérer sa mémoire.</span><span class="sxs-lookup"><span data-stu-id="59798-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

