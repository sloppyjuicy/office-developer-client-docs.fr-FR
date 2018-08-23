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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 0f1495549df751c59ab84e2b16fffbaf2f4f9fa5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574719"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [MTSID](mtsid.md) , chacun d'entre eux contient un identificateur d’entrée X.400 message transport système (MTS). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macros connexes :  <br/> |[CbFLATMTSIDLIST](cbflatmtsidlist.md), [CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md) <br/> |
   
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
  
> Nombre de structures **MTSID** dans le tableau indiqué par le membre **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Nombre d’octets dans le tableau décrit par **abMTSIDs**.
    
 **abMTSIDs**
  
> Tableau d’octets qui contient une ou plusieurs structures **MTSID** . 
    
## <a name="remarks"></a>Remarques

Utilisation de la structure **FLATMTSIDLIST** messagerie X.400 correspond à l’utilisation de la structure [FLATENTRYLIST](flatentrylist.md) de messagerie MAPI. MAPI utilise des structures **FLATMTSIDLIST** pour mettre à jour les propriétés X.400 lors de la gestion du message. Fournisseurs de services utilisent des structures **FLATMTSIDLIST** lors de la gestion des messages X.400 entrants et sortants. 
  
Dans le tableau **abMTSIDs** , chaque structure **MTSID** est aligné sur une limite alignée naturellement. Octets supplémentaires sont inclus comme remplissage pour rendre l’alignement que naturel entre les deux structures **MTSID** . La première structure **MTSID** dans le tableau est toujours alignée correctement, car le décalage du membre **abMTSIDs** est 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée d’arrondi au multiple prochain de 4. Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d’une structure **MTSID** . 
  
## <a name="see-also"></a>Voir aussi



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Structures MAPI](mapi-structures.md)

