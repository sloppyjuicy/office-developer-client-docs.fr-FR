---
title: Propriété canonique PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 033c1f5ce189033dab2a749ccefb5229c8db9379
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594978"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propriété canonique PidTagRemoteProgress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient un nombre qui indique l’état d’un transfert à distance.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificateur :  <br/> |0x3E0B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si aucun transfert n’est en cours, cette propriété doit être définie sur 1. Si un transfert est en cours, il doit être réglé sur une valeur de 0 à 100 indiquant le pourcentage d’achèvement du transfert.
  
Le texte associé au code d’état numérique apparaît dans la **propriété PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Les indicateurs suivants peuvent être définies pour cette propriété :
  
MSGSTATUS_REMOTE_DELETE
  
> Le transfert de message est supprimé.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Le transfert des messages est en cours.
    
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

