---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: Obtient le nombre spécifié suivant de blocs de données de libre/occupé dans une éumération.
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422137"
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
  
> [in] Nombre de blocs de données de libre/occupé dans  *pblk*  à récupérer. 
    
_pblk_
  
> [in] Pointeur vers un tableau de blocs de libre/occupé. Une taille delt est allouée *au tableau.* Les blocs de libre/occupé demandés sont renvoyés dans ce tableau. 
    
_pcfetch_
  
> [out] Nombre de blocs de libre/occupé réellement renvoyés dans  *pblk*  . 
    
## <a name="return-values"></a>Valeurs de retour

|**[HRESULT]**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Le nombre demandé de blocs a été renvoyé.  <br/> |
|S_FALSE  <br/> |Le nombre demandé de blocs n’a pas été renvoyé.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [Constantes (API de libre/occupé)](constants-free-busy-api.md)  
- [FBBlock_1](fbblock_1.md)  
- [IEnumFBBlock::Clone](ienumfbblock-clone.md)  
- [IEnumFBBlock::Reset](ienumfbblock-reset.md)  
- [IEnumFBBlock::Restrict](ienumfbblock-restrict.md)  
- [IEnumFBBlock::Skip](ienumfbblock-skip.md)

