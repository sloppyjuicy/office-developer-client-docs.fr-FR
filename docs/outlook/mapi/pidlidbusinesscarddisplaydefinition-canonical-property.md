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
ms.openlocfilehash: 34d29b9a15cc6f5a3f88a6477738eb63904e1fdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785085"
---
# <a name="pidlidbusinesscarddisplaydefinition-canonical-property"></a>Propriété canonique PidLidBusinessCardDisplayDefinition

  
  
**S’applique à**: Outlook 
  
Contient des détails de personnalisation de l’utilisateur pour l’affichage d’un contact dans une carte de visite.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidBCDisplayDefinition  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Address  <br/> |
|ID de type long (capot) :  <br/> |0x00008040  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Remarques

La disposition d’une carte de visite peut être représentée comme une image et un nombre de champs de texte. L’image peut être une photo du contact, ou une image de la carte. Champs de texte se composent d’une valeur à partir d’un autre jeu de propriétés sur le contact et une chaîne d’étiquette personnalisée facultative fournie par l’utilisateur. Notez que les valeurs multiples octets sont stockés dans le format little-endian dans la mémoire tampon.
  
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

