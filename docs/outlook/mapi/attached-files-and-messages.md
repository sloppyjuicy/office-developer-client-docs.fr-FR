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
# <a name="attached-files-and-messages"></a><span data-ttu-id="e8f7d-103">Fichiers et messages joints</span><span class="sxs-lookup"><span data-stu-id="e8f7d-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="e8f7d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f7d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f7d-105">Si MIME avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes sont dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="e8f7d-106">Le format TNEF lui-même est un fichier binaire joint unique nommé Winmail.dat, codé comme décrit pour MIME sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="e8f7d-107">Si MIME est utilisé sans TNEF, les fichiers joints sont envoyés en tant que composants de contenu de message MIME.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="e8f7d-108">Le nom de fichier est placé dans le paramètre  *name*  de  *l’en-tête Content-type*  de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="e8f7d-109">Le jeu de caractères de la pièce jointe est placé dans le  *paramètre charset*  au  *type de contenu*  ; Il et le contenu-transfer-encoding sont déterminés par l’analyse de l’intégralité du contenu de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="e8f7d-110">Les pièces jointes d’URL sont traitées de manière spéciale :</span><span class="sxs-lookup"><span data-stu-id="e8f7d-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="e8f7d-111">Si la pièce jointe est une URL (un fichier joint avec une extension . URL) et le mode d’accès défini dans ce fichier est FTP anonyme, il est codé en tant que message externe et le contenu du fichier (l’URL) est copié dans l’en-tête du message externe.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="e8f7d-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span><span class="sxs-lookup"><span data-stu-id="e8f7d-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="e8f7d-113">Si seuls des caractères 7 bits sont trouvés et qu’aucune ligne ne dépasse 140 caractères, la pièce jointe est du texte ASCII.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="e8f7d-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span><span class="sxs-lookup"><span data-stu-id="e8f7d-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="e8f7d-115">Si des lignes longues ou jusqu’à 25 % de caractères 8 bits sont trouvés, le contenu de la pièce jointe est du texte et le jeu de caractères est déterminé par les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="e8f7d-116">Il doit être choisi parmi les jeux de caractères définis par la norme ISO 8859.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="e8f7d-117">*Content-type: text/plain; charset=ISO-8859-1*  (par exemple)</span><span class="sxs-lookup"><span data-stu-id="e8f7d-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="e8f7d-118">*Content-Transfer-Encoding: quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="e8f7d-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="e8f7d-119">Si 25 % ou plus des caractères ont le jeu de bits élevé, la pièce jointe est binaire.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="e8f7d-120">Il est codé à l’aide de l’algorithme Base64.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="e8f7d-121">*Content-type: application/octet-stream*  (par défaut ; en fonction de l’extension de fichier)</span><span class="sxs-lookup"><span data-stu-id="e8f7d-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="e8f7d-122">Content-Transfer-Encoding: base64 \*</span><span class="sxs-lookup"><span data-stu-id="e8f7d-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="e8f7d-123">Sur les messages sortants, le type de contenu doit être dérivé de l’extension à trois lettres du nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="e8f7d-124">Ce mappage existe dans le Registre système ; sous se trouve une valeur de chaîne nommée « Content Type » qui donne au type de contenu MIME s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="e8f7d-125">Cet exemple est pour un fichier image TIFF :</span><span class="sxs-lookup"><span data-stu-id="e8f7d-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="e8f7d-126">HKEY_LOCAL_MACHINE</span><span class="sxs-lookup"><span data-stu-id="e8f7d-126">HKEY_LOCAL_MACHINE</span></span>\
  
<span data-ttu-id="e8f7d-127">Software</span><span class="sxs-lookup"><span data-stu-id="e8f7d-127">Software</span></span>\
  
<span data-ttu-id="e8f7d-128">Microsoft</span><span class="sxs-lookup"><span data-stu-id="e8f7d-128">Microsoft</span></span>\
  
<span data-ttu-id="e8f7d-129">Classes</span><span class="sxs-lookup"><span data-stu-id="e8f7d-129">Classes</span></span>\
  
<span data-ttu-id="e8f7d-130">.tif</span><span class="sxs-lookup"><span data-stu-id="e8f7d-130">.tif</span></span>
  
<span data-ttu-id="e8f7d-131">Type de contenu = « image/tiff »</span><span class="sxs-lookup"><span data-stu-id="e8f7d-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="e8f7d-132">S’il n’existe aucun mappage pour l’extension de fichier, le flux  *d’application/d’octet*  par défaut doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="e8f7d-133">Sur les messages entrants, le type de contenu d’une pièce jointe doit toujours être copié dans la propriété MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8f7d-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="e8f7d-134">Même si un nom de fichier est défini pour un fichier joint, l’extension mappée par le type de contenu doit être utilisée dans les propriétés **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) et **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e8f7d-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="e8f7d-135">Le  *paramètre*  name est officiellement supprimé par la RFC 821.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="e8f7d-136">Au fil de l’évolution des normes, Microsoft envisagera de spécifier un mappage de remplacement pour les noms de fichiers joints.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="e8f7d-137">Les messages joints sortants sont envoyés sous la forme \* Type de contenu : message/rfc822 \* Les messages joints sont codés de manière récursive, à leur place.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-137">Outbound attached messages are sent as \* Content-type: message/rfc822 \*  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="e8f7d-138">Les composants de contenu de message entrant avec  *Content-Type: multipart/digest*  sont également mappés sur des messages incorporés.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="e8f7d-139">Si uuencode avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes se trouve dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="e8f7d-140">Le format TNEF lui-même est un fichier binaire joint unique nommé Winmail.dat, codé comme décrit pour Uuencode sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="e8f7d-141">Si uuencode est utilisé sans TNEF, tous les fichiers joints sont traités comme binaires et uuencoded, à la suite du texte du message.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="e8f7d-142">Le nom de fichier est présent dans l’en-tête uuencode :</span><span class="sxs-lookup"><span data-stu-id="e8f7d-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="e8f7d-143">begin 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="e8f7d-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="e8f7d-144">... données ...</span><span class="sxs-lookup"><span data-stu-id="e8f7d-144">... data ...</span></span> 
  
 <span data-ttu-id="e8f7d-145">end</span><span class="sxs-lookup"><span data-stu-id="e8f7d-145">end</span></span> 
  
<span data-ttu-id="e8f7d-146">Les messages joints sont textuels dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="e8f7d-147">La hiérarchie des messages joints est toujours aplatie ; autrement dit, les messages au sein des messages joints sont retirés au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="e8f7d-148">Les objets OLE incorporés sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="e8f7d-149">Les positions de rendu des pièces jointes sont transmises littéralement, à l’aide de la **propriété PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) dans le TNEF.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="e8f7d-150">Si le TNEF n’est pas utilisé, ils sont perdus.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="e8f7d-151">Les pièces jointes entrantes sans position de rendu (y compris en l’absence de TNEF) ont leur position de rendu définie sur 0xFFFFFFFF, c’est-à-dire, sans position dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="e8f7d-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e8f7d-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8f7d-152">See also</span></span>



[<span data-ttu-id="e8f7d-153">Mappage des attributs de messagerie Internet aux propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f7d-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

