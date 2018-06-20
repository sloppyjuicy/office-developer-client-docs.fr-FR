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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783128"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**S’applique à**: Outlook 
  
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
  

