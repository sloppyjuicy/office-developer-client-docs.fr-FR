---
title: Propriété canonique PidTagAttachSize
description: Décrit la propriété canonique PidTagAttachSize, qui contient la somme, en octets, des tailles de toutes les propriétés sur une pièce jointe.
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
ms.openlocfilehash: b3970dc8c70f30809ca1bd02b9805c51ca2dc45a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816527"
---
# <a name="pidtagattachsize-canonical-property"></a>Propriété canonique PidTagAttachSize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la somme, en octets, des tailles de toutes les propriétés d’une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_SIZE  <br/> |
|Identificateur :  <br/> |0x0E20  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Il est recommandé que les sous-objets de pièce jointe exposent la propriété **PR_ATTACH_SIZE** . La somme contenue dans **PR_ATTACH_SIZE** inclut la taille de la propriété **PR_ATTACH_DATA_BIN** ([PidTagAttachDataBinary](pidtagattachdatabinary-canonical-property.md)) ou **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)). Par conséquent, **PR_ATTACH_SIZE** est généralement plus grand que le contenu de la pièce jointe seule. 
  
Cette propriété peut être utilisée pour vérifier la taille approximative de la pièce jointe avant d’effectuer un transfert à distance par modem et pour afficher les indicateurs de progression lors de l’enregistrement de la pièce jointe sur le disque. Il est particulièrement utile avec les objets OLE attachés. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageSize](pidtagmessagesize-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

