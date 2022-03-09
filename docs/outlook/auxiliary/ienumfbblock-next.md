---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération.
ms.openlocfilehash: 7a5ff3fc06d4fa336d8a96b2afa96ead156f2cb1
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380283"
---
# <a name="ienumfbblocknext"></a>IEnumFBBlock::Next

Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération.
  
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
  
> [in] Nombre de blocs de données de libre/occupé dans *pblk*  à récupérer.

_pblk_
  
> [in] Pointeur vers un tableau de blocs de libre/occupé. Une taille delt est allouée au *tableau*. Les blocs de libre/occupé demandés sont renvoyés dans ce tableau.

_pcfetch_
  
> [out] Nombre de blocs de libre/occupé réellement renvoyés dans *pblk*.

## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Le nombre demandé de blocs a été renvoyé. |
|S_FALSE  <br/> |Le nombre demandé de blocs n’a pas été renvoyé. |

## <a name="see-also"></a>Voir aussi

- [Constantes (API de libre/occupé)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)
