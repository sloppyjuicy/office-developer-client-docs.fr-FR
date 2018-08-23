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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: f95c86a137e7253f3445123c23f2dc0d76b6d87a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567390"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Décrémente le décompte de références, nettoie et supprime par instance globale des données pour la DLL MAPI. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIX.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Paramètres

Aucune 
  
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

Une application cliente appelle la fonction **MAPIUninitialize** pour mettre fin à son interaction avec l’interface MAPI, commencé avec un appel à la fonction [exécuter MAPIInitialize](mapiinitialize.md) . Après avoir appelé **MAPIUninitialize** , aucun autre appel MAPI ne peut être effectuées par le client. 
  
 **MAPIUninitialize** décrémente le nombre et la fonction **exécuter MAPIInitialize** correspondante incrémente le décompte de références. Par conséquent, le nombre d’appels à une fonction doit correspondre au nombre d’appels à l’autre. 
  
> [!NOTE]
> Impossible d’appeler **exécuter MAPIInitialize** ou **MAPIUninitialize** au sein d’une fonction Win32 **DllMain** ou toute autre fonction qui crée ou met fin à des threads. Pour plus d’informations, voir [Utilisation des objets Thread-Safe](using-thread-safe-objects.md). 
  

