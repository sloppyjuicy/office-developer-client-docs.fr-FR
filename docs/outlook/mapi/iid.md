---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
ms.openlocfilehash: afe90bf23e0b87ecb924a6f6b68cd7dc9d88a8b7
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375663"
---
# <a name="iid"></a>IID

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrit une structure [GUID](guid.md) utilisée pour décrire un identificateur pour une interface MAPI. 
  
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a>Members

Voir la structure **guid** . 
  
## <a name="remarks"></a>Remarques

Une **structure IID** permet d’identifier de manière unique une interface MAPI et d’associer une interface particulière à un objet. Par exemple, lorsqu’un client appelle [IMAPISession::OpenEntry](imapisession-openentry.md) pour ouvrir un dossier, le client définit le paramètre  _lpInterface_ pour qu’il pointe vers un **IID** représentant l’interface [IMAPIFolder](imapifolderimapicontainer.md) . MAPI définit **L’IMAPIFolderIID** à IID_IMAPIFolder. **Les structures IID** sont également utilisées pour identifier de manière unique les interfaces OLE. 
  
Toutes les structures **IID** spécifiques pour les interfaces MAPI sont définies dans le fichier d’en-tête Mapiguid.h. 
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)


[Structures MAPI](mapi-structures.md)

