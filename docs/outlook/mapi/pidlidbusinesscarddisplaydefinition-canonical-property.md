---
title: Propriété canonique PidLidBusinessCardDisplayDefinition
description: Décrit la propriété canonique PidLidBusinessCardDisplayDefinition, qui contient les détails de personnalisation de l’utilisateur pour l’affichage d’un contact en tant que carte de visite.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidBusinessCardDisplayDefinition
api_type:
- COM
ms.assetid: c0b956dd-7139-49e3-a32a-d70bfb11e0b1
ms.openlocfilehash: 7dcb110b5d992634aa868334ab29409f1531b609
ms.sourcegitcommit: 1b44c8f9eac3aedaf7fe7ec70c808fe8ed7d4b99
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65853978"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Propriété canonique PidLidBusinessCardDisplayDefinition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient les détails de personnalisation de l’utilisateur pour l’affichage d’un contact en tant que carte de visite.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBCDisplayDefinition  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID long (LID) :  <br/> |0x00008040  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La disposition d’une carte de visite peut être représentée sous la forme d’une image et d’un certain nombre de champs de texte. L’image peut être une photo de contact ou une image de carte. Les champs de texte sont constitués d’une valeur d’une autre propriété définie sur le contact et d’une chaîne d’étiquette personnalisée facultative fournie par l’utilisateur. Notez que les valeurs de plusieurs octets sont stockées au format little-endian dans la mémoire tampon.
  
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

