---
title: Lire les propriétés de fuseau horaire à partir d’un rendez-vous
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: ba1b9425-6c16-cab2-da0a-a21734118098
description: Cette rubrique présente une fonction, ReadTimeZones, qui appelle les deux fonctions, BinToTZDEFINITION et BinToTZREG, pour lire les propriétés de fuseau horaire, PidLidAppointmentTimeZoneDefinitionStartDisplay et PidLidTimeZoneStruct, à partir d’un rendez-vous.
ms.openlocfilehash: 14774f5a565926bda2bdc16e846f3eed3d2002ce
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605455"
---
# <a name="read-time-zone-properties-from-an-appointment"></a>Lire les propriétés de fuseau horaire à partir d’un rendez-vous

Cette rubrique présente une fonction, qui appelle les deux fonctions et, pour lire les propriétés de fuseau  `ReadTimeZones`  `BinToTZDEFINITION`  `BinToTZREG` horaire, [PidLidAppointmentTimeZoneDefinitionStartDisplay](https://msdn.microsoft.com/library/08239670-3211-420c-99d7-0056ed967cb8%28Office.15%29.aspx) et [PidLidTimeZoneStruct,](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx)à partir d’un rendez-vous.
  
**PidLidAppointmentTimeZoneDefinitionStartDisplay** contient un flux qui est mappant au format persistant d’une structure [TZDEFINITION,](tzdefinition.md) et **PidLidTimeZoneStruct** contient un flux qui est mappant sur le format persistant d’une structure [TZREG.](tzreg.md) Pour obtenir les structures **TZDEFINITION** et **TZREG** exactes et sont utilisées pour l’pare-rendu approprié des valeurs de flux de  `BinToTZDEFINITION` ces  `BinToTZREG` propriétés. Ces deux fonctions sont définies dans [Parse a stream from a binary property to read the TZDEFINITION structure](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md) and [Parse a stream from a binary property to read the TZREG structure](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md), respectivement. 
  
```cpp
void ReadTimeZones(LPMAPIPROP lpAppointment) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID[2] = {0}; 
    LPMAPINAMEID lpNamedID[2]; 
    lpNamedID[0] = &amp;NamedID[0]; 
    lpNamedID[1] = &amp;NamedID[1]; 
    NamedID[0].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[0].ulKind = MNID_ID; 
    NamedID[0].Kind.lID = dispidTimeZoneStruct; 
    NamedID[1].lpguid = (LPGUID)&amp;PSETID_Appointment; 
    NamedID[1].ulKind = MNID_ID; 
    NamedID[1].Kind.lID = dispidApptTZDefStartDisplay; 
    hRes = lpAppointment->GetIDsFromNames( 
        2, 
        lpNamedID, 
        NULL, 
        &amp;lpNamedPropTags); 
    if (SUCCEEDED(hRes) &amp;&amp; lpNamedPropTags) 
    { 
        SizedSPropTagArray(2,sptaTzProps) = {2, 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_BINARY), 
            CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[1],PT_BINARY), 
        }; 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
        hRes = lpAppointment->GetProps( 
            (LPSPropTagArray)&amp;sptaTzProps, 
            NULL, 
            &amp;cProps, 
            &amp;lpProps); 
        if (SUCCEEDED(hRes) &amp;&amp; 2 == cProps &amp;&amp; lpProps) 
        { 
            if (PT_BINARY == PROP_TYPE(lpProps[0].ulPropTag)) 
            { 
                TZREG* ptzReg = BinToTZREG(lpProps[0].Value.bin.cb,lpProps[0].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzReg. 
                delete ptzReg; 
            } 
            if (PT_BINARY == PROP_TYPE(lpProps[1].ulPropTag)) 
            { 
                TZDEFINITION* ptzDef = BinToTZDEFINITION(lpProps[1].Value.bin.cb,lpProps[1].Value.bin.lpb); 
                // TODO: Do whatever is necessary with ptzDef. 
                delete[] ptzDef; 
            } 
           } 
        MAPIFreeBuffer(lpProps); 
    } 
    MAPIFreeBuffer(lpNamedPropTags); 
}
```

## <a name="see-also"></a>Voir aussi

- [À propos de la relocalisation des calendriers par programme à l'heure](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)

