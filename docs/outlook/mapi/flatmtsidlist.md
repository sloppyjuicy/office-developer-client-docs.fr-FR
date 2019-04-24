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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: bd9bfe4d1411b84a7811235aa68728afaefe64ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327306"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [MTSID](mtsid.md) , chacune contenant un identificateur d'entrée MTS (message transport System) X. 400. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Macros connexes:  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
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
  
> Nombre de structures **MTSID** dans le tableau décrit par le membre **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Nombre d'octets dans le tableau décrit par **abMTSIDs**.
    
 **abMTSIDs**
  
> Tableau d'octets qui contient une ou plusieurs structures **MTSID** . 
    
## <a name="remarks"></a>Remarques

L'utilisation de la structure **FLATMTSIDLIST** dans la messagerie X. 400 correspond à l'utilisation de la structure [FLATENTRYLIST](flatentrylist.md) dans la messagerie MAPI. MAPI utilise des structures **FLATMTSIDLIST** pour conserver les propriétés X. 400 lors de la gestion des messages. Les fournisseurs de services utilisent les structures **FLATMTSIDLIST** lors de la gestion des messages entrants et sortants X. 400. 
  
Dans le tableau **abMTSIDs** , chaque structure **MTSID** est alignée sur une frontière naturellement alignée. Les octets supplémentaires sont inclus comme remplissage afin de s'assurer de l'alignement naturel entre deux structures **MTSID** . La première structure **MTSID** dans le tableau est toujours alignée correctement car l'offset du membre **abMTSIDs** est égal à 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4. Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d'une structure **MTSID** . 
  
## <a name="see-also"></a>Voir aussi



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Structures MAPI](mapi-structures.md)

