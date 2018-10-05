---
title: À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 0dec535d-d48f-39a5-97d5-0bd109134b3b
description: Les propriétés de fuseau horaire, PidLidAppointmentTimeZoneDefinitionEndDisplay, PidLidAppointmentTimeZoneDefinitionRecur et PidLidAppointmentTimeZoneDefinitionStartDisplay sont binaire nommé de propriétés, chacun d'entre eux contient un flux qui mappe sur le format persistant d’une structure TZDEFINITION.
ms.openlocfilehash: f94b751a55aa852c962eebe5d46968e9e622e315
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398618"
---
# <a name="about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property"></a>À propos de la persistance de TZDEFINITION dans un flux de validation dans une propriété binaire

Les propriétés de fuseau horaire, [PidLidAppointmentTimeZoneDefinitionEndDisplay](https://msdn.microsoft.com/library/7b6193cb-612b-408e-b9bc-285df313e2cc%28Office.15%29.aspx), [PidLidAppointmentTimeZoneDefinitionRecur](https://msdn.microsoft.com/library/52fd57a0-9e34-4452-9ecd-2acb454446c9%28Office.15%29.aspx)et [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) sont binaire nommé de propriétés, chacun d'entre eux contient un flux qui mappe sur le format d’une structure [TZDEFINITION](tzdefinition.md) persistant. 
  
Cette rubrique décrit un format endian peu qui peut être utilisé lors de la persistance **TZDEFINITION** dans un flux pour valider une des trois propriétés binaires. Utilisez le même format de primauté dans un analyseur pour interpréter une valeur de flux de données obtenue à partir d’une de ces propriétés. 
  
```cpp
BYTE  bMajorVersion;    // breaking change
BYTE  bMinorVersion;    // extensibility
WORD  cbHeader;         // size of following data until TZREG sub structure
WORD  wFlags;
if (TZDEFINITION_FLAG_VALID_GUID)
   GUID  guid;                // guid
if (TZDEFINITION_FLAG_VALID_KEYNAME)     
    WORD   cchKeyName;        // does not include null char
    WCHAR  rgchKeyName;       // not null terminated
    WORD  cRules;             // number of rules
// for each rule
   BYTE        bMajorVersion;         // breaking change
   BYTE        bMinorVersion;         // extensibility
   WORD        cbRule;                // size of following data
   WORD        wFlags;                // flags
   SYSTEMTIME  stStart;               // GMT when this rule starts
// Following are the fields of the TZREG sub structure
   long        lBias;                // offset from GMT
   long        lStandardBias;        // offset from bias during standard time
   long        lDaylightBias;        // offset from bias during daylight time
   SYSTEMTIME  stStandardDate;       // time to switch to standard time
   SYSTEMTIME  stDaylightDate;       // time to switch to daylight time
```

Le numéro de version principal est utilisé pour modifier une minute. Les clients qui ne sont pas familiarisés avec le numéro de version principal doivent traiter la propriété comme si elle n’est pas présente. Écriture de la structure des clients doivent spécifier la constante **TZ_BIN_VERSION_MAJOR**. 
  
Le numéro de version secondaire est utilisé pour l’extensibilité. Les clients qui ne sont pas familiarisés avec le numéro de version secondaire doivent lire les données qu’ils comprennent et ignorer les données qui peuvent être ajoutées à chaque règle ou dans le flux global. Écriture de la structure des clients doivent spécifier la constante **TZ_BIN_VERSION_MINOR**. 
  
Si un analyseur ne comprend pas la version principale de l’en-tête, il ne doit pas lire le reste de la structure et se comportent comme si les données sont manquantes. Si un analyseur ne comprend pas la version secondaire de l’en-tête, elle doit utiliser **cbHeader** d’ignorer les parties qu’il ne comprend pas avance pour lire les parties du flux de données qu’il comprend. 
  
La valeur de **wFlags** est toujours **TZDEFINITION_FLAG_VALID_KEYNAME**. Nom de la clé a une taille maximale de **MAX_PATH**. 
  
Si un analyseur ne reconnaît pas la version principale d’une règle, le client doit ignorer la règle et permet de passer à la règle suivante **cbRule** . Si un analyseur ne reconnaît pas la version secondaire d’une règle, le client doit analyser uniquement les composants de la règle qu’il comprend. 
  
Lors de la persistance d’une structure **TZDEFINITION** à un flux, un analyseur doit essayer pas d’écrire les informations qu’il ne comprend pas. 
  
Le nombre maximal de règles est 1 024.
  
Notez que la structure [TZREG](tzreg.md) est conservée ici différemment que lorsqu’elles sont persistantes seul, donc le même code ne peut être utilisé pour analyser. 
  
## <a name="see-also"></a>Voir aussi

- [Constantes (Outlook des API exportées)](constants-outlook-exported-apis.md)
- [Analyser un flux de données à partir d’une propriété binaire pour lire la structure TZDEFINITION](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
- [Lire les propriétés de fuseau horaire à partir d’un rendez-vous](how-to-read-time-zone-properties-from-an-appointment.md)

