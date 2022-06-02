---
title: Propriété canonique PidLidImageAttachmentsCompressionLevel
description: Décrit la propriété canonique PidLidImageAttachmentsCompressionLevel, qui définit un niveau de compression à appliquer aux pièces jointes d’image.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidImageAttachmentsCompressionLevel
api_type:
- COM
ms.assetid: cc169ba8-e9b7-42ad-8f0e-77b0843f95ea
ms.openlocfilehash: ce8bb7546f4eb1a69320b4b61d4c9a862accff76
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65854615"
---
# <a name="pidlidimageattachmentscompressionlevel-canonical-property"></a>Propriété canonique PidLidImageAttachmentsCompressionLevel

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit un niveau de compression à appliquer sur les pièces jointes d’image.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidImgAttchmtsCompressLevel  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Common  <br/> |
|ID long (LID) :  <br/> |0x00008593  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Configuration au moment de l’exécution  <br/> |
   
## <a name="remarks"></a>Remarques

Les niveaux de compression suivants sont valides :
  
```cpp
enum PictureCompressLevel
{
 pclOriginal = 0,
 pclEmail = 1,
 pclWeb = 2,
 pclDocuments = 3,
};
```

## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]] 
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

