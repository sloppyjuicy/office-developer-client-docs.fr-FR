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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 68dbae7a6d2e7cc458b3b7ed71ddd06bab7fb1f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584091"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une propriété nommée. 
  
|||
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
    
Valeur définie par le client
  
> 
    
 **ulKind**
  
> Valeur décrivant le type de valeur dans le **membre Kind.** Les valeurs valides sont les suivantes : 
    
MNID_ID 
  
> Le **membre Kind** contient une valeur entière qui représente le nom de la propriété. 
    
MNID_STRING 
  
> Le **membre Kind** contient une chaîne de caractères Unicode représentant le nom de la propriété. 
    
 **Kind**
  
> Union décrivant le nom de la propriété nommée. Le nom peut être une valeur d’un chiffre, stockée dans **lID** ou une chaîne de caractères Unicode, stockée dans **lpwstrName**.
    
## <a name="remarks"></a>Remarques

La structure **MAPINAMEID** est utilisée pour décrire les propriétés nommées qui ont des identificateurs sur 0x8000. Un jeu de propriétés est une partie importante d’une propriété nommée. Par exemple, PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI. 
  
Les propriétés nommées permettent aux clients de définir des propriétés personnalisées dans un espace de noms plus grand que celui disponible dans la plage d’identificateurs de propriétés définie par MAPI. Les noms de propriété ne peuvent pas être utilisés pour obtenir des valeurs de propriété directement ; Ils doivent d’abord être mappés aux identificateurs de propriété via la méthode [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Pour des objets particuliers tels que des messages, MAPI réserve une plage d’identificateurs de propriété pour les propriétés personnalisées. Par conséquent, pour ces objets, les clients n’ont pas besoin d’utiliser les propriétés nommées et peuvent économiser la surcharge associée. 
  
Pour plus d’informations sur les propriétés nommées, voir [Propriétés nommées.](mapi-named-properties.md)
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Structures MAPI](mapi-structures.md)

