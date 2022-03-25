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
description: Décrémente le nombre de références, nettoie et supprime les données globales par instance pour la DLL MAPI.
ms.openlocfilehash: 12255dfee1537dc9ef9beb8846393d91ab53d24b
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763956"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrémente le nombre de références, nettoie et supprime les données globales par instance pour la DLL MAPI. 
  
|Propriété |Valeur |
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

Une application cliente appelle la **fonction MAPIUninitialize** pour mettre fin à son interaction avec MAPI, commencée par un appel à la fonction [MAPIInitialize](mapiinitialize.md) . Une **fois MAPIUninitialize** appelé, aucun autre appel MAPI ne peut être effectué par le client. 
  
 **MAPIUninitialize** décrémente le nombre de références et la fonction **MAPIInitialize** correspondante incrémente le nombre de références. Par conséquent, le nombre d’appels à une fonction doit être égal au nombre d’appels à l’autre. 
  
> [!NOTE]
> Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d’une fonction **Win32 DllMain** ou toute autre fonction qui crée ou termine des threads. Pour plus d’informations, [voir Using Thread-Safe Objects](using-thread-safe-objects.md). 
  

