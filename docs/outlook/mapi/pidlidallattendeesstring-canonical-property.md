---
title: Propriété canonique PidLidAllAttendeesString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAllAttendeesString
api_type:
- COM
ms.assetid: 2ffc0609-341d-4e35-8f53-ed3096c6fa7f
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 11b4ea96283bbef2dcb9afb109a6a81102727efc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570456"
---
# <a name="pidlidallattendeesstring-canonical-property"></a>Propriété canonique PidLidAllAttendeesString

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Spécifie une liste de tous les participants à l’exception de l’organisateur, y compris les ressources et les participants de rédaction.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidAllAttendeesString  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008238  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Réunions  <br/> |
   
## <a name="remarks"></a>Remarques

La valeur de chaque participant est le nom du participant complet. Des entrées doivent être séparées par un point-virgule suivi d’un espace. Cette propriété n’est pas requise.
  
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

