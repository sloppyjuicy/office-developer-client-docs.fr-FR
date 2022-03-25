---
title: MAPINAMEID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.MAPINAMEID
api_type:
- COM
ms.assetid: 9a92e9cd-8282-4cf0-93af-4089b3763594
description: Décrit une propriété nommée. Les propriétés nommées permettent aux clients de définir des propriétés personnalisées dans un espace de noms plus grand que la plage d’identificateurs de propriétés définie par MAPI.
ms.openlocfilehash: 8e7c7a7ad9a78aae32c827c5d3747df1e5736e33
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405537"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété nommée. 
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
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
  
> Pointeur vers une structure [GUID](guid.md) définissant un jeu de propriétés particulier ; ce membre ne peut pas être NULL. Les valeurs valides sont les suivantes : 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Une valeur définie par le client
  
> 
    
 **ulKind**
  
> Valeur décrivant le type de valeur dans le **membre Kind** . Les valeurs valides sont les suivantes : 
    
MNID_ID 
  
> Le **membre Kind** contient une valeur entière qui représente le nom de la propriété. 
    
MNID_STRING 
  
> Le **membre Kind** contient une chaîne de caractères Unicode représentant le nom de la propriété. 
    
 **Kind**
  
> Union décrivant le nom de la propriété nommée. Il peut s’agit d’une valeur d’un ensemble, stockée dans **lID** ou d’une chaîne de caractères Unicode, stockée dans **lpwstrName**.
    
## <a name="remarks"></a>Remarques

La structure **MAPINAMEID** est utilisée pour décrire les propriétés nommées qui ont des identificateurs sur 0x8000. Un jeu de propriétés est une partie importante d’une propriété nommée. Par exemple, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI. 
  
Les propriétés nommées permettent aux clients de définir des propriétés personnalisées dans un espace de noms plus grand que celui disponible dans la plage d’identificateurs de propriétés définie par MAPI. Les noms de propriété ne peuvent pas être utilisés pour obtenir des valeurs de propriété directement ; Ils doivent d’abord être mappés aux identificateurs de propriété via la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Pour des objets particuliers tels que des messages, MAPI réserve une plage d’identificateurs de propriété pour les propriétés personnalisées. Par conséquent, pour ces objets, les clients n’ont pas besoin d’utiliser les propriétés nommées et peuvent économiser la surcharge associée. 
  
Pour plus d’informations sur les propriétés nommées, voir [Propriétés nommées](mapi-named-properties.md).
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Structures MAPI](mapi-structures.md)

