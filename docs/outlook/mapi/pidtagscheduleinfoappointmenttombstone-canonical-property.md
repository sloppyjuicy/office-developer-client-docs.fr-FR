---
title: Propriété canonique PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e554a496dd1869dd7c07b315d92a136676e05006
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590042"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propriété canonique PidTagScheduleInfoAppointmentTombstone

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient une liste de blocs de données qui représentent les réunions qui ont été refusées.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificateur :  <br/> |0x686A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Informations de disponibilité  <br/> |
   
## <a name="remarks"></a>Remarques

Les blocs de données commencent par un en-tête de valeurs 32 bits définie en tant que :
  
|**Valeur**|**Description**|
|:-----|:-----|
|Identifier  <br/> |Ce champ doit être la valeur 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Ce champ doit avoir la valeur 0x00000014.  <br/> |
|Version  <br/> |Ce champ doit avoir la valeur 3.  <br/> |
|RecordsCount  <br/> |Le nombre d’enregistrements qui suivent.  <br/> |
|RecordsSize  <br/> |Ce champ doit avoir la valeur 0x00000014.  <br/> |
   
L’en-tête est suivi d’entrées **RecordsCount** des valeurs 32 bits définies en tant que : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|StartTime  <br/> |Heure de début de l’objet de la réunion en minutes depuis minuit, le 1er janvier 1601 UTC.  <br/> |
|EndTime  <br/> |Heure de fin de l’objet de la réunion en minutes depuis minuit, le 1er janvier 1601 UTC.  <br/> |
|GlobalObjectIdSize  <br/> |La taille, en octets, du champ GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |La valeur de la propriété **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la réunion cet enregistrement représente.  <br/> |
|UserName  <br/> |Les deux premiers octets sont la longueur de la chaîne PT_STRING8 qui suit.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
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

