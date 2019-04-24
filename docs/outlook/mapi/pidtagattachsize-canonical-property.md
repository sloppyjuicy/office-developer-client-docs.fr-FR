---
title: Propriété canonique PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361088"
---
# <a name="pidtagattachsize-canonical-property"></a>Propriété canonique PidTagAttachSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la somme, en octets, des tailles de toutes les propriétés d'une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificateur :  <br/> |0x0E20  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets des pièces jointes exposent la propriété **PR_ATTACH_SIZE** . La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). Par conséquent, **PR_ATTACH_SIZE** est généralement plus volumineux que le contenu de la pièce jointe seule. 
  
Cette propriété peut être utilisée pour vérifier la taille approximative de la pièce jointe avant d'effectuer un transfert distant par modem et d'afficher des indicateurs de progression lors de l'enregistrement de la pièce jointe sur le disque. Elle est particulièrement utile avec les objets OLE attachés. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et Attachment.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

