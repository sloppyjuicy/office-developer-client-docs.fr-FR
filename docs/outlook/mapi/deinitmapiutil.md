---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e84dbc0976f5c438a7e0b5fd7cddcbf1c0659f40
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574796"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fonctions utilitaire appelées explicitement par la fonction [ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la fonction [exécuter MAPIInitialize](mapiinitialize.md) le relâche. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Paramètres

Aucune 
  
## <a name="return-value"></a>Valeur renvoy�e

Aucune 
  
## <a name="remarks"></a>Remarques

La fonction **DeinitMapiUtil** release fonctions initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [exécuter MAPIInitialize](mapiinitialize.md). 
  
Lors de l’utilisation des fonctions appelée par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour libérer les. En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**. 
  

