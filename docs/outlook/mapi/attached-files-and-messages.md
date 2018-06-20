---
title: Les Messages et les fichiers joints
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 489930b35d24d2691c9b9fbb59b0fa95707a0618
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782921"
---
# <a name="attached-files-and-messages"></a><span data-ttu-id="0fda5-103">Les Messages et les fichiers joints</span><span class="sxs-lookup"><span data-stu-id="0fda5-103">Attached Files and Messages</span></span>

  
  
<span data-ttu-id="0fda5-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0fda5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0fda5-105">Si MIME avec TNEF est utilisé lors de l’encodage du contenu des messages, toutes les propriétés des pièces jointes et le contenu se trouvent dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="0fda5-105">If MIME with TNEF is used while encoding message content,all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="0fda5-106">Le format TNEF elle-même est un seul fichier joint binaire nommé Winmail.dat, codés comme décrit MIME sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="0fda5-106">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for MIME without TNEF.</span></span> 
  
<span data-ttu-id="0fda5-107">Si MIME est utilisée sans TNEF, les fichiers joints sont envoyés en tant que parties de contenu de message MIME.</span><span class="sxs-lookup"><span data-stu-id="0fda5-107">If MIME is used without TNEF, attached files are sent as MIME message content parts.</span></span> <span data-ttu-id="0fda5-108">Le nom de fichier est placé dans le paramètre *name* à l’en-tête *Content-type* de la pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0fda5-108">The filename is placed in the  *name*  parameter to the  *Content-type*  header for the attachment.</span></span> <span data-ttu-id="0fda5-109">Le jeu de caractères de la pièce jointe est placé dans le paramètre de *jeu de caractères* pour le *type de contenu* ; Il et le contenu-transfert-codage sont déterminés par analyse du contenu de pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="0fda5-109">The character set for the attachment is placed in the  *charset*  parameter to the  *Content-type*  ; it and the content-transfer-encoding are determined by scanning the entire attachment content.</span></span> <span data-ttu-id="0fda5-110">Pièces jointes URL sont traités spécialement :</span><span class="sxs-lookup"><span data-stu-id="0fda5-110">URL attachments are treated specially:</span></span> 
  
- <span data-ttu-id="0fda5-111">Si la pièce jointe est une URL (un fichier joint avec l’extension. URL), le mode d’accès défini est anonyme FTP, il est codé en tant qu’un message externe et le contenu du fichier (l’URL) est copié dans l’en-tête du message externe.</span><span class="sxs-lookup"><span data-stu-id="0fda5-111">If the attachment is a URL (an attached file with extension .URL), and the access mode defined in it is anonymous FTP, it is encoded as an external message, and the content of the file (the URL) is copied into the header of the external message.</span></span> <span data-ttu-id="0fda5-112">*Content-type : message/externe-corps ; type d’accès = l’authentification anonyme ftp*  (Codage de transfert de contenu : 7 bits est supposé.)</span><span class="sxs-lookup"><span data-stu-id="0fda5-112">*Content-type: message/external-body; access-type=anon-ftp*  (Content-Transfer-Encoding: 7bit is assumed.)</span></span> 
    
- <span data-ttu-id="0fda5-113">Si seuls les caractères 7 bits sont détectés et aucune ligne ne dépasse 140 caractères, la pièce jointe est texte ASCII.</span><span class="sxs-lookup"><span data-stu-id="0fda5-113">If only 7-bit characters are found and no line exceeds 140 characters in length, the attachment is ASCII text.</span></span> <span data-ttu-id="0fda5-114">*Type de contenu : texte brut ; CharSet = us-ascii Content-Transfer-Encoding : 7 bits*</span><span class="sxs-lookup"><span data-stu-id="0fda5-114">*Content-type: text/plain; charset=us-ascii Content-Transfer-Encoding: 7bit*</span></span> 
    
- <span data-ttu-id="0fda5-115">Si long des lignes ou à 25 % de caractères 8 bits sont détectés, le contenu de pièce jointe est un texte et le jeu de caractères est déterminé par les paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="0fda5-115">If long lines or up to 25% 8-bit characters are found, the attachment content is text and the character set is determined by the locale.</span></span> <span data-ttu-id="0fda5-116">Il doit être choisie dans les jeux de caractères définis par la norme ISO 8859 standard.</span><span class="sxs-lookup"><span data-stu-id="0fda5-116">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="0fda5-117">*Type de contenu : texte/ordinaire ; charset = ISO-8859-1*  (par exemple)</span><span class="sxs-lookup"><span data-stu-id="0fda5-117">*Content-type: text/plain; charset=ISO-8859-1*  (for example)</span></span> 
    
     <span data-ttu-id="0fda5-118">*Content-Transfer-Encoding : quoted-printable*</span><span class="sxs-lookup"><span data-stu-id="0fda5-118">*Content-Transfer-Encoding: quoted-printable*</span></span> 
    
- <span data-ttu-id="0fda5-119">Si au moins 25 % des caractères possède le bit élevé, la pièce jointe est binaire.</span><span class="sxs-lookup"><span data-stu-id="0fda5-119">If 25% or more of the characters have the high bit set, the attachment is binary.</span></span> <span data-ttu-id="0fda5-120">Il est codé à l’aide de l’algorithme en Base64.</span><span class="sxs-lookup"><span data-stu-id="0fda5-120">It is encoded using the Base64 algorithm.</span></span> <span data-ttu-id="0fda5-121">*Content-type : application/octet-flux*  (par défaut, basé sur l’extension de fichier)</span><span class="sxs-lookup"><span data-stu-id="0fda5-121">*Content-type: application/octet-stream*  (by default; based on file extension)</span></span> 
    
     * <span data-ttu-id="0fda5-122">Content-Transfer-Encoding : base64 \*</span><span class="sxs-lookup"><span data-stu-id="0fda5-122">Content-Transfer-Encoding: base64 \*</span></span> 
    
<span data-ttu-id="0fda5-123">Sur les messages sortants, le type de contenu doit être dérivé à partir de l’extension de nom de fichier à trois lettres.</span><span class="sxs-lookup"><span data-stu-id="0fda5-123">On outbound messages, the content-type should be derived from the filename's three-letter extension.</span></span> <span data-ttu-id="0fda5-124">Ce mappage existe dans le Registre système. sous là est une valeur de chaîne nommée « Type de contenu » qui fournit le type de contenu MIME s’il est défini.</span><span class="sxs-lookup"><span data-stu-id="0fda5-124">This mapping exists in the system registry; under there is a string value named "Content Type" that gives the MIME content type if one is defined.</span></span> <span data-ttu-id="0fda5-125">Cet exemple est un fichier image TIFF :</span><span class="sxs-lookup"><span data-stu-id="0fda5-125">This example is for a TIFF image file:</span></span>
  
<span data-ttu-id="0fda5-126">HKEY_LOCAL_MACHINE\\</span><span class="sxs-lookup"><span data-stu-id="0fda5-126">HKEY_LOCAL_MACHINE\\</span></span>
  
<span data-ttu-id="0fda5-127">Logiciels\\</span><span class="sxs-lookup"><span data-stu-id="0fda5-127">Software\\</span></span>
  
<span data-ttu-id="0fda5-128">Microsoft\\</span><span class="sxs-lookup"><span data-stu-id="0fda5-128">Microsoft\\</span></span>
  
<span data-ttu-id="0fda5-129">Classes\\</span><span class="sxs-lookup"><span data-stu-id="0fda5-129">Classes\\</span></span>
  
<span data-ttu-id="0fda5-130">.tif</span><span class="sxs-lookup"><span data-stu-id="0fda5-130">.tif</span></span>
  
<span data-ttu-id="0fda5-131">Type de contenu = « image/tiff »</span><span class="sxs-lookup"><span data-stu-id="0fda5-131">Content Type = "image/tiff"</span></span>
  
<span data-ttu-id="0fda5-132">S’il n’existe aucun mappage pour l’extension de fichier, le flux *d’application/octet* par défaut doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0fda5-132">If there is no mapping for the file extension, the default  *application/octet*  stream should be used.</span></span> 
  
<span data-ttu-id="0fda5-133">Sur les messages entrants, le type de contenu d’une pièce jointe doit toujours être copié à la propriété MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0fda5-133">On inbound messages, the content-type for an attachment should always be copied to the MAPI property **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)).</span></span> <span data-ttu-id="0fda5-134">Même si un nom de fichier est défini pour une pièce jointe, l’extension est mappée par le type de contenu doit être utilisée dans les **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) et les propriétés de **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .</span><span class="sxs-lookup"><span data-stu-id="0fda5-134">Even if a filename is defined for an attached file, the extension mapped by the content-type should be used in the **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) and **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="0fda5-135">Le paramètre *name* est officiellement déconseillé par la spécification RFC 821.</span><span class="sxs-lookup"><span data-stu-id="0fda5-135">The  *name*  parameter is officially deprecated by RFC 821.</span></span> <span data-ttu-id="0fda5-136">Comme les normes, Microsoft considère spécifiant un mappage de remplacement pour les noms de fichiers joints.</span><span class="sxs-lookup"><span data-stu-id="0fda5-136">As standards evolve, Microsoft will consider specifying an alternate mapping for attached filenames.</span></span> 
  
<span data-ttu-id="0fda5-137">Joint les messages sortants sont envoyés en tant que *-type de contenu : message/rfc822 * Messages dans les messages transférés sont codées de manière récursive, à l’emplacement adéquat.</span><span class="sxs-lookup"><span data-stu-id="0fda5-137">Outbound attached messages are sent as * Content-type: message/rfc822 *  Messages within attached messages are encoded recursively, in their proper place.</span></span> <span data-ttu-id="0fda5-138">Entrant des composants de contenu de message avec *Content-Type : / multipartie* sont également mappés à des messages incorporés.</span><span class="sxs-lookup"><span data-stu-id="0fda5-138">Inbound message content parts with  *Content-Type: multipart/digest*  are also mapped to embedded messages.</span></span> 
  
<span data-ttu-id="0fda5-139">Si uuencode avec TNEF est utilisé lors de l’encodage du contenu des messages, toutes les propriétés des pièces jointes et le contenu se trouvent dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="0fda5-139">If uuencode with TNEF is used while encoding message content, all attachment properties and content are in the TNEF stream.</span></span> <span data-ttu-id="0fda5-140">Le format TNEF elle-même est un seul fichier joint binaire nommé Winmail.dat, codés comme décrit pour Uuencode sans TNEF.</span><span class="sxs-lookup"><span data-stu-id="0fda5-140">The TNEF itself is a single, binary attached file named Winmail.dat, encoded as described for Uuencode without TNEF.</span></span>
  
<span data-ttu-id="0fda5-141">Si uuencode est utilisée sans TNEF, tous les fichiers joints sont considérés comme des fichiers binaires et UUENCODE, suivant le texte du message.</span><span class="sxs-lookup"><span data-stu-id="0fda5-141">If uuencode is used without TNEF, all attached files are treated as binary and uuencoded, following the message text.</span></span> <span data-ttu-id="0fda5-142">Le nom de fichier est présent dans l’en-tête uuencode :</span><span class="sxs-lookup"><span data-stu-id="0fda5-142">The file name is present in the uuencode header:</span></span>
  
 <span data-ttu-id="0fda5-143">commencer 0755 Winmail.dat</span><span class="sxs-lookup"><span data-stu-id="0fda5-143">begin 0755 Winmail.dat</span></span> 
  
 <span data-ttu-id="0fda5-144">... données...</span><span class="sxs-lookup"><span data-stu-id="0fda5-144">... data ...</span></span> 
  
 <span data-ttu-id="0fda5-145">end</span><span class="sxs-lookup"><span data-stu-id="0fda5-145">end</span></span> 
  
<span data-ttu-id="0fda5-146">Messages joints sont textized dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="0fda5-146">Attached messages are textized into the message text.</span></span> <span data-ttu-id="0fda5-147">La hiérarchie de messages associées est toujours aplatie ; Autrement dit, les messages dans les messages transférés sont extraits au niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="0fda5-147">The hierarchy of attached messages is always flattened; that is, messages within attached messages are pulled out to the top level.</span></span>
  
<span data-ttu-id="0fda5-148">Objets OLE incorporés sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="0fda5-148">Embedded OLE objects are discarded.</span></span>
  
<span data-ttu-id="0fda5-149">Positions de rendu des pièces jointes sont transmises en réalité, à l’aide de la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) dans le format TNEF.</span><span class="sxs-lookup"><span data-stu-id="0fda5-149">Attachment rendering positions are transmitted literally, using the property **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) in the TNEF.</span></span> <span data-ttu-id="0fda5-150">Si le format TNEF n’est pas utilisée, ils sont perdus.</span><span class="sxs-lookup"><span data-stu-id="0fda5-150">If TNEF is not used, they are lost.</span></span> <span data-ttu-id="0fda5-151">Pièces jointes entrants avec aucune position de rendu (y compris lorsqu’il n’existe aucune TNEF) n’ont leur position rendu 0xFFFFFFFF, autrement dit, aucune position dans le texte du message.</span><span class="sxs-lookup"><span data-stu-id="0fda5-151">Incoming attachments with no rendering position (including when there is no TNEF) have their rendering position set to 0xFFFFFFFF, that is, no position in the message text.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fda5-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0fda5-152">See also</span></span>



[<span data-ttu-id="0fda5-153">Mappage d’attributs de messagerie Internet sur des propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0fda5-153">Mapping of Internet Mail Attributes to MAPI Properties</span></span>](mapping-of-internet-mail-attributes-to-mapi-properties.md)

