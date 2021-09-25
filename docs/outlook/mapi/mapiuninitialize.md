---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e06dfe806ca3d99f35a369eb4a7cf6fe8da50717
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551127"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrémente le nombre de références, nettoie et supprime les données globales par instance pour la DLL MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Paramètres

Aucun 
  
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une application cliente appelle la **fonction MAPIUninitialize** pour mettre fin à son interaction avec MAPI, commencée par un appel à la fonction [MAPIInitialize.](mapiinitialize.md) Une **fois MAPIUninitialize** appelé, aucun autre appel MAPI ne peut être effectué par le client. 
  
 **MAPIUninitialize** décrémente le nombre de références et la fonction **MAPIInitialize** correspondante incrémente le nombre de références. Par conséquent, le nombre d’appels à une fonction doit être égal au nombre d’appels à l’autre. 
  
> [!NOTE]
> Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d’une fonction **Win32 DllMain** ou toute autre fonction qui crée ou termine des threads. Pour plus d’informations, [voir Using Thread-Safe Objects](using-thread-safe-objects.md). 
  

