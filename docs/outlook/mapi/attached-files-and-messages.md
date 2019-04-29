---
title: Fichiers et messages joints
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436838"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="ae986-103">Fichiers et messages joints</span><span class="sxs-lookup"><span data-stu-id="ae986-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="ae986-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae986-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae986-105">Si MIME avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes se trouvent dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="ae986-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="ae986-106">Le format TNEF lui-même est un fichier binaire unique nommé Winmail. dat, encodé comme indiqué pour MIME sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="ae986-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="ae986-107">Si MIME est utilisé sans TNEF, les fichiers joints sont envoyés en tant que parties de contenu de message MIME.</span><span class="sxs-lookup"><span data-stu-id="ae986-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="ae986-108">Le nom de fichier est placé dans le paramètre *Name* vers l'en-tête *Content-type* pour la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ae986-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="ae986-109">Le jeu de caractères de la pièce jointe est placé dans le paramètre *charset* vers le *type Content-type* ; elle et le Content-Transfer-Encoding sont déterminés en analysant l'intégralité du contenu de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="ae986-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="ae986-110">Les pièces jointes d'URL sont traitées de la façon suivante:</span><span class="sxs-lookup"><span data-stu-id="ae986-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="ae986-111">Si la pièce jointe est une URL (fichier joint avec l'extension. URL), et le mode d'accès qui y est défini est le mode FTP anonyme, il est encodé sous la forme d'un message externe et le contenu du fichier (l'URL) est copié dans l'en-tête du message externe.</span><span class="sxs-lookup"><span data-stu-id="ae986-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="ae986-112">*Content-type: message/External-Body; Access-type = Anon-FTP*  (Content-Transfer-Encoding: 7bit est supposé.)</span><span class="sxs-lookup"><span data-stu-id="ae986-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="ae986-113">Si seuls les caractères 7 bits sont trouvés et qu'aucune ligne ne dépasse 140 caractères, la pièce jointe est du texte ASCII.</span><span class="sxs-lookup"><span data-stu-id="ae986-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="ae986-114">*Content-type: text/plain; charset = US-ASCII Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="ae986-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="ae986-115">Si des lignes longues ou jusqu'à 25% de caractères 8 bits sont trouvés, le contenu de la pièce jointe est du texte et le jeu de caractères est déterminé par les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="ae986-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="ae986-116">Il doit être choisi parmi les jeux de caractères définis par la norme ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="ae986-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="ae986-117">*Content-type: text/plain; charset = ISO-8859-1*  (par exemple)</span><span class="sxs-lookup"><span data-stu-id="ae986-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="ae986-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="ae986-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="ae986-119">Si 25% ou plus des caractères ont le bit supérieur défini, la pièce jointe est binaire.</span><span class="sxs-lookup"><span data-stu-id="ae986-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="ae986-120">Elle est codée à l'aide de l'algorithme base64.</span><span class="sxs-lookup"><span data-stu-id="ae986-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="ae986-121">*Content-type: application/octet-stream*  (par défaut, en fonction de l'extension de fichier)</span><span class="sxs-lookup"><span data-stu-id="ae986-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="ae986-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="ae986-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="ae986-123">Sur les messages sortants, le type de contenu doit être dérivé de l'extension de nom de fichier de trois lettres.</span><span class="sxs-lookup"><span data-stu-id="ae986-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="ae986-124">Ce mappage existe dans le registre système; sous il existe une valeur de chaîne nommée «Content type» qui indique le type de contenu MIME s'il est défini.</span><span class="sxs-lookup"><span data-stu-id="ae986-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="ae986-125">Cet exemple est destiné à un fichier image TIFF:</span><span class="sxs-lookup"><span data-stu-id="ae986-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="ae986-126">HKEY_LOCAL_MACHINE \\</span><span class="sxs-lookup"><span data-stu-id="ae986-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="ae986-127">Application</span><span class="sxs-lookup"><span data-stu-id="ae986-127">Software\\</span></span>
  
<span data-ttu-id="ae986-128">Librairie</span><span class="sxs-lookup"><span data-stu-id="ae986-128">Microsoft\\</span></span>
  
<span data-ttu-id="ae986-129">Classes</span><span class="sxs-lookup"><span data-stu-id="ae986-129">Classes\\</span></span>
  
<span data-ttu-id="ae986-130">. TIF</span><span class="sxs-lookup"><span data-stu-id="ae986-130">.tif</span></span>
  
<span data-ttu-id="ae986-131">Type de contenu = «image/TIFF»</span><span class="sxs-lookup"><span data-stu-id="ae986-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="ae986-132">S'il n'existe aucun mappage pour l'extension de fichier, le flux d' *application/octet* par défaut doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="ae986-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="ae986-133">Sur les messages entrants, le type de contenu d'une pièce jointe doit toujours être copié dans la propriété MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="ae986-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="ae986-134">Même si un nom de fichier est défini pour un fichier joint, l'extension mappée par le type de contenu doit être utilisée dans les propriétés **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) et **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). .</span><span class="sxs-lookup"><span data-stu-id="ae986-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="ae986-135">Le paramètre *Name* est officiellement déconseillé par la norme RFC 821.</span><span class="sxs-lookup"><span data-stu-id="ae986-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="ae986-136">À mesure que les standards évoluent, Microsoft envisagera de spécifier un autre mappage pour les noms de fichier attachés.</span><span class="sxs-lookup"><span data-stu-id="ae986-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="ae986-137">Les messages joints sortants sont envoyés en tant que \* content-type: message/rfc822 \* les messages joints sont codés de manière récursive, à leur emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="ae986-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="ae986-138">Les parties de contenu de messages entrants avec *Content-type: multipart/Digest* sont également mappées aux messages incorporés.</span><span class="sxs-lookup"><span data-stu-id="ae986-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="ae986-139">Si uuencode avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes se trouvent dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="ae986-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="ae986-140">Le format TNEF lui-même est un fichier binaire unique nommé Winmail. dat, encodé comme décrit pour uuencode sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="ae986-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="ae986-141">Si uuencode est utilisé sans TNEF, tous les fichiers joints sont traités comme binaires et UUEncoded, à la suite du texte du message.</span><span class="sxs-lookup"><span data-stu-id="ae986-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="ae986-142">Le nom de fichier est présent dans l'en-tête uuencode:</span><span class="sxs-lookup"><span data-stu-id="ae986-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="ae986-143">début 0755 Winmail. dat</span><span class="sxs-lookup"><span data-stu-id="ae986-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="ae986-144">... données...</span><span class="sxs-lookup"><span data-stu-id="ae986-144">... data ...</span></span> 
  
 <span data-ttu-id="ae986-145">end</span><span class="sxs-lookup"><span data-stu-id="ae986-145">end</span></span> 
  
<span data-ttu-id="ae986-146">Les messages joints sont détextuels dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ae986-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="ae986-147">La hiérarchie des messages attachés est toujours aplatie; autrement dit, les messages dans les messages joints sont extraits vers le niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="ae986-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="ae986-148">Les objets OLE incorporés sont rejetés.</span><span class="sxs-lookup"><span data-stu-id="ae986-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="ae986-149">Les positions de rendu des pièces jointes sont transmises littéralement, à l'aide de la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) dans le format TNEF.</span><span class="sxs-lookup"><span data-stu-id="ae986-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="ae986-150">Si TNEF n'est pas utilisé, ils sont perdus.</span><span class="sxs-lookup"><span data-stu-id="ae986-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="ae986-151">Les pièces jointes entrantes sans position de rendu (y compris lorsqu'il n'y a pas de TNEF) ont leur position de rendu définie sur 0xFFFFFFFF, autrement dit, pas de position dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="ae986-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae986-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae986-152">See also</span></span>



[<span data-ttu-id="ae986-153">Mappage des attributs de messagerie Internet aux propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ae986-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

