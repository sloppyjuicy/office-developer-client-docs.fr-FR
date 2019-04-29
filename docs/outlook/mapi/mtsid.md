---
title: MTSID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MTSID
api_type:
- COM
ms.assetid: 3d9bc643-332f-4c8e-83e6-ce9b15711945
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 96da91acec741322e6c07c64555171d35f0f7e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435172"
---
# <a name="mtsid"></a>MTSID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d'entrée de système de transport de messages (MTS) X. 400. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Members

 **cb**
  
> Nombre d'octets dans le tableau décrit par le membre **abEntry** . 
    
 **abEntry**
  
> Tableau d'octets qui contient les données de l'identificateur de l'entrée MTS.
    
## <a name="remarks"></a>Remarques

La structure **MTSID** est utilisée uniquement pour les mappages X. 400 des identificateurs d'entrée MAPI. Elle correspond à la structure [FLATENTRY](flatentry.md) MAPI. 
  
Un identificateur MTS a le même format qu'un identificateur d'entrée MAPI ou une valeur de propriété binaire. Les identificateurs MTS peuvent être particulièrement utiles pour annuler les messages différés. 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Structures MAPI](mapi-structures.md)

