---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 70d6365ed2f1b38da7759c4d872c25358dc927d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556811"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère les fonctions utilitaires appelées explicitement par la [fonction ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la fonction [MAPIInitialize.](mapiinitialize.md) 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a>Paramètres

Aucun 
  
## <a name="return-value"></a>Valeur renvoyée

Aucun 
  
## <a name="remarks"></a>Remarques

Fonctions de publication de la fonction **DeinitMapiUtil** initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md). 
  
Lorsque l’utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour les libérer. En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**. 
  

