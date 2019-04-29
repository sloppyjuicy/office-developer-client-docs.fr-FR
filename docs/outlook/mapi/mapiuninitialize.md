---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408522"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Décrémente le décompte de références, nettoie et supprime les données globales par instance pour la DLL MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapix. h  <br/> |
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

Une application cliente appelle la fonction **MAPIUninitialize** pour mettre fin à son interaction avec MAPI, commencée par un appel à la fonction [MAPIInitialize](mapiinitialize.md) . Après l'appel de **MAPIUninitialize** , aucun autre appel MAPI ne peut être effectué par le client. 
  
 **MAPIUninitialize** décrémente le décompte de références, et la fonction **MAPIInitialize** correspondante incrémente le nombre de références. Par conséquent, le nombre d'appels à une fonction doit être égal au nombre d'appels à l'autre. 
  
> [!NOTE]
> Vous ne pouvez pas appeler **MAPIInitialize** ou **MAPIUninitialize** à partir d'une fonction **DllMain** Win32 ou de toute autre fonction qui crée ou termine des threads. Pour plus d'informations, consultez la rubrique [utilisation d'objets thread-safe](using-thread-safe-objects.md). 
  

