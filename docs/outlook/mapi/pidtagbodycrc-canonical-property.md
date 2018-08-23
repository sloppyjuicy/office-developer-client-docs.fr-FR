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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 55da942e59c619dd384bef58349aa3a00d4a6d8c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571471"
---
# <a name="pidtagbodycrc-canonical-property"></a>Propriété canonique PidTagBodyCrc

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une valeur de redondance cyclique (CRC) sur le texte du message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_BODY_CRC  <br/> |
|Identificateur :  <br/> |0x0E1C  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Remarques

La banque de messages permettre utiliser n’importe quel algorithme CRC qui génère une valeur PT_LONG. Il doit calculer cette propriété dans le cadre de la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) lorsque la propriété **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) a été définie pour la première fois, et chaque fois qu’il a été modifié par la suite.
  
Une application cliente utilise **PR_BODY_CRC** pour faciliter la comparaison de chaînes de texte de message contenues dans les propriétés **PR_BODY** ou leurs variantes. À l’aide de cette propriété, le client peut rapidement et facilement détecter lorsque le texte du message a été modifiée. Il peut réaliser des gains de performances significatifs en utilisant **PR_BODY_CRC** au lieu d’obtention **PR_BODY** à partir de la banque de messages et en les comparant avec une version locale. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

