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
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331576"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propriété canonique PidLidMeetingType

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique le type de demande de réunion ou de mise à jour de réunion.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidMeetingType  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Meeting  <br/> |
|ID long (LID) :  <br/> |0x00000026  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de cette propriété doit être définie sur l’une des valeurs suivantes :
  
|**Propriété**|**Valeur**|**Description**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Non spécifié.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Demande de réunion initiale.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Mise à jour complète.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Mise à jour d’informations.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Une demande de réunion ou une mise à jour de réunion plus nouvelle a été reçue après celle-ci.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Cette fonction est définie sur la copie du délégant lorsqu’un délégué gère des objets liés à la réunion.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

