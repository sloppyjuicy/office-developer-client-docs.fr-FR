---
title: FLATMTSIDLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439218"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [MTSID,](mtsid.md) chacune contenant un identificateur d’entrée de système de transport de messages (MTS) X.400. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros associées :  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cMTSIDs;
  ULONG cbMTSIDs;
  BYTE abMTSIDs[MAPI_DIM];
} FLATMTSIDLIST, FAR *LPFLATMTSIDLIST;

```

## <a name="members"></a>Members

 **cMTSIDs**
  
> Nombre de structures **MTSID** dans le tableau décrit par le membre **abMTSIDs.** 
    
 **cbMTSIDs**
  
> Nombre d’octets dans le tableau décrit par **abMTSIDs**.
    
 **abMTSIDs**
  
> Tableau d’bytes qui contient une ou plusieurs structures **MTSID.** 
    
## <a name="remarks"></a>Remarques

L’utilisation de la structure **FLATMTSIDLIST** dans la messagerie X.400 correspond à l’utilisation de la structure [FLATENTRYLIST](flatentrylist.md) dans la messagerie MAPI. MAPI utilise des structures **FLATMTSIDLIST** pour gérer les propriétés X.400 lors de la gestion des messages. Les fournisseurs de services utilisent des structures **FLATMTSIDLIST** lors de la gestion des messages X.400 entrants et sortants. 
  
Dans le **tableau abMTSIDs,** chaque structure **MTSID** est alignée sur une limite alignée naturellement. Des octets supplémentaires sont inclus comme remplissage pour assurer un alignement naturel entre deux structures **MTSID.** La première structure **MTSID** du tableau est toujours alignée correctement, car le décalage du membre **abMTSIDs** est 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4. Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d’une structure **MTSID.** 
  
## <a name="see-also"></a>Voir aussi



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Structures MAPI](mapi-structures.md)

