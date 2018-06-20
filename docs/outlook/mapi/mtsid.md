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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e42bbf23ea8cf4e6196017a962329366e168420d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784911"
---
# <a name="mtsid"></a>MTSID

  
  
**S’applique à**: Outlook 
  
Contient un identificateur d’entrée X.400 message transport système (MTS). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbMTSID](cbmtsid.md), [CbNewMTSID](cbnewmtsid.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cb;
  BYTE abEntry[MAPI_DIM];
} MTSID, FAR *LPMTSID;

```

## <a name="members"></a>Membres

 **cb**
  
> Nombre d’octets dans le tableau indiqué par le membre **abEntry** . 
    
 **abEntry**
  
> Tableau d’octets qui contient les données d’identificateur MTS entrée.
    
## <a name="remarks"></a>Remarques

La structure **MTSID** est utilisée uniquement pour les mappages X.400 d’identificateurs d’entrée MAPI. Il correspond à la structure MAPI [FLATENTRY](flatentry.md) . 
  
Un identificateur MTS a le même format qu’un identificateur d’entrée MAPI ou une valeur de propriété binaire. Les identificateurs MTS peuvent être particulièrement utiles pour l’annulation de messages différés. 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Structures MAPI](mapi-structures.md)

