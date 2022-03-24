---
title: Propriété canonique PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: Contient un message qui indique l’état actuel d’une ressource de session, telle que le carnet d’adresses intégré ou un fournisseur de services particulier.
ms.openlocfilehash: f086a691ee3ef71b864ce4379e12151e11fbe5dd
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763228"
---
# <a name="pidtagstatusstring-canonical-property"></a>Propriété canonique PidTagStatusString

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un message qui indique l’état actuel d’une ressource de session. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W  <br/> |
|Identificateur :  <br/> |0x3E08  <br/> |
|Type de données :  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Ces propriétés donnent aux fournisseurs de services et à MAPI la possibilité de fournir des informations spécifiques sur l’état d’une ressource de session, telles que le carnet d’adresses intégré ou un fournisseur de services particulier. Cette propriété explique et fournit des informations supplémentaires sur un code d’état ou la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)). Alors **PR_STATUS_CODE** est requise pour tous les objets d’état **, les** PR_STATUS_STRING et les propriétés associées sont facultatives. Lorsque le fournisseur de transport ne fournit pas de valeur, lepooler MAPI fournit une valeur par défaut. 
  
La chaîne est générée du même côté de l’appel de procédure distante que lepooler MAPI ; Il parcourt la mémoire partagée au lieu d’être marshalé à travers une limite de processus.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

