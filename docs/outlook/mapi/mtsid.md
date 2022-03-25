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
ms.openlocfilehash: a5e1b7943fed017741c8d460c90e4759cb48de8d
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63782067"
---
# <a name="mtsid"></a>MTSID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un identificateur d’entrée MTS (Message Transport System) X.400. 
  
|Propriété|Valeur|
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
  
> Nombre d’octets dans le tableau décrit par le **membre abEntry** . 
    
 **abEntry**
  
> Tableau d’bytes qui contient les données d’identificateur d’entrée MTS.
    
## <a name="remarks"></a>Remarques

La structure **MTSID** est utilisée uniquement pour les mappages X.400 des identificateurs d’entrée MAPI. Il correspond à la structure [MAPI FLATENTRY](flatentry.md) . 
  
Un identificateur MTS a le même format qu’un identificateur d’entrée MAPI ou une valeur de propriété binaire. Les identificateurs MTS peuvent être particulièrement utiles pour annuler les messages différés. 
  
## <a name="see-also"></a>Voir aussi



[FLATENTRY](flatentry.md)
  
[FLATMTSIDLIST](flatmtsidlist.md)


[Structures MAPI](mapi-structures.md)

