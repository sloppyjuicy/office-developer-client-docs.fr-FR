---
title: Propriété canonique PidLidTimeZoneStruct
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a4dcb58b48342e54ae7c1b8fb28dbd05814805ad
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455439"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriété canonique PidLidTimeZoneStruct

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui ma visite le format persistant d’une structure [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , qui décrit le fuseau horaire à utiliser pour l’heure de début et de fin d’un rendez-vous périodique ou d’une demande de réunion. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTimeZoneStruct  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID long (LID) :  <br/> |0x00008233  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003, les versions antérieures de Outlook et les applications basées sur CDO (Collaboration Data Objects) 1.21 dont les utilisateurs n’ont pas exécuté l’outil de mise à jour du calendrier fourni par Outlook ou Exchange Server  stockez l’heure de début et l’heure de fin d’un rendez-vous périodique ou d’une demande de réunion en tant qu’heure relative, et stockez le fuseau horaire où le rendez-vous ou la demande de réunion est créé dans **dispidTimeZoneStruct**. Toutefois, ce schéma ignore qu’au fil du temps, les règles de fuseau horaire peuvent changer, ce qui entraîne certains rendez-vous et réunions que les utilisateurs ont programmés avant que les règles ne changent et se produisent à des moments incorrects. Les utilisateurs et les administrateurs qui n’exécutent pas Windows Vista ou qui n’ont pas de mise à jour automatique doivent utiliser les outils de rebasing de calendrier fournis par Outlook ou Exchange Server pour ajuster l’heure de ces rendez-vous et demandes de réunion. Pour plus d’informations sur ces outils de rebasing de calendrier et les API qui rebasent les calendriers, voir à propos de [la rebase des calendriers](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx) par programme pour l’heure d’été
  
Utilisez le format little-endian suivant lors de l’utilisation d’un flux obtenu à partir de **dispidTimeZoneStruct**, ou lors de la persistance de la structure **TZREG** dans un flux à valider dans la propriété binaire **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Cette propriété est définie sur une série périodique pour spécifier des informations de fuseau horaire et indique comment convertir des champs horaires entre l’heure locale et le temps universel coordonné (UTC).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
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

