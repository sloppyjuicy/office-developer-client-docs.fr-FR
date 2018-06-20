---
title: FLAGLIST
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FLAGLIST
api_type:
- COM
ms.assetid: b4c0655c-1a3a-4f89-a977-0431db596512
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2cf5ff69e8453b2da26fd5044823ddf4f99a9f45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783320"
---
# <a name="flaglist"></a>FLAGLIST

  
  
**S’applique à**: Outlook 
  
Contient une liste d’indicateurs utilisés pour indiquer l’état d’entrées d’adresse au cours du processus de résolution de nom.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct
{
  ULONG cFlags;
  ULONG ulFlags[MAPI_DIM];
} FlagList, FAR * LPFlagList;

```

## <a name="members"></a>Membres

 **cFlags**
  
> Nombre d’indicateurs MAPI dans la liste.
    
 **ulFlags**
  
> Tableau des indicateurs qui fournit l’état de l’opération de résolution de nom d’un destinataire. Les indicateurs suivants peuvent être définis :
    
MAPI_AMBIGUOUS 
  
> Le destinataire a été résolu, mais pas à un identificateur d’entrée unique. Autres conteneurs de carnet d’adresses ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_RESOLVED 
  
> Le destinataire a été résolu en un identificateur d’entrée unique. Autres conteneurs de carnet d’adresses ne doivent pas essayer de résoudre ce destinataire. 
    
MAPI_UNRESOLVED 
  
> L’entrée n’a pas été résolue. Autres conteneurs de carnet d’adresses doivent essayer de résoudre ce destinataire.
    
## <a name="remarks"></a>Remarques

La structure **FLAGLIST** est utilisée comme paramètre pour [IABContainer::ResolveNames](iabcontainer-resolvenames.md). Chacun des destinataires à résoudre est inclus dans une structure [ADRLIST](adrlist.md) . Comme le conteneur de carnet d’adresses essaie de résoudre chaque destinataire, il définit l’indicateur approprié dans l’entrée correspondante dans la structure **FLAGLIST** . Toutes les entrées de la structure **FLAGLIST** sont dans le même ordre que les entrées de la structure **ADRLIST** . Cela facilite associer un paramètre d’indicateur à un destinataire. 
  
## <a name="see-also"></a>Voir aussi



[ADRLIST](adrlist.md)
  
[IABContainer::ResolveNames](iabcontainer-resolvenames.md)


[Structures MAPI](mapi-structures.md)

