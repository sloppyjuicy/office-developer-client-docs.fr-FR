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
# <a name="attached-files-and-messages"></a>Les Messages et les fichiers joints

  
  
**S’applique à**: Outlook 
  
Si MIME avec TNEF est utilisé lors de l’encodage du contenu des messages, toutes les propriétés des pièces jointes et le contenu se trouvent dans le flux TNEF. Le format TNEF elle-même est un seul fichier joint binaire nommé Winmail.dat, codés comme décrit MIME sans TNEF. 
  
Si MIME est utilisée sans TNEF, les fichiers joints sont envoyés en tant que parties de contenu de message MIME. Le nom de fichier est placé dans le paramètre *name* à l’en-tête *Content-type* de la pièce jointe. Le jeu de caractères de la pièce jointe est placé dans le paramètre de *jeu de caractères* pour le *type de contenu* ; Il et le contenu-transfert-codage sont déterminés par analyse du contenu de pièce jointe. Pièces jointes URL sont traités spécialement : 
  
- Si la pièce jointe est une URL (un fichier joint avec l’extension. URL), le mode d’accès défini est anonyme FTP, il est codé en tant qu’un message externe et le contenu du fichier (l’URL) est copié dans l’en-tête du message externe. *Content-type : message/externe-corps ; type d’accès = l’authentification anonyme ftp*  (Codage de transfert de contenu : 7 bits est supposé.) 
    
- Si seuls les caractères 7 bits sont détectés et aucune ligne ne dépasse 140 caractères, la pièce jointe est texte ASCII. *Type de contenu : texte brut ; CharSet = us-ascii Content-Transfer-Encoding : 7 bits* 
    
- Si long des lignes ou à 25 % de caractères 8 bits sont détectés, le contenu de pièce jointe est un texte et le jeu de caractères est déterminé par les paramètres régionaux. Il doit être choisie dans les jeux de caractères définis par la norme ISO 8859 standard. *Type de contenu : texte/ordinaire ; charset = ISO-8859-1*  (par exemple) 
    
     *Content-Transfer-Encoding : quoted-printable* 
    
- Si au moins 25 % des caractères possède le bit élevé, la pièce jointe est binaire. Il est codé à l’aide de l’algorithme en Base64. *Content-type : application/octet-flux*  (par défaut, basé sur l’extension de fichier) 
    
     * Content-Transfer-Encoding : base64 * 
    
Sur les messages sortants, le type de contenu doit être dérivé à partir de l’extension de nom de fichier à trois lettres. Ce mappage existe dans le Registre système. sous là est une valeur de chaîne nommée « Type de contenu » qui fournit le type de contenu MIME s’il est défini. Cet exemple est un fichier image TIFF :
  
HKEY_LOCAL_MACHINE\
  
Logiciels\
  
Microsoft\
  
Classes\
  
.tif
  
Type de contenu = « image/tiff »
  
S’il n’existe aucun mappage pour l’extension de fichier, le flux *d’application/octet* par défaut doit être utilisé. 
  
Sur les messages entrants, le type de contenu d’une pièce jointe doit toujours être copié à la propriété MAPI **PR_ATTACH_MIME_TAG** ([PidTagAttachMimeTag](pidtagattachmimetag-canonical-property.md)). Même si un nom de fichier est défini pour une pièce jointe, l’extension est mappée par le type de contenu doit être utilisée dans les **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) et les propriétés de **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) .
  
Le paramètre *name* est officiellement déconseillé par la spécification RFC 821. Comme les normes, Microsoft considère spécifiant un mappage de remplacement pour les noms de fichiers joints. 
  
Joint les messages sortants sont envoyés en tant que *-type de contenu : message/rfc822 * Messages dans les messages transférés sont codées de manière récursive, à l’emplacement adéquat. Entrant des composants de contenu de message avec *Content-Type : / multipartie* sont également mappés à des messages incorporés. 
  
Si uuencode avec TNEF est utilisé lors de l’encodage du contenu des messages, toutes les propriétés des pièces jointes et le contenu se trouvent dans le flux TNEF. Le format TNEF elle-même est un seul fichier joint binaire nommé Winmail.dat, codés comme décrit pour Uuencode sans TNEF.
  
Si uuencode est utilisée sans TNEF, tous les fichiers joints sont considérés comme des fichiers binaires et UUENCODE, suivant le texte du message. Le nom de fichier est présent dans l’en-tête uuencode :
  
 commencer 0755 Winmail.dat 
  
 ... données... 
  
 end 
  
Messages joints sont textized dans le texte du message. La hiérarchie de messages associées est toujours aplatie ; Autrement dit, les messages dans les messages transférés sont extraits au niveau supérieur.
  
Objets OLE incorporés sont ignorés.
  
Positions de rendu des pièces jointes sont transmises en réalité, à l’aide de la propriété **PR_ATTACH_RENDERING** ([PidTagAttachRendering](pidtagattachrendering-canonical-property.md)) dans le format TNEF. Si le format TNEF n’est pas utilisée, ils sont perdus. Pièces jointes entrants avec aucune position de rendu (y compris lorsqu’il n’existe aucune TNEF) n’ont leur position rendu 0xFFFFFFFF, autrement dit, aucune position dans le texte du message.
  
## <a name="see-also"></a>Voir aussi



[Mappage d’attributs de messagerie Internet sur des propriétés MAPI](mapping-of-internet-mail-attributes-to-mapi-properties.md)

