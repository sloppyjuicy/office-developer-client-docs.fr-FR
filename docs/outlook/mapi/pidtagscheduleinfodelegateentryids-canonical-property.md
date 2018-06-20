---
title: Propriété canonique PidTagScheduleInfoDelegateEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDelegateEntryIds
api_type:
- COM
ms.assetid: c178a4e4-6f4c-409c-9db3-f6338bd4f40f
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8ea60fb989cd85b23e6dd9302bc03a9b5befd20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786699"
---
# <a name="pidtagscheduleinfodelegateentryids-canonical-property"></a>Propriété canonique PidTagScheduleInfoDelegateEntryIds

  
  
**S’applique à**: Outlook 
  
Contient **identificateurs d’entrée** des délégués. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_DELEGATE_ENTRYIDS  <br/> |
|Identificateur :  <br/> |0x6845  <br/> |
|Type de données :  <br/> |PT_MV_BINARY  <br/> |
|Zone :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Chaque entrée doit contenir la valeur de la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’entrée de carnet d’adresses de chaque délégué. Cette propriété doit être définie dans l’objet d’informations de délégué.
  
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
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

