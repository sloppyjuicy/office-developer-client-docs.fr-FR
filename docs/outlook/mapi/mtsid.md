---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84ffea2a1c5f0cb70cdd49f5aa318921f8a3d044
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595643"
---
# <a name="mtsid"></a>MTSID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée MTS (Message Transport System) X.400. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d’octets dans le tableau décrit par le **membre abEntry.** 
    
 **abEntry**
  
> Tableau d’bytes qui contient les données d’identificateur d’entrée MTS.
    
## <a name="remarks"></a>Remarques

La structure **MTSID** est utilisée uniquement pour les mappages X.400 des identificateurs d’entrée MAPI. Il correspond à la structure [MAPI FLATENTRY.](flatentry.md) 
  
Un identificateur MTS a le même format qu’un identificateur d’entrée MAPI ou une valeur de propriété binaire. Les identificateurs MTS peuvent être particulièrement utiles pour annuler les messages différés. 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Structures MAPI](mapi-structures.md)

