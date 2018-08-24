---
title: Propriété canonique PidLidBusinessCardCardPicture
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1b83316b599ea9ee62bde78cbd734dfb6b2d8b80
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588495"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Propriété canonique PidLidBusinessCardCardPicture

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient l’image à utiliser dans une carte de visite.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBCCardPicture  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008041  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être un graphique réseau portable (PNG) ou un flux au format JPEG. Cette propriété doit être utilisée conjointement avec la propriété **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) comme suit : **dispidBCCardPicture** ne doit pas être présent sur un contact se ** dispidBCDisplayDefinition** n’est pas présent. Cette propriété également ne doit pas être présente si les données **dispidBCCardPicture** ne requièrent pas une image de la carte. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

