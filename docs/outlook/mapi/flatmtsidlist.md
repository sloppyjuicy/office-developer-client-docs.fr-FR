---
title: FLATMTSIDLIST
description: Décrit FLATMTSIDLIST et fournit une syntaxe, des membres et des remarques supplémentaires.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FLATMTSIDLIST
api_type:
- COM
ms.assetid: b66c2815-72bc-4535-b34c-899bb830f29e
ms.openlocfilehash: 2c75189b7e2c773b6a4cbfd933e66b9f0a8da8d5
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816450"
---
# <a name="flatmtsidlist"></a>FLATMTSIDLIST

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un tableau de structures [MTSID](mtsid.md) , chacune contenant un identificateur d’entrée du système de transport de messages (MTS) X.400. 
  
|Propriété|Valeur|
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
  
> Nombre de structures **MTSID** dans le tableau décrit par le membre **abMTSIDs** . 
    
 **cbMTSIDs**
  
> Nombre d’octets dans le tableau décrit par **les abMTSID**.
    
 **abMTSIDs**
  
> Tableau d’octets qui contient une ou plusieurs structures **MTSID** . 
    
## <a name="remarks"></a>Remarques

L’utilisation de la structure **FLATMTSIDLIST** dans la messagerie X.400 correspond à l’utilisation de la structure [FLATENTRYLIST](flatentrylist.md) dans la messagerie MAPI. MAPI utilise des structures **FLATMTSIDLIST** pour gérer les propriétés X.400 pendant la gestion des messages. Les fournisseurs de services utilisent des structures **FLATMTSIDLIST** lors de la gestion des messages X.400 entrants et sortants. 
  
Dans le tableau **abMTSIDs** , chaque structure **MTSID** est alignée sur une limite alignée naturellement. Des octets supplémentaires sont inclus comme remplissage pour garantir un alignement naturel entre deux structures **MTSID** . La première structure **MTSID** du tableau est toujours alignée correctement, car le décalage du membre **abMTSIDs** est 8. Pour calculer le décalage de la structure suivante, utilisez la taille de la première entrée arrondie au multiple suivant de 4. Utilisez la macro [CbNewMTSID](cbnewmtsid.md) pour calculer la taille d’une structure **MTSID** . 
  
## <a name="see-also"></a>Voir aussi



[CbNewFLATMTSIDLIST](cbnewflatmtsidlist.md)
  
[FLATENTRYLIST](flatentrylist.md)
  
[MTSID](mtsid.md)


[Structures MAPI](mapi-structures.md)

