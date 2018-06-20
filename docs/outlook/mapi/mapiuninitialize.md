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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784792"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**S’applique à**: Outlook 
  
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
  

