---
title: Propriété canonique PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e89049186dfe32e6e76cd52324ef9aad37d8a82
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550462"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propriété canonique PidTagScheduleInfoAppointmentTombstone

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de blocs de données qui représentent des réunions qui ont été refusées.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificateur :  <br/> |0x686A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Les blocs de données commencent par un en-tête de valeurs de 32 bits définies comme :
  
|**Valeur**|**Description**|
|:-----|:-----|
|Identifier  <br/> |Ce champ doit être la valeur 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Ce champ doit avoir la valeur 0x00000014.  <br/> |
|Version  <br/> |Ce champ doit avoir la valeur 3.  <br/> |
|RecordsCount  <br/> |Nombre d’enregistrements qui suivent.  <br/> |
|RecordsSize  <br/> |Ce champ doit avoir la valeur 0x00000014.  <br/> |
   
L’en-tête est suivi des **entrées RecordsCount** de valeurs 32 bits définies comme suit : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|StartTime  <br/> |Heure de début de l’objet de réunion en minutes depuis le 1er janvier 1601 à minuit(UTC).  <br/> |
|EndTime  <br/> |Heure de fin de l’objet de réunion en minutes depuis le 1er janvier 1601 à minuit(UTC).  <br/> |
|GlobalObjectIdSize  <br/> |Taille, en octets, du champ GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |Valeur de la **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la réunion que cet enregistrement représente.  <br/> |
|UserName  <br/> |Les deux premiers octets sont la longueur de la chaîne PT_STRING8 suivante.  <br/> |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

