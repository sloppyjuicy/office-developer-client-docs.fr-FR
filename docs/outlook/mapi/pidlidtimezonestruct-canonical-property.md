---
title: Propriété canonique PidLidTimeZoneStruct
description: Décrit la propriété canonique PidLidTimeZoneStruct, qui contient un flux qui correspond au format persistant d’une structure TZREG.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidTimeZoneStruct
api_type:
- COM
ms.assetid: 2acf0036-2f3e-4f90-8614-7aa667860f74
ms.openlocfilehash: 76fd138be5e95c5bd42ed98e043d529329a19807
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818060"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriété canonique PidLidTimeZoneStruct

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui correspond au format persistant d’une structure [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , qui décrit le fuseau horaire à utiliser pour l’heure de début et de fin d’un rendez-vous périodique ou d’une demande de réunion. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTimeZoneStruct  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008233  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003, les versions antérieures de Outlook et les applications basées sur Collaboration Data Objects (CDO) 1.21 dont les utilisateurs n’ont pas exécuté l’outil de mise à jour du calendrier fourni par Outlook ou Exchange Server  stockez l’heure de début et l’heure de fin d’un rendez-vous périodique ou d’une demande de réunion en tant qu’heure relative, et stockez le fuseau horaire dans lequel la demande de rendez-vous ou de réunion est créée dans **dispidTimeZoneStruct**. Toutefois, ce schéma ignore qu’au fil du temps, les règles de fuseau horaire peuvent changer, ce qui entraîne des rendez-vous et des réunions que les utilisateurs ont planifiés avant la modification des règles et se produisent à des moments incorrects. Les utilisateurs et administrateurs qui n’exécutent pas Windows Vista ou qui n’ont pas de mises à jour automatiques activées doivent utiliser les outils de rebasage de calendrier fournis par Outlook ou Exchange Server pour ajuster l’heure de ces rendez-vous et demandes de réunion. Pour plus d’informations sur ces outils et API de rebasage de calendriers qui réappamentent des calendriers, consultez [À propos du rebasage des calendriers par programmation pour l’heure d’été](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Utilisez le format little-endian suivant lors de l’analyse d’un flux obtenu à partir de **dispidTimeZoneStruct** ou lors de la conservation de la structure **TZREG** dans un flux pour valider la propriété binaire **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Cette propriété est définie sur une série périodique pour spécifier des informations de fuseau horaire et spécifie comment convertir des champs de temps entre l’heure locale et le temps universel coordonné (UTC).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications de protocole Exchange Server associées.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

