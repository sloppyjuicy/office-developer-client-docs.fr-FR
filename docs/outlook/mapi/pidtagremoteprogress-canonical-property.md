---
title: Propriété canonique PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e1f57fd95ff38ef102cd74b0035dbb6b553259c9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569350"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propriété canonique PidTagRemoteProgress

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette propriété contient un nombre qui indique l’état d’un transfert à distance.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificateur :  <br/> |0x3E0B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si aucun transfert n’est en cours, cette propriété doit être définie sur 1. Si un transfert est en cours, il doit être défini sur une valeur comprise entre 0 et 100 indiquant le pourcentage de transfert d’achèvement.
  
Le texte associé au code d’état numérique s’affiche dans la propriété **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Les indicateurs suivants peuvent être définis pour cette propriété :
  
MSGSTATUS_REMOTE_DELETE
  
> Le transfert des messages est supprimé.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Le transfert de messages est en cours.
    
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

