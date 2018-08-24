---
title: Propriété canonique PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: ebc7ed4563040e16c71e1df1094667f87a4c09b2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572367"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propriété canonique PidLidMeetingType

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Indique le type de demande de réunion ou de mise à jour de la réunion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidMeetingType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID de type long (capot) :  <br/> |0x00000026  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit avoir une des options suivantes :
  
|**Propriété**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Non spécifié.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Demande de réunion initiale.  <br/> |
|mtgFull  <br/> |0 x 00010000  <br/> |Mise à jour intégrale.  <br/> |
|mtgInfo  <br/> |0 x 00020000  <br/> |Mise à jour d’information.  <br/> |
|mtgOutOfDate  <br/> |0 x 00080000  <br/> |Une nouvelle demande de réunion ou une mise à jour de la réunion a été reçu après celle-ci.  <br/> |
|mtgDelegatorCopy  <br/> |0 x 00100000  <br/> |Elle est définie sur la copie de la personne qui a délégué lorsqu’un délégué poignées réunion les objets liés.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

