---
title: Création de texte du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 70d1fb24-91a9-4043-8c9d-be1523012e6b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bd840c7bef0607db37c6477bd8f4a7320a8188c6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574754"
---
# <a name="creating-message-text"></a><span data-ttu-id="3d6aa-103">Création de texte du message</span><span class="sxs-lookup"><span data-stu-id="3d6aa-103">Creating message text</span></span>

<span data-ttu-id="3d6aa-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d6aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d6aa-105">Bien que certains messages sont composés de rien de plus qu’une liste de destinataires et une ligne d’objet, le contenu de la plupart des messages, spécifiquement IPM. Remarque Les messages, contient du texte.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-105">Although some messages are made up of nothing more than a recipient list and a subject line, the content of most messages, specifically IPM.Note messages, includes text.</span></span> <span data-ttu-id="3d6aa-106">Message texte peut être brut ou mise en forme et est stockée dans trois propriétés : **PR\_corps** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) et **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d6aa-106">Message text can be plain or formatted and is stored in three properties: **PR\_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), **PR\_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)), and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)).</span></span> 

<span data-ttu-id="3d6aa-107">Si votre client est basé sur le texte brut, définissez **PR\_BODY**.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-107">If your client is plain text-based, set **PR\_BODY**.</span></span> <span data-ttu-id="3d6aa-108">Si vous prenez en charge texte mis en forme dans le Format de texte enrichi (RTF), définir **PR_RTF_COMPRESSED** ou les deux **PR_RTF_COMPRESSED** et **PR\_corps**, selon le fournisseur de banque de messages que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-108">If you support formatted text in the Rich Text Format (RTF), set either **PR_RTF_COMPRESSED** only or both **PR_RTF_COMPRESSED** and **PR\_BODY**, depending on the message store provider that you are using.</span></span> <span data-ttu-id="3d6aa-109">Lorsqu’un client prenant en charge les RTF utilise une banque de messages RTF prenant en charge, il définit **PR_RTF_COMPRESSED** uniquement.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-109">When an RTF-aware client is using an RTF-aware message store, it sets **PR_RTF_COMPRESSED** only.</span></span> <span data-ttu-id="3d6aa-110">Lorsqu’un client prenant en charge les RTF utilise une banque de messages non compatible RICH, il définit les deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-110">When an RTF-aware client is using a non-RTF-aware message store, it sets both properties.</span></span> <span data-ttu-id="3d6aa-111">Si votre client prend en charge HTML, définissez la propriété **PR_HTML** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-111">If your client supports HTML, set the **PR_HTML** property.</span></span> 
  
## <a name="determine-whether-your-message-store-supports-rich-text-format"></a><span data-ttu-id="3d6aa-112">Déterminer si la banque de messages prend en charge le Format RTF</span><span class="sxs-lookup"><span data-stu-id="3d6aa-112">Determine whether your message store supports Rich Text Format</span></span>
  
1. <span data-ttu-id="3d6aa-113">Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3d6aa-113">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property.</span></span>
    
2. <span data-ttu-id="3d6aa-114">Recherchez le bit STORE_RTF_OK.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-114">Check for the STORE_RTF_OK bit.</span></span> <span data-ttu-id="3d6aa-115">Si STORE_RTF_OK est défini, le fournisseur de banque de message prend en charge le texte RTF.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-115">If STORE_RTF_OK is set, the message store provider supports RTF text.</span></span> <span data-ttu-id="3d6aa-116">Si elle n’est pas définie, le fournisseur de banque de message prend en charge uniquement en texte brut.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-116">If it is not set, the message store provider supports plain text only.</span></span>
    
## <a name="determine-whether-your-message-store-supports-html"></a><span data-ttu-id="3d6aa-117">Déterminer si la banque de messages prend en charge HTML</span><span class="sxs-lookup"><span data-stu-id="3d6aa-117">Determine whether your message store supports HTML</span></span>
  
1. <span data-ttu-id="3d6aa-118">Appeler la méthode de [IMAPIProp::GetProps](imapiprop-getprops.md) de la banque de messages pour récupérer la propriété **PR_STORE_SUPPORT_MASK** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-118">Call the message store's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
2. <span data-ttu-id="3d6aa-119">Recherchez le bit STORE_HTML_OK.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-119">Check for the STORE_HTML_OK bit.</span></span> <span data-ttu-id="3d6aa-120">Si STORE_HTML_OK est défini, le fournisseur de banque de message prend en charge le texte HTML.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-120">If STORE_HTML_OK is set, the message store provider supports HTML text.</span></span> 
    
## <a name="set-prrtfcompressed"></a><span data-ttu-id="3d6aa-121">Définir PR\_RTF_COMPRESSED</span><span class="sxs-lookup"><span data-stu-id="3d6aa-121">Set PR\_RTF_COMPRESSED</span></span>
  
1. <span data-ttu-id="3d6aa-122">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du message pour ouvrir la propriété **PR_RTF_COMPRESSED** , spécifiant IID_IStream comme l’identificateur d’interface et la définition de l’indicateur MAPI_CREATE.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-122">Call the message's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_RTF_COMPRESSED** property, specifying IID_IStream as the interface identifier and setting the MAPI_CREATE flag.</span></span> 
    
2. <span data-ttu-id="3d6aa-123">Appelez la fonction [WrapCompressedRTFStream](wrapcompressedrtfstream.md) , en passant l’indicateur STORE_UNCOMPRESSED_RTF si le bit STORE_UNCOMPRESSED_RTF est défini dans la propriété **PR_STORE_SUPPORT_MASK** du message.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-123">Call the [WrapCompressedRTFStream](wrapcompressedrtfstream.md) function, passing the STORE_UNCOMPRESSED_RTF flag if the STORE_UNCOMPRESSED_RTF bit is set in the message store's **PR_STORE_SUPPORT_MASK** property.</span></span> 
    
3. <span data-ttu-id="3d6aa-124">Publier le flux d’origine en appelant son ** IUnknown::Release ** méthode.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-124">Release the original stream by calling its ** IUnknown::Release ** method.</span></span> 
    
4. <span data-ttu-id="3d6aa-125">Appeler ** IStream::Write ** ou **IStream::CopyTo** pour écrire le texte du message dans le flux renvoyé par **WrapCompressedRTFStream**.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-125">Call either ** IStream::Write ** or **IStream::CopyTo** to write the message text to the stream returned from **WrapCompressedRTFStream**.</span></span>
    
5. <span data-ttu-id="3d6aa-126">Appeler les méthodes de **validation** et de **version** sur le flux retourné par la méthode **OpenProperty** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-126">Call the **Commit** and **Release** methods on the stream returned from the **OpenProperty** method.</span></span> 
    
<span data-ttu-id="3d6aa-127">À ce stade, si le fournisseur de banque de message prend en charge le format RTF, vous avez réalisé tout ce qui est requis.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-127">At this point, if the message store provider supports RTF, you have done all that is required.</span></span> <span data-ttu-id="3d6aa-128">Vous pouvez compter sur le fournisseur de banque de messages pour gérer la synchronisation du contenu du message et la mise en forme et créer la **PR\_corps** propriété si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-128">You can depend on the message store provider to handle synchronizing the message content and formatting and to create the **PR\_BODY** property if necessary.</span></span> <span data-ttu-id="3d6aa-129">Banques de messages RTF prenant en charge appellent [RTFSync](rtfsync.md) pour gérer la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-129">RTF-aware message stores call [RTFSync](rtfsync.md) to handle the synchronization.</span></span> <span data-ttu-id="3d6aa-130">Si le format RTF\_SYNC_BODY_CHANGED est défini sur TRUE, le fournisseur sera régénérer la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-130">If the RTF\_SYNC_BODY_CHANGED flag is set to TRUE, the provider will recompute the **PR_BODY** property.</span></span> 
  
<span data-ttu-id="3d6aa-131">Si votre fournisseur de magasin de message ne gère pas le format RTF, vous devez également ajouter le contenu des messages non RTF en définissant la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-131">If your message store provider does not support RTF, you must also add non-RTF message content by setting the **PR_BODY** property.</span></span> 
  
## <a name="set-prhtml"></a><span data-ttu-id="3d6aa-132">Set PR_HTML</span><span class="sxs-lookup"><span data-stu-id="3d6aa-132">Set PR_HTML</span></span>
  
1. <span data-ttu-id="3d6aa-133">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_HTML** avec l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-133">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_HTML** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="3d6aa-134">Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-134">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="3d6aa-135">Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-135">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    
## <a name="set-prbody"></a><span data-ttu-id="3d6aa-136">Définir PR_BODY</span><span class="sxs-lookup"><span data-stu-id="3d6aa-136">Set PR_BODY</span></span>
  
1. <span data-ttu-id="3d6aa-137">Appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété **PR_BODY** avec l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="3d6aa-137">Call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_BODY** property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="3d6aa-138">Appelez **IStream::Write** pour écrire les données de texte du message dans le flux renvoyé par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-138">Call **IStream::Write** to write the message text data to the stream returned from **OpenProperty**.</span></span> 
    
3. <span data-ttu-id="3d6aa-139">Appelez la fonction [RTFSync](rtfsync.md) pour synchroniser le texte avec la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-139">Call the [RTFSync](rtfsync.md) function to synchronize the text with the formatting.</span></span> <span data-ttu-id="3d6aa-140">Car il s’agit d’un nouveau message, définir des indicateurs de la RTF_SYNC_RTF_CHANGED et RTF_SYNC_BODY_CHANGED pour indiquer que le texte brut et RTF version du texte du message a été modifié.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-140">Because this is a new message, set both the RTF_SYNC_RTF_CHANGED and RTF_SYNC_BODY_CHANGED flags to indicate that both the RTF and plain text version of the message text has changed.</span></span> <span data-ttu-id="3d6aa-141">**RTFSync** sera définir plusieurs propriétés liées par le fournisseur de banque de messages, tel que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) et les enregistrer dans le message.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-141">**RTFSync** will set several related properties that the message store provider requires, such as **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)), and write them to the message.</span></span>
    
4. <span data-ttu-id="3d6aa-142">Appelez **IStream::Commit** et **IUnknown::Release** sur le flux pour valider les modifications et libérer la mémoire.</span><span class="sxs-lookup"><span data-stu-id="3d6aa-142">Call **IStream::Commit** and **IUnknown::Release** on the stream to commit the changes and free its memory.</span></span> 
    

