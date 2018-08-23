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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: a60bc55686e883cabd144af3a9badfb55f835472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593122"
---
# <a name="pidtagstatuscode-canonical-property"></a>Propriété canonique PidTagStatusCode

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un masque de bits d’indicateurs qui indiquent l’état actuel d’une ressource de session. Tous les fournisseurs de services de définissent les codes d’état comme MAPI pour créer des rapports sur l’état du sous-système, le spouleur MAPI et le carnet d’adresses intégré.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_STATUS_CODE  <br/> |
|Identificateur :  <br/> |0x3E04  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |État MAPI  <br/> |
   
## <a name="remarks"></a>Remarques

Le code d’état doit apparaître dans le fichier Mapisvc.inf pour tous les fournisseurs. 
  
Objets d’état sont implémentés par MAPI et par tous les fournisseurs de services. Il existe deux jeux de valeurs valides pour les codes d’état, un ensemble de tous les objets d’état et un autre ensemble pour les fournisseurs de transport uniquement. Tous les objets d’état peuvent définir cette propriété sur les valeurs suivantes :
  
STATUS_AVAILABLE 
  
> Indique que la ressource est opérationnelle.
    
VALEUR 
  
> Indique que la ressource est un problème. Pour les fournisseurs de service, la valeur indique que le fournisseur bientôt est arrêté à la fin de la session en cours.
    
STATUS_OFFLINE 
  
> Indique que les données locales uniquement ou les services sont disponibles.
    
Fournisseurs de transport peuvent également définir leur statut **PR_STATUS_CODE** propriétés des objets aux valeurs suivantes : 
  
STATUS_INBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message entrant. 
    
STATUS_INBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut recevoir des messages entrants.
    
STATUS_INBOUND_FLUSH 
  
> Indique que le fournisseur de transport téléchargement des messages à partir de la file d’attente entrante.
    
STATUS_OUTBOUND_ACTIVE 
  
> Indique que le fournisseur de transport reçoit un message sortant. 
    
STATUS_OUTBOUND_ENABLED 
  
> Indique que le fournisseur de transport peut gérer les messages sortants.
    
STATUS_OUTBOUND_FLUSH 
  
> Indique que le fournisseur de transport est téléchargement des messages à partir de sa file d’attente sortante.
    
STATUS_REMOTE_ACCESS 
  
> Indique que le fournisseur de transport prend en charge l’accès à distance.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)


[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

