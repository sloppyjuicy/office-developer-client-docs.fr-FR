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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427345"
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
  

