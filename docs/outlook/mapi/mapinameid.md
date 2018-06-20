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
ms.openlocfilehash: c3a21e8a6e69cae9d8b757a60fe56d63e079b3ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784744"
---
# <a name="mapinameid"></a>MAPINAMEID

  
  
**S’applique à**: Outlook 
  
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

## <a name="members"></a>Membres

 **lpguid**
  
> Pointeur vers une structure [GUID](guid.md) de définition d’une propriété spécifique défini ; Ce membre ne peut pas être NULL. Les valeurs valides sont les suivantes : 
    
PS_PUBLIC_STRINGS
  
> 
    
PS_MAPI
  
> 
    
Une valeur définie par le client
  
> 
    
 **ulKind**
  
> Valeur décrivant le type de valeur dans le membre de **type** . Les valeurs valides sont les suivantes : 
    
MNID_ID 
  
> Le **type** de membre contient une valeur entière qui représente le nom de propriété. 
    
MNID_STRING 
  
> Le **type** de membre contient une chaîne de caractères Unicode qui représente le nom de propriété. 
    
 **Kind**
  
> Union décrivant le nom de la propriété nommée. Le nom peut être une valeur entière, stockés dans le **capot**, soit une chaîne de caractères Unicode, stockés dans **lpwstrName**.
    
## <a name="remarks"></a>Remarques

La structure **MAPINAMEID** est utilisée pour décrire les propriétés nommés qui ont des identificateurs sur 0 x 8000. Un jeu de propriétés constitue une part importante une propriété nommée. Par exemple PS_PUBLIC_STRINGS ou PS_ROUTING_ADDRTYPE sont des jeux de propriétés définis par MAPI. 
  
Propriétés nommées permettent aux clients permet de définir des propriétés personnalisées dans un espace de noms plus grand que ce qui est disponible dans la plage d’identificateurs MAPI défini par la propriété. Les noms de propriété ne peut être utilisés pour obtenir des valeurs de propriété directement. ils doivent être tout d’abord mappées aux identificateurs de propriété par le biais de la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Pour des objets spécifiques tels que les messages, MAPI réserve une plage d’identificateurs de propriété pour les propriétés personnalisées. Par conséquent, pour ces objets, les clients et n’est pas à utiliser les propriétés nommées peuvent enregistrer les frais généraux. 
  
Pour plus d’informations sur les propriétés nommées, voir [Propriétés nommées](mapi-named-properties.md).
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)


[Structures MAPI](mapi-structures.md)

