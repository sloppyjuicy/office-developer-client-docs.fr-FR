---
title: Propriété canonique PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e8370a613162e3bc8d4395a18e9a7e177255b9b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567299"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propriété canonique PidTagStatusString

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un message qui indique l’état actuel d’une ressource de session. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificateur :  <br/> |0x3E08  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés donnent MAPI la possibilité de fournir des informations spécifiques sur l’état d’une ressource de session, tel que le carnet d’adresses intégré ou un fournisseur de services et les fournisseurs de services. Cette propriété explique et fournit des informations supplémentaires sur un code d’état ou la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Tandis que **PR_STATUS_CODE** est requis pour tous les objets d’état, **PR_STATUS_STRING** et les propriétés associées sont facultatives. Lorsque le fournisseur de transport ne fournit pas de valeur, le spouleur MAPI fournit une valeur par défaut. 
  
La chaîne est générée sur le même côté de l’appel de procédure distante en tant que le spouleur MAPI ; qu’elle traverse mémoire partagée au lieu de marshalé sur une limite de processus.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

