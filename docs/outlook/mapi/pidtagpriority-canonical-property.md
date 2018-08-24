---
title: Propriété canonique PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e69211c15a3a05b3396dc1510483fddafe3faeb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588607"
---
# <a name="pidtagpriority-canonical-property"></a>Propriété canonique PidTagPriority

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique la priorité relative d’un message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PRIORITY  <br/> |
|Identificateur :  <br/> |0x0026  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |E-mail  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété et la propriété **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) ne doivent pas être confondus. Importance indique une valeur pour les utilisateurs, tandis que la priorité indique l’ordre ou la vitesse à laquelle le message doit être envoyé par le logiciel de système de messagerie. Priorité plus élevée indique généralement un coût plus élevé. Importance supérieure est généralement associée à un autre affichage par l’interface utilisateur.
  
La priorité d’un message de rapport doit être identique à la priorité du message d’origine signalée.
  
Cette propriété peut avoir exactement une des valeurs suivantes :
  
PRIO_NONURGENT 
  
> Le message n’est pas urgent.
    
PRIO_NORMAL 
  
> Le message a une priorité normale.
    
PRIO_URGENT 
  
> Le message est urgent.
    
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

