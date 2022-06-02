---
title: Propriété canonique PidLidBusinessCardCardPicture
description: Décrit la propriété canonique PidLidBusinessCardCardPicture, qui contient l’image à utiliser sur une carte de visite.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidBusinessCardCardPicture
api_type:
- COM
ms.assetid: 2c7af147-f7eb-41ef-8403-93584a2041ba
ms.openlocfilehash: f9307f961baf040844a4472387c374451d5fc63b
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854503"
---
# <a name="pidlidbusinesscardcardpicture-canonical-property"></a>Propriété canonique PidLidBusinessCardCardPicture

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient l’image à utiliser sur une carte de visite.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBCCardPicture  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008041  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être un flux PNG (Portable Network Graphics) ou JPEG. Cette propriété doit être utilisée conjointement avec la propriété **dispidBCDisplayDefinition** ([PidLidBusinessCardDisplayDefinition](pidlidbusinesscarddisplaydefinition-canonical-property.md)) comme suit : **dispidBCCardPicture** ne doit pas être présent sur un contact si **dispidBCDisplayDefinition** n’est pas présent. Cette propriété ne doit pas non plus être présente si les données de **dispidBCCardPicture** ne nécessitent pas d’image de carte. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations autorisées pour les contacts et les listes de distribution personnelles.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

