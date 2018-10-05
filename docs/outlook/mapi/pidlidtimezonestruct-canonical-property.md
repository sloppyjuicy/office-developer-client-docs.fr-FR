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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b9c2a1bbf519379c1735c489c2dcd3fcfb395a60
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401614"
---
# <a name="pidlidtimezonestruct-canonical-property"></a>Propriété canonique PidLidTimeZoneStruct

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un flux qui mappe sur le format persistant d’une structure [TZREG](https://msdn.microsoft.com/library/bb820983%28v=office.12%29.aspx) , qui décrit le fuseau horaire à utiliser pour l’heure de début et de fin d’une demande de réunion ou un rendez-vous périodique. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |dispidTimeZoneStruct  <br/> |
|Jeu de propriétés :  <br/> |PSETID_Appointment  <br/> |
|ID de type long (capot) :  <br/> |0x00008233  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Calendrier  <br/> |
   
## <a name="remarks"></a>Remarques

Microsoft Office Outlook 2003, les versions antérieures d’Outlook et les applications basées sur Collaboration Data Objects (CDO) 1.21 dont les utilisateurs n’ont pas exécuter l’outil de mise à jour de calendrier fournie par Outlook ou Exchange Server stockent l’heure de début et heure de fin d’un périodique rendez-vous ou une demande de réunion en tant qu’heure relative et de stocker le fuseau horaire dans lequel la demande de réunion ou de rendez-vous est créée dans **dispidTimeZoneStruct**. Toutefois, ce schéma ignore qu’au fil du temps, les règles de fuseau horaire peuvent changer, entraînant des rendez-vous et des réunions que les utilisateurs avant les règles modifiées et se produisent à des moments incorrectes. Les utilisateurs et les administrateurs qui n’exécutent pas Windows Vista ou qui n’ont pas de mises à jour automatiques activées doivent utiliser le calendrier redéfinition des outils fournis par Outlook ou Exchange Server pour régler l’heure de ces rendez-vous et des demandes de réunion. Pour plus d’informations sur ces outils de redéfinition de calendrier et les API qui redéfinir des calendriers, voir [à propos des calendriers de redéfinition par programme à l’heure](https://msdn.microsoft.com/library/38b342d9-ab10-04b6-5490-9a45f847a60f%28Office.15%29.aspx)
  
Utilisez le format little-endian suivant lors de l’analyse d’un flux de données obtenu à partir de **dispidTimeZoneStruct**, ou lors de la persistance de la structure **TZREG** dans un flux pour valider à la propriété binaire **dispidTimeZoneStruct** . 
  
```cpp
long        lBias;           // offset from GMT
long        lStandardBias;   // offset from bias during standard time
long        lDaylightBias;   // offset from bias during daylight time
WORD        wStandardYear;      // matches the stStandardDate's wYear member
SYSTEMTIME  stStandardDate;  // time to switch to standard time
WORD        wDaylightYear;      // matches the stDaylightDate's wYear field
SYSTEMTIME  stDaylightDate;  // time to switch to daylight time
```

Cette propriété est définie sur une série périodique pour spécifier les informations de fuseau horaire et indique comment convertir les champs de temps entre l’heure locale et le temps universel coordonné (UTC).
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

