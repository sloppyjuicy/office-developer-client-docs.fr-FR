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
description: 'Libère les fonctions utilitaires appelées explicitement par la fonction ScInitMapiUtil ou implicitement par la fonction MAPIInitialize. '
ms.openlocfilehash: 99dc2c80d348f56117ffb5bb15d8afc19dcf60ec
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764341"
---
# <a name="deinitmapiutil"></a>DeinitMapiUtil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Libère les fonctions utilitaires appelées explicitement par la [fonction ScInitMapiUtil](scinitmapiutil.md) ou implicitement par la [fonction MAPIInitialize](mapiinitialize.md) . 
  
|Propriété |Valeur |
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

Aucune 
  
## <a name="remarks"></a>Remarques

Fonctions **de publication de la fonction DeinitMapiUtil** initialisées avec [ScInitMapiUtil](scinitmapiutil.md) ou [MAPIInitialize](mapiinitialize.md). 
  
Lorsque l’utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour les libérer. En revanche, [MAPIUninitialize](mapiuninitialize.md) appelle implicitement **DeinitMapiUtil**. 
  

