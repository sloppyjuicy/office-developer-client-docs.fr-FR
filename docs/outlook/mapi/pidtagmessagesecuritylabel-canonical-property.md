---
title: Propriété canonique PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f7d43edc01eadcf14ec75cd09d2a3ac3710e9974
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64524274"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a>Propriété canonique PidTagMessageSecurityLabel

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une étiquette de sécurité pour un message.
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_SECURITY_LABEL  <br/> |
|Identificateur :  <br/> |0x001E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit la base sur laquelle la **propriété PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protège un message. Son association avec le contenu du message est garantie par le jeton.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

