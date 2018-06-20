---
title: Propriété canonique PidTagAttachMimeTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachMimeTag
api_type:
- HeaderDef
ms.assetid: cbc4585d-f970-4b22-ac08-d7fc91bff3d3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6f65d67903fa9ebb255345f8666cd53de5512cab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785737"
---
# <a name="pidtagattachmimetag-canonical-property"></a>Propriété canonique PidTagAttachMimeTag

  
  
**S’applique à**: Outlook 
  
Contient des informations de mise en forme sur une pièce jointe Multipurpose Internet Mail Extensions (MIME). 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_MIME_TAG, PR_ATTACH_MIME_TAG_A, PR_ATTACH_MIME_TAG_W  <br/> |
|Identificateur :  <br/> |0x370E  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

Si la propriété **PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) contient la valeur **OID_MIMETAG**, le fournisseur de transport doit se présenter ces propriétés pour déterminer la façon dont la pièce jointe est mis en forme. 
  
Ces propriétés sont copiées à partir du paramètre type de contenu de l’en-tête MIME entrant. La composition de la chaîne est définie dans le document RFC 1521. Le format est type/sous-type, telles que l’application/binaire ou texte/ordinaire. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Spécifie les propriétés des messages codés géré par des droits.
    
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

