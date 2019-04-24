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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 9b4510a32fe14e4316a6bcddafcc163ee899436e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278892"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propriété canonique PidTagStatusString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un message qui indique l'état actuel d'une ressource de session. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificateur :  <br/> |0x3E08  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés permettent aux fournisseurs de services et à l'interface MAPI de fournir des informations spécifiques sur l'état d'une ressource de session, comme le carnet d'adresses intégré ou un fournisseur de services particulier. Cette propriété explique et fournit des informations supplémentaires sur un code d'État ou la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Tandis que **PR_STATUS_CODE** est requis pour tous les objets d'État, **PR_STATUS_STRING** et les propriétés associées sont facultatifs. Lorsque le fournisseur de transport ne fournit pas de valeur, le spouleur MAPI fournit une valeur par défaut. 
  
La chaîne est générée sur le même côté de l'appel de procédure distante que le spouleur MAPI; il transite par le biais de la mémoire partagée au lieu d'être marshalé dans une limite de processus.
  
## <a name="related-resources"></a>Ressources associées

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

