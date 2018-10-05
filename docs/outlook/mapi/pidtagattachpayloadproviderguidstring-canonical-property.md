---
title: Propriété canonique PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389042"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>Propriété canonique PidTagAttachPayloadProviderGuidString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur d’un champ d’en-tête MIME X-charge utile-fournisseur-Guid.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|Identificateur :  <br/> |0x3719  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |Application Outlook  <br/> |
   
## <a name="remarks"></a>Remarques

Pour définir la valeur de ces propriétés, les clients MIME doivent écrire un champ d’en-tête X-charge utile-fournisseur-Guid à une entité MIME qui est analysée en tant que pièce jointe.
  
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

