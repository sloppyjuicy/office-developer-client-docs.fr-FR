---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: Décrit un verbe MAPI pour Outlook 2013 et Outlook 2016.
ms.openlocfilehash: c89bcbb8d8b486c7ceac283e56001c8697329798
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455215"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un verbe MAPI.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiform.h  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a>Members

 **lVerb**
  
> Code représentant le verbe transmis à [IMAPIForm::D oVerb](imapiform-doverb.md). Les verbes standard sont définis dans le fichier d’en-tête Exchform.h.
    
 **szVerbname**
  
> Nom complet du verbe tel qu’il apparaît dans le menu du formulaire.
    
 **fuFlags**
  
> Indicateurs du verbe.
    
 **grfAttribs**
  
> Attributs du verbe. 
    
 **ulFlags**
  
> Indicateur indiquant le format du nom complet du verbe. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Le nom complet est au format Unicode. Si l’MAPI_UNICODE n’est pas définie, le nom complet est au format ANSI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerb** est transmise en tant que paramètre dans les méthodes suivantes : 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[CbMessageClassArray](cbmessageclassarray.md)


[Structures MAPI](mapi-structures.md)

