---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6dbc027dfc3dfb2a0b4cf3a0096c5d33e5b4d4a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59591212"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Remplace [MAPIInitialize lorsque](mapiinitialize.md) seules certaines fonctions utilitaires sont utilisées. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) collaborent pour appeler et libérer des fonctions utilitaires de sélection, par opposition à [MAPIInitialize](mapiinitialize.md), qui appelle core ainsi que des fonctions utilitaires. Lorsque **ScInitMapiUtil** appelle des fonctions utilitaires, il initialise également la mémoire nécessaire. 
  
Lorsque l’utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour les libérer. En revanche, **MAPIInitialize** appelle implicitement **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUninitialize](mapiuninitialize.md)

