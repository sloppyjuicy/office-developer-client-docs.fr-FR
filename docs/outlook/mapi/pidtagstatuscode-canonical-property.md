---
title: Propriété canonique PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fcd890f9fa7055abfd4eb6765434992e758ecb32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599395"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propriété canonique PidTagStatusCode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs qui indiquent l’état actuel d’une ressource de session. Tous les fournisseurs de services définissent des codes d’état, de même que MAPI pour signaler l’état du sous-système, dupooler MAPI et du carnet d’adresses intégré.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_CODE  <br/> |
|Identificateur :  <br/> |0x3E04  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le code d’état doit apparaître dans le fichier Mapisvc.inf pour tous les fournisseurs. 
  
Les objets d’état sont implémentés par MAPI et par tous les fournisseurs de services. Il existe deux ensembles de valeurs valides pour les codes d’état, l’un pour tous les objets d’état et l’autre pour les fournisseurs de transport uniquement. Tous les objets d’état peuvent définir cette propriété sur les valeurs suivantes :
  
STATUS_AVAILABLE 
  
> Indique que la ressource est opérationnelle.
    
STATUS_FAILURE 
  
> Indique que la ressource rencontre un problème. Pour les fournisseurs de services, STATUS_FAILURE indique que le fournisseur peut bientôt être arrêté pour mettre fin à la session en cours.
    
STATUS_OFFLINE 
  
> Indique que seuls les services ou données locaux sont disponibles.
    
Les fournisseurs de transport peuvent également définir les propriétés d’PR_STATUS_CODE **de** leurs objets d’état sur les valeurs suivantes : 
  
STATUS_INBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message entrant. 
    
STATUS_INBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut recevoir des messages entrants.
    
STATUS_INBOUND_FLUSH 
  
> Indique que le fournisseur de transport télécharge des messages à partir de la file d’attente entrante.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message sortant. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut gérer les messages sortants.
    
STATUS_OUTBOUND_FLUSH 
  
> Indique que le fournisseur de transport télécharge des messages à partir de sa file d’attente sortante.
    
STATUS_REMOTE_ACCESS 
  
> Indique que le fournisseur de transport prend en charge l’accès à distance.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

