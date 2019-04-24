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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335433"
---
# <a name="pidtagremoteprogress-canonical-property"></a>Propriété canonique PidTagRemoteProgress

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette propriété contient un nombre qui indique l'état d'un transfert distant.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_REMOTE_PROGRESS  <br/> |
|Identificateur :  <br/> |0x3E0B  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Si aucun transfert n'est en cours, cette propriété doit être définie sur 1. Si un transfert est en cours, il doit être défini sur une valeur comprise entre 0 et 100 indiquant le pourcentage d'achèvement du transfert.
  
Le texte associé au code d'état numérique apparaît dans la propriété **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).
  
Les indicateurs suivants peuvent être définis pour cette propriété:
  
MSGSTATUS_REMOTE_DELETE
  
> Le transfert du message est supprimé.
    
MSGSTATUS_REMOTE_DOWNLOAD
  
> Le transfert du message est en cours.
    
## <a name="related-resources"></a>Ressources associées

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

