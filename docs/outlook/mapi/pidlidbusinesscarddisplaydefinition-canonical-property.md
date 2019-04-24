---
title: Propriété canonique PidLidBusinessCardDisplayDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f25f8a538ff61bc7e04c234efd7404b1c866d64d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342034"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Propriété canonique PidLidBusinessCardDisplayDefinition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des détails sur la personnalisation de l'utilisateur pour l'affichage d'un contact sous forme de carte de visite.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBCDisplayDefinition  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Address  <br/> |
|ID long (couvercle):  <br/> |0x00008040  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La mise en page d'une carte de visite peut être représentée sous la forme d'une image et de plusieurs champs de texte. L'image peut être une photo de contact ou une image de carte. Les champs de texte se composent d'une valeur d'une autre propriété définie sur le contact et d'une chaîne d'étiquette personnalisée facultative fournie par l'utilisateur. Notez que les valeurs multioctets sont stockées au format Little endian dans la mémoire tampon.
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les contacts et les listes de distribution personnelle.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

