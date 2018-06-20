---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782580"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Obtient le nombre spécifié suivant de blocs de données et de disponibilité dans une énumération.
  
## <a name="quick-info"></a>Informations rapides

Voir [IEnumFBBlock](ienumfbblock.md).
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a>Paramètres

_celt_
  
> [in] Le nombre de données et de disponibilité se bloque dans *pblk* à récupérer. 
    
_PBLK_
  
> [in] Pointeur vers un tableau de blocs et de disponibilité. Le tableau est alloué à une taille de *celt* . Les blocs de disponibilité requis sont retournés dans ce tableau. 
    
_pcfetch_
  
> [out] Le nombre de blocs de disponibilité retournés dans *pblk* . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Le nombre de blocs demandé a été renvoyé.  <br/> |
|S_FALSE  <br/> |Le nombre de blocs demandé n’a pas été retourné.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (disponibilité API)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

