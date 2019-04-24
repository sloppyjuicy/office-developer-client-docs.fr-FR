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
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309484"
---
# <a name="smapiverb"></a>SMAPIVerb

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit un verbe MAPI.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm. h  <br/> |
   
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
  
> Code représentant le verbe passé à [IMAPIForm::D overb](imapiform-doverb.md). Les verbes standard sont définis dans le fichier d'en-tête Exchform. h.
    
 **szVerbname**
  
> Nom complet du verbe tel qu'il apparaît dans le menu formulaire.
    
 **fuFlags**
  
> Indicateurs pour le verbe.
    
 **grfAttribs**
  
> Attributs du verbe. 
    
 **ulFlags**
  
> Indicateur qui indique le format du nom d'affichage du verbe. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Le nom complet est au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, le nom d'affichage est au format ANSI.
    
## <a name="remarks"></a>Remarques

La structure **SMAPIVerb** est transmise en tant que paramètre dans les méthodes suivantes: 
  
- [IMAPIFormContainer::ResolveMultipleMessageClasses](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [IMAPIFormMgr::ResolveMultipleMessageClasses](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a>Voir aussi



[CbMessageClassArray](cbmessageclassarray.md)


[Structures MAPI](mapi-structures.md)

