---
title: IContabAdminRemoveStore
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IContabAdmin.RemoveStore
api_type:
- COM
ms.assetid: 2a5fcf5c-8a5a-4774-b8c9-1ac1ff27947d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: f92e562196f551bc6dca7be9f3fd5093d5f4cc03
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592444"
---
# <a name="icontabadminremovestore"></a>IContabAdmin::RemoveStore

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime le carnet d’adresses de contact spécifié par l’ID d’entrée donné de la hiérarchie du carnet d’adresses.
  
```cpp
HRESULT RemoveStore(
ULONG cbEntryID, 
LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.
    

