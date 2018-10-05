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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6a84e51325fcb60c54c2f6b42af0c26a0efd3382
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396616"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a>Propriété canonique PidTagAttachPayloadClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur d’un champ d’en-tête X-charge utile-classe MIME.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W  <br/> |
|Identificateur :  <br/> |0x371A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête X-charge utile-classe à une entité MIME qui est analysée en tant que pièce jointe.
  
Lecteurs MIME doivent copier cette valeur de champ d’en-tête sur la valeur de la propriété correspondante. Lecteurs MIME doivent ignorer ce champ d’en-tête lorsqu’il apparaît sur une entité MIME qui est analysée en tant que message ou le corps du message, au lieu d’une pièce jointe.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet aux objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

