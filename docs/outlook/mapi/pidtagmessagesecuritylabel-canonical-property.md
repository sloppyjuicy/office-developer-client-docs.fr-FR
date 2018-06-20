---
title: Propriété canonique PidTagMessageSecurityLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSecurityLabel
api_type:
- HeaderDef
ms.assetid: aae41f1b-19bb-40c7-8564-0c87a5a4e47c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 24cf7d8d7b025e5a013ce3a5c1bb03da5ae8a6a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786235"
---
# <a name="pidtagmessagesecuritylabel-canonical-property"></a>Propriété canonique PidTagMessageSecurityLabel

  
  
**S’applique à**: Outlook 
  
Contient une étiquette de sécurité pour un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_SECURITY_LABEL  <br/> |
|Identificateur :  <br/> |0x001E  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Serveur  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit la base sur laquelle la propriété **PR_MESSAGE_TOKEN** ([PidTagMessageToken](pidtagmessagetoken-canonical-property.md)) protège un message. L’association avec le contenu du message est garantie par le jeton.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

