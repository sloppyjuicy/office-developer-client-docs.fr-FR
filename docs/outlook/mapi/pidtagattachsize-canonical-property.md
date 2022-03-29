---
title: Propriété canonique PidTagAttachSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachSize
api_type:
- HeaderDef
ms.assetid: 768b3215-dd9f-4aa0-b52c-178ca81a7b07
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: dcfc419aad08fd0511b0ea83b6d9f81afe02f282
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455145"
---
# <a name="pidtagattachsize-canonical-property"></a>Propriété canonique PidTagAttachSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la somme, en octets, de la taille de toutes les propriétés d’une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificateur :  <br/> |0x0E20  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièce jointe exposent **PR_ATTACH_SIZE** propriété. La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). Par conséquent, **PR_ATTACH_SIZE** est généralement plus grand que le contenu de la pièce jointe uniquement. 
  
Cette propriété permet de vérifier la taille approximative de la pièce jointe avant d’effectuer un transfert à distance par modem et d’afficher des indicateurs de progression lors de l’enregistrement de la pièce jointe sur le disque. Il est particulièrement utile avec les objets OLE attachés. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

