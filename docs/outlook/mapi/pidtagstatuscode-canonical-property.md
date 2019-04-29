---
title: Propriété canonique PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418513"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propriété canonique PidTagStatusCode

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un masque de réindicateur des indicateurs qui indiquent l'état actuel d'une ressource de session. Tous les fournisseurs de services définissent les codes d'État comme le fait MAPI pour indiquer l'état du sous-système, le spouleur MAPI et le carnet d'adresses intégré.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_CODE  <br/> |
|Identificateur :  <br/> |0x3E04  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le code d'État doit apparaître dans le fichier MAPISVC. inf pour tous les fournisseurs. 
  
Les objets d'État sont implémentés par MAPI et par tous les fournisseurs de services. Il existe deux ensembles de valeurs valides pour les codes d'État, un ensemble pour tous les objets d'État et un autre ensemble pour les fournisseurs de transport uniquement. Tous les objets d'État peuvent définir cette propriété avec les valeurs suivantes:
  
STATUS_AVAILABLE 
  
> Indique que la ressource est opérationnelle.
    
STATUS_FAILURE 
  
> Indique que la ressource rencontre un problème. Pour les fournisseurs de services, STATUS_FAILURE indique que le fournisseur peut bientôt être arrêté pour mettre fin à la session en cours.
    
STATUS_OFFLINE 
  
> Indique que seules les données locales ou les services sont disponibles.
    
Les fournisseurs de transport peuvent également définir les propriétés **PR_STATUS_CODE** de leurs objets d'État sur les valeurs suivantes: 
  
STATUS_INBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message entrant. 
    
STATUS_INBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut recevoir des messages entrants.
    
STATUS_INBOUND_FLUSH 
  
> Indique que le fournisseur de transport télécharge les messages à partir de la file d'attente entrante.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message sortant. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut gérer les messages sortants.
    
STATUS_OUTBOUND_FLUSH 
  
> Indique que le fournisseur de transport télécharge les messages à partir de sa file d'attente sortante.
    
STATUS_REMOTE_ACCESS 
  
> Indique que le fournisseur de transport prend en charge l'accès à distance.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

