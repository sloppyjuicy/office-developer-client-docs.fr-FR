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
description: Remplace MAPIInitialize lorsque seules certaines fonctions utilitaires sont utilisées pour Outlook 2013 ou Outlook 2016.
ms.openlocfilehash: 5396032e1ee1070f0ef57c46ad83f31ab76e0221
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455257"
---
# <a name="scinitmapiutil"></a>ScInitMapiUtil

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Remplace [MAPIInitialize lorsque](mapiinitialize.md) seules certaines fonctions utilitaires sont utilisées. 
  
|Propriété |Valeur |
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

Les **fonctions ScInitMapiUtil** et [DeinitMapiUtil](deinitmapiutil.md) collaborent pour appeler et libérer des fonctions utilitaires sélectionnées, par opposition à [MAPIInitialize](mapiinitialize.md), qui appelle core ainsi que des fonctions utilitaires. Lorsque **ScInitMapiUtil** appelle des fonctions utilitaires, il initialise également la mémoire nécessaire. 
  
Lorsque l’utilisation des fonctions appelées par **ScInitMapiUtil** est terminée, **DeinitMapiUtil** doit être explicitement appelée pour les libérer. En revanche, **MAPIInitialize** appelle implicitement **DeinitMapiUtil**. 
  
## <a name="see-also"></a>Voir aussi



[MAPIUninitialize](mapiuninitialize.md)

