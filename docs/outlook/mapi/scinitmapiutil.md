---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420590"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Remplace [MAPIInitialize](mapiinitialize.md) lorsque seules les fonctions utilitaires Select sont utilisées. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
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

Les fonctions **ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) coopèrent pour appeler et libérer des fonctions utilitaires Select, par opposition à [MAPIInitialize](mapiinitialize.md), qui appelle Core ainsi que des fonctions utilitaires. Lorsque **ScInitMapiUtil** appelle les fonctions utilitaires, il initialise également la mémoire nécessaire. 
  
Lorsque l'utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être appelé explicitement pour les libérer. En revanche, **MAPIInitialize** appelle implicitement **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUninitialize](mapiuninitialize.md)

