---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: baec750a460b3ba9becd2e1dddf967705424ac4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357189"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété nommée. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _MAPINAMEID
{
  LPGUID lpguid;
  ULONG ulKind;
  union
  {
    LONG lID;
    LPWSTR lpwstrName;
  } Kind;
} MAPINAMEID, FAR *LPMAPINAMEID;

```

## <a name="members"></a>Members

 **lpguid**
  
> Pointeur vers une structure de [GUID](guid.md) définissant un jeu de propriétés particulier; ce membre ne peut pas être NULL. Les valeurs valides sont les suivantes : 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Valeur définie par le client
  
> 
    
 **ulKind**
  
> Valeur décrivant le type de valeur dans le membre **Kind** . Les valeurs valides sont les suivantes : 
    
MNID_ID 
  
> Le membre **Kind** contient une valeur entière qui représente le nom de la propriété. 
    
MNID_STRING 
  
> Le membre **Kind** contient une chaîne de caractères Unicode représentant le nom de la propriété. 
    
 **Kind**
  
> Union décrivant le nom de la propriété nommée. Le nom peut être soit une valeur entière, stockée sur un **couvercle**, soit une chaîne de caractères Unicode, stockée dans **lpwstrName**.
    
## <a name="remarks"></a>Remarques

La structure **MAPINAMEID** est utilisée pour décrire les propriétés de propriétés nommées qui comportent des identificateurs sur 0x8000. Un jeu de propriétés est une partie importante d'une propriété nommée. Par exemple PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI. 
  
Les propriétés nommées permettent aux clients de définir des propriétés personnalisées dans un espace de noms plus grand que ce qui est disponible dans la plage d'identificateurs de propriété définie par MAPI. Les noms de propriétés ne peuvent pas être utilisés pour obtenir directement des valeurs de propriété; elles doivent d'abord être mappées aux identificateurs de propriétés via la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Pour des objets particuliers comme les messages, MAPI se réserve une plage d'identificateurs de propriétés pour les propriétés personnalisées. Par conséquent, pour ces objets, les clients n'ont pas besoin d'utiliser les propriétés nommées et peuvent enregistrer la charge de travail associée. 
  
Pour plus d'informations sur les propriétés nommées, voir [named Properties](mapi-named-properties.md).
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Structures MAPI](mapi-structures.md)

