---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787222"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**S’applique à**: Outlook 
  
Décrit un verbe MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
   
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

## <a name="members"></a>Membres

 **lVerb**
  
> Code représentant le verbe qui est transmis à [IMAPIForm::DoVerb](imapiform-doverb.md). Les verbes standard sont définies dans le fichier d’en-tête Exchform.h.
    
 **szVerbname**
  
> Nom complet du verbe telle qu’elle apparaît dans le menu formulaire.
    
 **fuFlags**
  
> Indicateurs pour le verbe.
    
 **grfAttribs**
  
> Attributs du verbe. 
    
 **ulFlags**
  
> Indicateur indiquant le format du nom d’affichage du verbe. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Le nom complet est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, le nom complet est au format ANSI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerb** est transmise en tant que paramètre dans les méthodes suivantes : 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[CbMessageClassArray](cbmessageclassarray.md)


[Structures MAPI](mapi-structures.md)

