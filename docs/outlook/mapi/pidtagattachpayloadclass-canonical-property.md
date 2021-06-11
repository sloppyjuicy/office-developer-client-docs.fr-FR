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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327236"
---
# <a name="pidtagattachpayloadclass-canonical-property"></a>Propriété canonique PidTagAttachPayloadClass

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur d’un champ d’en-tête MIME X-Payload-Class.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PAYLOAD_CLASS, PR_ATTACH_PAYLOAD_CLASS_A, PR_ATTACH_PAYLOAD_CLASS_W  <br/> |
|Identificateur :  <br/> |0x371A  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Outlook application  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête de classe de charge utile X dans une entité MIME qui sera analysée en tant que pièce jointe.
  
Les lecteurs MIME doivent copier cette valeur de champ d’en-tête sur la valeur de la propriété correspondante. Les lecteurs MIME doivent ignorer ce champ d’en-tête lorsqu’il apparaît sur une entité MIME analysée sous forme de message ou de corps de message, plutôt que sous forme de pièce jointe.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convertit des conventions de messagerie standard Internet en objets de message.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

