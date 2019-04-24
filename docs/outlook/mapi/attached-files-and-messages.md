---
title: Fichiers et messages joints
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b2f2fb72-23ae-4e0b-a8a1-3b78a1862acb
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c4dbe1a761a753bef77168aec8d2674a1b2b100e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318129"
---
# <a name="attached-files-and-messages"></a>Fichiers et messages joints

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Si MIME avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes se trouvent dans le flux TNEF. Le format TNEF lui-même est un fichier binaire unique nommé Winmail. dat, encodé comme indiqué pour MIME sans TNEF. 
  
Si MIME est utilisé sans TNEF, les fichiers joints sont envoyés en tant que parties de contenu de message MIME. Le nom de fichier est placé dans le paramètre *Name* vers l'en-tête *Content-type* pour la pièce jointe. Le jeu de caractères de la pièce jointe est placé dans le paramètre *charset* vers le *type Content-type* ; elle et le Content-Transfer-Encoding sont déterminés en analysant l'intégralité du contenu de la pièce jointe. Les pièces jointes d'URL sont traitées de la façon suivante: 
  
- Si la pièce jointe est une URL (fichier joint avec l'extension. URL), et le mode d'accès qui y est défini est le mode FTP anonyme, il est encodé sous la forme d'un message externe et le contenu du fichier (l'URL) est copié dans l'en-tête du message externe. *Content-type: message/External-Body; Access-type = Anon-FTP*  (Content-Transfer-Encoding: 7bit est supposé.) 
    
- Si seuls les caractères 7 bits sont trouvés et qu'aucune ligne ne dépasse 140 caractères, la pièce jointe est du texte ASCII. *Content-type: text/plain; charset = US-ASCII Content-Transfer-Encoding: 7bit* 
    
- Si des lignes longues ou jusqu'à 25% de caractères 8 bits sont trouvés, le contenu de la pièce jointe est du texte et le jeu de caractères est déterminé par les paramètres régionaux. Il doit être choisi parmi les jeux de caractères définis par la norme ISO 8859. *Content-type: text/plain; charset = ISO-8859-1*  (par exemple) 
    
     *Content-Transfer-Encoding: quoted-printable* 
    
- Si 25% ou plus des caractères ont le bit supérieur défini, la pièce jointe est binaire. Elle est codée à l'aide de l'algorithme base64. *Content-type: application/octet-stream*  (par défaut, en fonction de l'extension de fichier) 
    
     * Content-Transfer-Encoding: base64 * 
    
Sur les messages sortants, le type de contenu doit être dérivé de l'extension de nom de fichier de trois lettres. Ce mappage existe dans le registre système; sous il existe une valeur de chaîne nommée «Content type» qui indique le type de contenu MIME s'il est défini. Cet exemple est destiné à un fichier image TIFF:
  
HKEY_LOCAL_MACHINE \
  
Application
  
Librairie
  
Classes
  
. TIF
  
Type de contenu = «image/TIFF»
  
S'il n'existe aucun mappage pour l'extension de fichier, le flux d' *application/octet* par défaut doit être utilisé. 
  
Sur les messages entrants, le type de contenu d'une pièce jointe doit toujours être copié dans la propriété MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Même si un nom de fichier est défini pour un fichier joint, l'extension mappée par le type de contenu doit être utilisée dans les propriétés **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) et **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)). .
  
Le paramètre *Name* est officiellement déconseillé par la norme RFC 821. À mesure que les standards évoluent, Microsoft envisagera de spécifier un autre mappage pour les noms de fichier attachés. 
  
Les messages joints sortants sont envoyés en tant que * content-type: message/rfc822 * les messages joints sont codés de manière récursive, à leur emplacement approprié. Les parties de contenu de messages entrants avec *Content-type: multipart/Digest* sont également mappées aux messages incorporés. 
  
Si uuencode avec TNEF est utilisé lors du codage du contenu des messages, toutes les propriétés et le contenu des pièces jointes se trouvent dans le flux TNEF. Le format TNEF lui-même est un fichier binaire unique nommé Winmail. dat, encodé comme décrit pour uuencode sans TNEF.
  
Si uuencode est utilisé sans TNEF, tous les fichiers joints sont traités comme binaires et UUEncoded, à la suite du texte du message. Le nom de fichier est présent dans l'en-tête uuencode:
  
 début 0755 Winmail. dat 
  
 ... données... 
  
 end 
  
Les messages joints sont détextuels dans le texte du message. La hiérarchie des messages attachés est toujours aplatie; autrement dit, les messages dans les messages joints sont extraits vers le niveau supérieur.
  
Les objets OLE incorporés sont rejetés.
  
Les positions de rendu des pièces jointes sont transmises littéralement, à l'aide de la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) dans le format TNEF. Si TNEF n'est pas utilisé, ils sont perdus. Les pièces jointes entrantes sans position de rendu (y compris lorsqu'il n'y a pas de TNEF) ont leur position de rendu définie sur 0xFFFFFFFF, autrement dit, pas de position dans le texte du message.
  
## <a name="see-also"></a>Voir aussi



[Mappage des attributs de messagerie Internet aux propriétés MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

