---
title: IID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IID
api_type:
- COM
ms.assetid: fa5498ab-2f8a-42f8-ba9d-1d555768594f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5605de7dbcc18197748713bcf909839690d7259f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336350"
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

Voir la structure du **GUID** . 
  
## <a name="remarks"></a>Remarques

Une structure d' **IID** est utilisée pour identifier une interface MAPI de manière unique et associer une interface particulière à un objet. Par exemple, lorsqu'un client appelle [IMAPISession:: OpenEntry](imapisession-openentry.md) pour ouvrir un dossier, le client définit le paramètre _lpInterface_ de sorte qu'il pointe vers un **IID** représentant l'interface [IMAPIFolder](imapifolderimapicontainer.md) . MAPI définit le **IMAPIFolderIID** à IID_IMAPIFolder. Les structures **IID** sont également utilisées pour identifier les interfaces OLE de manière unique. 
  
Toutes les structures d' **IID** spécifiques pour les interfaces MAPI sont définies dans le fichier d'en-tête Mapiguid. h. 
  
## <a name="see-also"></a>Voir aussi



[GUID](guid.md)


[Structures MAPI](mapi-structures.md)

