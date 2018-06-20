---
title: Création d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: eef42a8c7d19af313316bea68624ac67fb1ab4e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783112"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="e3d68-103">Création d’une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="e3d68-103">Creating a message attachment</span></span>
  
<span data-ttu-id="e3d68-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e3d68-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e3d68-105">Une pièce jointe du message est certaines données supplémentaires, comme un fichier, un autre message ou un objet OLE, que vous pouvez envoyer ou enregistrer avec un message.</span><span class="sxs-lookup"><span data-stu-id="e3d68-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="e3d68-106">Chaque pièce jointe est une collection de propriétés qui identifie et décrit le type et la façon dont il s’affiche.</span><span class="sxs-lookup"><span data-stu-id="e3d68-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="e3d68-107">Comme destinataires, pièces jointes des messages uniquement accessible via le message auquel ils appartiennent.</span><span class="sxs-lookup"><span data-stu-id="e3d68-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="e3d68-108">Par conséquent, pour une pièce jointe utilisable, son message doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="e3d68-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="e3d68-109">Créer une pièce jointe</span><span class="sxs-lookup"><span data-stu-id="e3d68-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="e3d68-110">Appelez la méthode [IMessage::CreateAttach](imessage-createattach.md) du message et passer la valeur NULL en tant que l’identificateur d’interface.</span><span class="sxs-lookup"><span data-stu-id="e3d68-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="e3d68-111">**CreateAttach** renvoie un numéro qui identifie de manière unique la nouvelle pièce jointe du message.</span><span class="sxs-lookup"><span data-stu-id="e3d68-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="e3d68-112">Le nombre de pièces jointes est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) et est valide uniquement tant que le message contenant la pièce jointe est ouvert.</span><span class="sxs-lookup"><span data-stu-id="e3d68-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="e3d68-113">Appelez [IMAPIProp::SetProps](imapiprop-setprops.md) pour définir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) pour indiquer comment accéder à la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e3d68-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="e3d68-114">**PR_ATTACH_METHOD** est requis.</span><span class="sxs-lookup"><span data-stu-id="e3d68-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="e3d68-115">Affectez-lui la valeur :</span><span class="sxs-lookup"><span data-stu-id="e3d68-115">Set it to:</span></span> 
    
   - <span data-ttu-id="e3d68-116">ATTACH_BY_VALUE s’il s’agit des données binaires.</span><span class="sxs-lookup"><span data-stu-id="e3d68-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="e3d68-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY si la pièce jointe est un fichier.</span><span class="sxs-lookup"><span data-stu-id="e3d68-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="e3d68-118">ATTACH_EMBEDDED_MSG si la pièce jointe est un message.</span><span class="sxs-lookup"><span data-stu-id="e3d68-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="e3d68-119">ATTACH_OLE si la pièce jointe est un objet OLE.</span><span class="sxs-lookup"><span data-stu-id="e3d68-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="e3d68-120">Définissez la propriété de données de pièce jointe approprié :</span><span class="sxs-lookup"><span data-stu-id="e3d68-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="e3d68-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) pour les données binaires et les objets OLE 1.</span><span class="sxs-lookup"><span data-stu-id="e3d68-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="e3d68-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="e3d68-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="e3d68-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) pour les messages et les objets OLE 2.</span><span class="sxs-lookup"><span data-stu-id="e3d68-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="e3d68-124">Définissez **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) pour contenir la représentation graphique de la pièce jointe de fichier ou de pièces jointes binaires.</span><span class="sxs-lookup"><span data-stu-id="e3d68-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="e3d68-125">Ne le définissez pas pour les objets OLE, qui stockent les informations de rendu en interne, ou pour les messages attachés.</span><span class="sxs-lookup"><span data-stu-id="e3d68-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="e3d68-126">Définissez **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pour indiquer où la pièce jointe doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="e3d68-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="e3d68-127">**PR_RENDERING_POSITION** s’applique uniquement aux clients qui définissent la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="e3d68-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="e3d68-128">Si vous ne prennent en charge **PR_RTF_COMPRESSED**, placez les informations d’espace réservé suivantes dans le flux compressé :</span><span class="sxs-lookup"><span data-stu-id="e3d68-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="e3d68-129">Pour définir **PR_RENDERING_POSITION**, attribuer soit un numéro qui représente un décalage ordinal en caractères, avec le premier caractère de **PR_BODY** étant égale à 0, si vous avez besoin de savoir où dans le message de la pièce jointe est restituée ou 0xFFFFFFFF, si vous le faites pas afficher les pièces jointes dans **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="e3d68-130">Définir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) pour indiquer le nom court du fichier d’une pièce jointe et **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) pour indiquer le nom du fichier de prise en charge sur une plateforme qui gère le format de nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="e3d68-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="e3d68-131">Les deux propriétés sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="e3d68-131">Both properties are optional.</span></span> <span data-ttu-id="e3d68-132">Toutefois, si vous définissez **PR_ATTACH_LONG_FILENAME**, définissez également **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="e3d68-133">Définissez **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) pour indiquer le nom de la pièce jointe qui peut apparaître dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e3d68-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="e3d68-134">PR_DISPLAY_NAME est facultative.</span><span class="sxs-lookup"><span data-stu-id="e3d68-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="e3d68-135">Définir PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="e3d68-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="e3d68-136">Appelez [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété avec l’interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="e3d68-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="e3d68-137">Si un fichier contient les données et il est ouvert ou si vous avez besoin de contrôle explicite sur la taille de la mémoire tampon, appelez **IStream::Write** dans une boucle pour placer les données dans le flux.</span><span class="sxs-lookup"><span data-stu-id="e3d68-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="e3d68-138">Une autre option consiste à appeler **OpenStreamOnFile** pour créer un flux de données pour accéder au fichier de données et ensuite appeler la méthode de **IStream::CopyTo** de ce flux pour copier les données dans le flux retourné par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="e3d68-139">Appeler la nouvelle méthode du flux **IStream::Commit** .</span><span class="sxs-lookup"><span data-stu-id="e3d68-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="e3d68-140">Définir PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="e3d68-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="e3d68-141">Appelez **IMAPIProp::OpenProperty** pour ouvrir la propriété avec l’interface **IStreamDocfile** pour créer un flux de données qui fonctionne avec le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="e3d68-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="e3d68-142">**IStreamDocfile** est implémentée par les fournisseurs de banque de messages de donner aux clients un moyen de meilleures performances pour stocker et récupérer du stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="e3d68-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="e3d68-143">L’interface **IStreamDocfile** est la même que **IStream**, mais le contenu de l’objet stream est systématiquement à mettre en forme en tant que stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="e3d68-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="e3d68-144">Si cet appel aboutit, créer le flux de données avec les mêmes étapes décrites pour le paramètre **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="e3d68-145">En cas d’échec de **OpenProperty** :</span><span class="sxs-lookup"><span data-stu-id="e3d68-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="e3d68-146">Appelez **OpenProperty** **IStorage**demandant à nouveau.</span><span class="sxs-lookup"><span data-stu-id="e3d68-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="e3d68-147">Appelez **StgOpenStorage** pour ouvrir l’objet OLE et de renvoyer un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="e3d68-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="e3d68-148">Appelez le stockage renvoyé **IStorage::CopyTo** méthode objet à copier vers l’objet de stockage renvoyé par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="e3d68-149">Appeler la méthode de **IStorage::Commit** du nouvel objet stockage.</span><span class="sxs-lookup"><span data-stu-id="e3d68-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="e3d68-150">Définir PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="e3d68-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="e3d68-151">Allouez une structure [SPropValue](spropvalue.md) , attribuez au membre **ulPropTag** **PR_ATTACH_PATHNAME** et le membre **Value.LPSZ** la chaîne de caractères représentant le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e3d68-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="e3d68-152">Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e3d68-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="e3d68-153">Si votre plate-forme prend en charge les noms de fichiers longs, définissez à la fois **PR_ATTACH_PATHNAME** et **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="e3d68-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="e3d68-154">Il peut être nécessaire appeler un système d’exploitation pour extraire le nom de fichier court.</span><span class="sxs-lookup"><span data-stu-id="e3d68-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3d68-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3d68-155">See also</span></span>

- [<span data-ttu-id="e3d68-156">Pièces jointes MAPI</span><span class="sxs-lookup"><span data-stu-id="e3d68-156">MAPI Attachments</span></span>](mapi-attachments.md)

