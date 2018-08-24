---
title: Propriété canonique PidTagScheduleInfoDelegateNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateNames
api_type:
- COM
ms.assetid: 592d9c78-4487-4c68-8ae7-4cd3d6265685
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 06462f992ec640992b95b89a618e7d82290eeeef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574502"
---
# <a name="pidtagscheduleinfodelegatenames-canonical-property"></a>Propriété canonique PidTagScheduleInfoDelegateNames

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient les noms des délégués.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_DELEGATE_NAMES, PR_SCHDINFO_DELEGATE_NAMES_A, PR_SCHDINFO_DELEGATE_NAMES_W  <br/> |
|Identificateur :  <br/> |0x6844  <br/> |
|Type de données :  <br/> |PT_MV_STRING8, PT_MV_UNICODE  <br/> |
|Domaine :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque entrée de ces propriétés doit contenir la valeur de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du carnet d’adresses de chaque délégué.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Spécifie les méthodes pour la connexion et configurer des boîtes aux lettres en tant que les délégués et les interactions avec les objets de messagerie et de calendrier lorsqu’ils agissent au nom d’un autre utilisateur.
    
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

