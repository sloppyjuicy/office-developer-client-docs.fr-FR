---
title: Propriété canonique PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786888"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a>Propriété canonique PidTagTextAttachmentCharset

  
  
**S’applique à**: Outlook 
  
Contient la valeur de jeu de caractères d’une pièce jointe.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |Aucun  <br/> |
|Identificateur :  <br/> |0x371B  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

Données de cette propriété sont dérivées d’un champ d’en-tête MIME Content-Type qui commence par « texte / », s’il existe un paramètre « charset ».
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

