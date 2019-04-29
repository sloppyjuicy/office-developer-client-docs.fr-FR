---
title: Propriété canonique PidTagBodyCrc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyCrc
api_type:
- HeaderDef
ms.assetid: 6efe9dc3-e988-4042-ab02-2863b5e0f294
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 416486c3b06c485a1fa6525b54c37a6e0d23f56c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415179"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propriété canonique PidTagBodyCrc

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une valeur de contrôle de redondance cyclique (CRC) sur le texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_CRC  <br/> |
|Identificateur :  <br/> |0x0E1C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

La Banque de messages peut utiliser n'importe quel algorithme CRC qui génère une valeur PT_LONG. Il doit calculer cette propriété dans le cadre de la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) lorsque la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) a été définie pour la première fois et chaque fois qu'elle a été modifiée par la suite.
  
Une application cliente utilise **PR_BODY_CRC** pour faciliter la comparaison des chaînes de texte de message contenues dans les propriétés **PR_BODY** ou leurs variantes. À l'aide de cette propriété, le client peut rapidement et facilement détecter lorsque le texte du message a changé. Elle peut réaliser des gains de performances significatifs à l'aide de **PR_BODY_CRC** au lieu d'obtenir des **PR_BODY** à partir de la Banque de messages et de la comparer avec une version locale. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés indiquées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

