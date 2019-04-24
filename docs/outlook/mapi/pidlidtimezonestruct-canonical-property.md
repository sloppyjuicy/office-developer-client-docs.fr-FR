---
title: Propriété canonique PidLidTimeZoneStruct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346374"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriété canonique PidLidTimeZoneStruct

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui correspond au format persistant d'une structure [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , qui décrit le fuseau horaire à utiliser pour l'heure de début et de fin d'une demande de réunion ou de rendez-vous périodique. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTimeZoneStruct  <br/> |
|Jeu de propriétés:  <br/> |PSETID_Appointment  <br/> |
|ID long (couvercle):  <br/> |0x00008233  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003, versions antérieures d'Outlook et applications basées sur des objets CDO (Collaboration Data Objects) 1,21 dont les utilisateurs n'ont pas exécuté l'outil de mise à jour de calendrier fourni par Outlook ou Exchange Server stockent l'heure de début et l'heure de fin d'une rendez-vous périodique ou une demande de réunion en tant que heure relative, et stockez le fuseau horaire dans lequel la demande de rendez-vous ou de réunion est créée dans **dispidTimeZoneStruct**. Toutefois, ce modèle ignore que, dans le temps, les règles de fuseau horaire peuvent varier, ce qui entraîne des rendez-vous et des réunions que les utilisateurs ont planifiés avant la modification des règles et qui se produisent à des moments incorrects. Les utilisateurs et administrateurs qui n'exécutent pas Windows Vista ou qui n'ont pas de mises à jour automatiques activées doivent utiliser les outils de relocalisation de calendrier fournis par Outlook ou Exchange Server pour ajuster le temps de ces rendez-vous et demandes de réunion. Pour plus d'informations sur ces outils de relocalisation de calendrier et les API qui rebasent les calendriers, voir [à propos de la relocalisation des calendriers par programmation pour l'heure d'été](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx) .
  
Utilisez le format Little-endian suivant lors de l'analyse d'un flux de flux obtenu à partir de **dispidTimeZoneStruct**ou lors de la persistance de la structure **TZREG** dans un flux pour la validation de la propriété binaire **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Cette propriété est définie sur une série périodique pour spécifier les informations de fuseau horaire, et indique comment convertir les champs d'heure entre l'heure locale et l'heure UTC (Coordinated Universal Time).
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

