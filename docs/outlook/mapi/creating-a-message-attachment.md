---
title: Création d’une pièce jointe de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 711b6765-7763-41ae-9ff8-61ca6ddd459d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2bdba3574c962c825f45cd098efa1cba6e21a4ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332941"
---
# <a name="creating-a-message-attachment"></a><span data-ttu-id="1f412-103">Création d’une pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="1f412-103">Creating a message attachment</span></span>
  
<span data-ttu-id="1f412-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f412-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f412-105">Une pièce jointe est une donnée supplémentaire, telle qu'un fichier, un autre message ou un objet OLE, que vous pouvez envoyer ou enregistrer avec un message.</span><span class="sxs-lookup"><span data-stu-id="1f412-105">A message attachment is some additional data, such as a file, another message, or an OLE object, that you can send or save along with a message.</span></span> <span data-ttu-id="1f412-106">Chaque pièce jointe possède une collection de propriétés qui l'identifient et décrit son type et son mode d'affichage.</span><span class="sxs-lookup"><span data-stu-id="1f412-106">Each attachment has a collection of properties that identifies it and describes its type and how it is rendered.</span></span> <span data-ttu-id="1f412-107">Comme pour les destinataires, les pièces jointes des messages sont accessibles uniquement par le biais du message auquel elles appartiennent.</span><span class="sxs-lookup"><span data-stu-id="1f412-107">Like recipients, message attachments can only be accessed through the message to which they belong.</span></span> <span data-ttu-id="1f412-108">Par conséquent, pour qu'une pièce jointe soit utilisable, son message doit être ouvert.</span><span class="sxs-lookup"><span data-stu-id="1f412-108">Therefore, for an attachment to be usable, its message must be open.</span></span>
  
## <a name="create-a-message-attachment"></a><span data-ttu-id="1f412-109">Créer une pièce jointe de message</span><span class="sxs-lookup"><span data-stu-id="1f412-109">Create a message attachment</span></span>
  
1. <span data-ttu-id="1f412-110">Appelez la méthode [IMessage:: CreateAttach](imessage-createattach.md) du message et transmettez la valeur NULL comme identificateur d'interface.</span><span class="sxs-lookup"><span data-stu-id="1f412-110">Call the message's [IMessage::CreateAttach](imessage-createattach.md) method and pass NULL as the interface identifier.</span></span> <span data-ttu-id="1f412-111">**CreateAttach** renvoie un numéro qui identifie de manière unique la nouvelle pièce jointe dans le message.</span><span class="sxs-lookup"><span data-stu-id="1f412-111">**CreateAttach** returns a number that uniquely identifies the new attachment within the message.</span></span> <span data-ttu-id="1f412-112">Le numéro de pièce jointe est stocké dans la propriété **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) et est valide uniquement tant que le message contenant la pièce jointe est ouvert.</span><span class="sxs-lookup"><span data-stu-id="1f412-112">The attachment number is stored in the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property and is valid only as long as the message containing the attachment is open.</span></span>
    
2. <span data-ttu-id="1f412-113">Appelez [IMAPIProp:: SetProps](imapiprop-setprops.md) pour définir **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) afin d'indiquer comment accéder à la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1f412-113">Call [IMAPIProp::SetProps](imapiprop-setprops.md) to set **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) to indicate how to access the attachment.</span></span> <span data-ttu-id="1f412-114">**PR_ATTACH_METHOD** est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="1f412-114">**PR_ATTACH_METHOD** is required.</span></span> <span data-ttu-id="1f412-115">Définissez-la sur:</span><span class="sxs-lookup"><span data-stu-id="1f412-115">Set it to:</span></span> 
    
   - <span data-ttu-id="1f412-116">ATTACH_BY_VALUE si la pièce jointe est une donnée binaire.</span><span class="sxs-lookup"><span data-stu-id="1f412-116">ATTACH_BY_VALUE if the attachment is binary data.</span></span>
    
   - <span data-ttu-id="1f412-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE ou ATTACH_BY_REF_ONLY si la pièce jointe est un fichier.</span><span class="sxs-lookup"><span data-stu-id="1f412-117">ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE, or ATTACH_BY_REF_ONLY if the attachment is a file.</span></span>
    
   - <span data-ttu-id="1f412-118">ATTACH_EMBEDDED_MSG si la pièce jointe est un message.</span><span class="sxs-lookup"><span data-stu-id="1f412-118">ATTACH_EMBEDDED_MSG if the attachment is a message.</span></span>
    
   - <span data-ttu-id="1f412-119">ATTACH_OLE si la pièce jointe est un objet OLE.</span><span class="sxs-lookup"><span data-stu-id="1f412-119">ATTACH_OLE if the attachment is an OLE object.</span></span>
    
3. <span data-ttu-id="1f412-120">Définissez la propriété de données de pièce jointe appropriée:</span><span class="sxs-lookup"><span data-stu-id="1f412-120">Set the appropriate attachment data property:</span></span>
    
   - <span data-ttu-id="1f412-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) pour les données binaires et les objets OLE 1.</span><span class="sxs-lookup"><span data-stu-id="1f412-121">**PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) for binary data and OLE 1 objects.</span></span>
    
   - <span data-ttu-id="1f412-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) pour les fichiers.</span><span class="sxs-lookup"><span data-stu-id="1f412-122">**PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) for files.</span></span>
    
   - <span data-ttu-id="1f412-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) pour les messages et les objets OLE 2.</span><span class="sxs-lookup"><span data-stu-id="1f412-123">**PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) for messages and OLE 2 objects.</span></span>
    
4. <span data-ttu-id="1f412-124">Définissez **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) pour qu'il contienne la représentation graphique de la pièce jointe de fichier ou de pièces jointes binaires.</span><span class="sxs-lookup"><span data-stu-id="1f412-124">Set **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) to hold the graphic representation of the attachment for file or binary attachments.</span></span> <span data-ttu-id="1f412-125">Ne la définissez pas pour les objets OLE, qui stockent les informations de rendu en interne ou pour les messages attachés.</span><span class="sxs-lookup"><span data-stu-id="1f412-125">Do not set it for OLE objects, which store the rendering information internally, or for attached messages.</span></span> 
    
5. <span data-ttu-id="1f412-126">Définissez **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) pour indiquer où la pièce jointe doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="1f412-126">Set **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) to indicate where the attachment should be displayed.</span></span> <span data-ttu-id="1f412-127">**PR_RENDERING_POSITION** s'applique uniquement aux clients qui définissent la propriété **PR_BODY** .</span><span class="sxs-lookup"><span data-stu-id="1f412-127">**PR_RENDERING_POSITION** applies only to clients that set the **PR_BODY** property.</span></span> <span data-ttu-id="1f412-128">Si vous prenez en charge uniquement **PR_RTF_COMPRESSED**, placez les informations d'espace réservé suivantes dans le flux compressé:</span><span class="sxs-lookup"><span data-stu-id="1f412-128">If you only support **PR_RTF_COMPRESSED**, place the following placeholder information in the compressed stream:</span></span>
    
   `\objattph`

   <span data-ttu-id="1f412-129">Pour définir **PR_RENDERING_POSITION**, affectez un nombre qui représente un décalage ordinal en caractères, le premier caractère de **PR_BODY** étant 0, si vous devez savoir où dans le message la pièce jointe est affichée, ou 0xFFFFFFFF, si vous ne le faites pas afficher les pièces jointes dans **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="1f412-129">To set **PR_RENDERING_POSITION**, assign either a number that represents an ordinal offset in characters, with the first character of **PR_BODY** being 0, if you need to know where in the message the attachment is rendered, or 0xFFFFFFFF, if you do not render attachments within **PR_BODY**.</span></span>
    
6. <span data-ttu-id="1f412-130">Définir **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) pour indiquer le nom abrégé du fichier pour un fichier joint et **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) pour indiquer le nom du fichier comme étant pris en charge sur une plateforme qui gère le format de nom de fichier long.</span><span class="sxs-lookup"><span data-stu-id="1f412-130">Set **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) to indicate the short name of the file for a file attachment and **PR\_ATTACH_LONG_FILENAME** ([PidTagAttachLongFilename](pidtagattachlongfilename-canonical-property.md)) to indicate the name of the file as supported on a platform that handles the long filename format.</span></span> <span data-ttu-id="1f412-131">Les deux propriétés sont facultatives.</span><span class="sxs-lookup"><span data-stu-id="1f412-131">Both properties are optional.</span></span> <span data-ttu-id="1f412-132">Toutefois, si vous définissez **PR_ATTACH_LONG_FILENAME**, définissez également **PR_ATTACH_FILENAME**.</span><span class="sxs-lookup"><span data-stu-id="1f412-132">However, if you set **PR_ATTACH_LONG_FILENAME**, also set **PR_ATTACH_FILENAME**.</span></span> 
    
7. <span data-ttu-id="1f412-133">Définissez **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) pour indiquer le nom de la pièce jointe qui peut s'afficher dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="1f412-133">Set **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to indicate the name for the attachment that can appear in a dialog box.</span></span> <span data-ttu-id="1f412-134">PR_DISPLAY_NAME est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1f412-134">PR_DISPLAY_NAME is optional.</span></span> 
    
## <a name="set-prattachdatabin"></a><span data-ttu-id="1f412-135">Définir PR_ATTACH_DATA_BIN</span><span class="sxs-lookup"><span data-stu-id="1f412-135">Set PR_ATTACH_DATA_BIN</span></span>
  
1. <span data-ttu-id="1f412-136">Appelez [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) pour ouvrir la propriété avec l'interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="1f412-136">Call [IMAPIProp::OpenProperty](imapiprop-openproperty.md) to open the property with the **IStream** interface.</span></span> 
    
2. <span data-ttu-id="1f412-137">Si un fichier contient les données et qu'il est ouvert ou si vous avez besoin d'un contrôle explicite sur la taille de la mémoire tampon, appelez **IStream:: Write** in a Loop to place the Data in the Stream.</span><span class="sxs-lookup"><span data-stu-id="1f412-137">If a file contains the data and it is open or if you need explicit control over buffer size, call **IStream::Write** in a loop to place the data in the stream.</span></span> 
    
3. <span data-ttu-id="1f412-138">Une autre option consiste à appeler **OpenStreamOnFile** pour créer un flux pour accéder au fichier de données, puis appeler la méthode **IStream:: CopyTo** de ce flux pour copier les données dans le flux renvoyé par **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="1f412-138">Another option is to call **OpenStreamOnFile** to create a stream to access the data file and then call this stream's **IStream::CopyTo** method to copy the data to the stream returned by **OpenProperty**.</span></span>
    
4. <span data-ttu-id="1f412-139">Appelez la méthode **IStream:: Commit** du nouveau flux.</span><span class="sxs-lookup"><span data-stu-id="1f412-139">Call the new stream's **IStream::Commit** method.</span></span> 
    
## <a name="set-prattachdataobj"></a><span data-ttu-id="1f412-140">Définir PR_ATTACH_DATA_OBJ</span><span class="sxs-lookup"><span data-stu-id="1f412-140">Set PR_ATTACH_DATA_OBJ</span></span>
  
1. <span data-ttu-id="1f412-141">Appelez **IMAPIProp:: OpenProperty** pour ouvrir la propriété avec l'interface **IStreamDocfile** afin de créer un flux qui fonctionne avec le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="1f412-141">Call **IMAPIProp::OpenProperty** to open the property with the **IStreamDocfile** interface to create a stream that works with structured storage.</span></span> <span data-ttu-id="1f412-142">**IStreamDocfile** est implémenté par les fournisseurs de banques de messages pour permettre aux clients de stocker et de récupérer de manière plus efficace le stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="1f412-142">**IStreamDocfile** is implemented by message store providers to give clients a higher-performance way to store and retrieve structured storage.</span></span> <span data-ttu-id="1f412-143">L'interface **IStreamDocfile** est identique à **IStream**, mais le contenu du flux est garanti être formaté en tant que stockage structuré.</span><span class="sxs-lookup"><span data-stu-id="1f412-143">The **IStreamDocfile** interface is the same as **IStream**, but the content of the stream is guaranteed to be formatted as structured storage.</span></span> <span data-ttu-id="1f412-144">Si cet appel réussit, créez le flux en suivant les mêmes étapes que celles décrites pour le paramétrage de **PR_ATTACH_DATA_BIN**.</span><span class="sxs-lookup"><span data-stu-id="1f412-144">If this call succeeds, create the stream with the same steps outlined for setting **PR_ATTACH_DATA_BIN**.</span></span>
    
2. <span data-ttu-id="1f412-145">Si **OpenProperty** échoue:</span><span class="sxs-lookup"><span data-stu-id="1f412-145">If **OpenProperty** fails:</span></span> 
    
   1. <span data-ttu-id="1f412-146">Appelez à nouveau **OpenProperty** en demandant **IStorage**.</span><span class="sxs-lookup"><span data-stu-id="1f412-146">Call **OpenProperty** again asking for **IStorage**.</span></span> 
      
   2. <span data-ttu-id="1f412-147">Appelez **StgOpenStorage** pour ouvrir l'objet OLE et renvoyer un objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="1f412-147">Call **StgOpenStorage** to open the OLE object and return a storage object.</span></span> 
      
   3. <span data-ttu-id="1f412-148">Appelez la méthode **IStorage:: CopyTo** de l'objet de stockage renvoyé vers l'objet de stockage renvoyé à partir de **OpenProperty**.</span><span class="sxs-lookup"><span data-stu-id="1f412-148">Call the returned storage object's **IStorage::CopyTo** method to copy to the storage object returned from **OpenProperty**.</span></span>
      
   4. <span data-ttu-id="1f412-149">Appelez la méthode **IStorage:: Commit** de l'objet de stockage.</span><span class="sxs-lookup"><span data-stu-id="1f412-149">Call the new storage object's **IStorage::Commit** method.</span></span> 
    
## <a name="set-prattachpathname"></a><span data-ttu-id="1f412-150">Définir PR_ATTACH_PATHNAME</span><span class="sxs-lookup"><span data-stu-id="1f412-150">Set PR_ATTACH_PATHNAME</span></span>
  
1. <span data-ttu-id="1f412-151">AlLouez une structure [SPropValue](spropvalue.md) , en définissant le membre **ulPropTag** sur **PR_ATTACH_PATHNAME** et le membre **value. LPSZ** sur la chaîne de caractères qui représente le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1f412-151">Allocate an [SPropValue](spropvalue.md) structure, setting the **ulPropTag** member to **PR_ATTACH_PATHNAME** and the **Value.LPSZ** member to the character string that represents the filename.</span></span> 
    
2. <span data-ttu-id="1f412-152">Appelez la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="1f412-152">Call the attachment's [IMAPIProp::SetProps](imapiprop-setprops.md) method.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1f412-153">Si votre plateforme prend en charge les noms de fichier longs, définissez à la fois **PR_ATTACH_PATHNAME** et **PR_ATTACH_LONG_PATHNAME**.</span><span class="sxs-lookup"><span data-stu-id="1f412-153">If your platform supports long filenames, set both **PR_ATTACH_PATHNAME** and **PR_ATTACH_LONG_PATHNAME**.</span></span> <span data-ttu-id="1f412-154">Il peut s'avérer nécessaire d'effectuer un appel de système d'exploitation pour récupérer le nom de fichier court.</span><span class="sxs-lookup"><span data-stu-id="1f412-154">It might be necessary to make an operating system call to retrieve the short filename.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f412-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1f412-155">See also</span></span>

- [<span data-ttu-id="1f412-156">Pièces jointes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f412-156">MAPI Attachments</span></span>](mapi-attachments.md)

