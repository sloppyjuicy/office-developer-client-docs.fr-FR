---
title: Propriété canonique PidTagAttachPayloadClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadClass
api_type:
- HeaderDef
ms.assetid: bc4de217-8241-45e7-9e97-8f0c1b16691a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: cef412d212bf29cfd1a1d5c4b2911440fae6a15e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785743"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a>Propriété canonique PidTagAttachPayloadClass

  
  
**S’applique à**: Outlook 
  
Contient la valeur d’un champ d’en-tête X-charge utile-classe MIME.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W  <br/> |
|Identificateur :  <br/> |0x371A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Zone :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête X-charge utile-classe à une entité MIME qui est analysée en tant que pièce jointe.
  
Lecteurs MIME doivent copier cette valeur de champ d’en-tête sur la valeur de la propriété correspondante. Lecteurs MIME doivent ignorer ce champ d’en-tête lorsqu’il apparaît sur une entité MIME qui est analysée en tant que message ou le corps du message, au lieu d’une pièce jointe.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
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

