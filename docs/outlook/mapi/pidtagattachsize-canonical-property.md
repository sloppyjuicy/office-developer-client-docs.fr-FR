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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f3e4f19ab43a3da7c4840d762d5131813c83d996
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399745"
---
# <a name="pidtagattachsize-canonical-property"></a>Propriété canonique PidTagAttachSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les fonctions sum, en octets, des tailles de toutes les propriétés sur une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificateur :  <br/> |0x0E20  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les pièces jointes sous-objets exposent la propriété **PR_ATTACH_SIZE** . La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou la propriété **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). En conséquence, **PR_ATTACH_SIZE** est généralement plus volumineux que le contenu de la pièce jointe uniquement. 
  
Cette propriété peut être utilisée pour vérifier la taille approximative de la pièce jointe avant d’effectuer un transfert à distance par modem et pour afficher les indicateurs de progression lors de l’enregistrement de la pièce jointe sur le disque. Il est particulièrement utile avec les objets OLE attachés. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

