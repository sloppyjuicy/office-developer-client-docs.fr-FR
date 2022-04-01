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
description: Contient une liste de blocs de données qui représentent des réunions qui ont été refusées pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: a32c6f331fe759ce15564621cd740b59dae398e4
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64521852"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propriété canonique PidTagScheduleInfoAppointmentTombstone

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une liste de blocs de données qui représentent les réunions qui ont été refusées.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificateur :  <br/> |0x686A  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Libre/Occupé  <br/> |
   
## <a name="remarks"></a>Remarques

Les blocs de données commencent par un en-tête de valeurs de 32 bits définies comme :
  
|**Valeur**|**Description**|
|:-----|:-----|
|Identifier  <br/> |Ce champ doit être la valeur 0xBEDEAFCD. |
|HeaderSize  <br/> |Ce champ doit avoir la valeur 0x00000014. |
|Version  <br/> |Ce champ doit avoir la valeur 3. |
|RecordsCount  <br/> |Nombre d’enregistrements qui suivent. |
|RecordsSize  <br/> |Ce champ doit avoir la valeur 0x00000014. |
   
L’en-tête est suivi des **entrées RecordsCount** de valeurs 32 bits définies comme suit : 
  
|**Valeur**|**Description**|
|:-----|:-----|
|StartTime  <br/> |Heure de début de l’objet de réunion en minutes depuis le 1er janvier 1601 à minuit(UTC). |
|EndTime  <br/> |Heure de fin de l’objet de réunion en minutes depuis le 1er janvier 1601 à minuit(UTC). |
|GlobalObjectIdSize  <br/> |Taille, en octets, du champ GlobalObjectId. |
|GlobalObjectId  <br/> |Valeur de la **propriété LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) de la réunion représentée par cet enregistrement. |
|UserName  <br/> |Les deux premiers octets sont la longueur de la chaîne PT_STRING8 suivante. |
   
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
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

