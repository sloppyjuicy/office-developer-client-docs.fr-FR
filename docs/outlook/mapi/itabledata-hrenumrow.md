---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418371"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait une ligne en fonction de sa position dans le tableau. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Paramètres

 _ulRowNumber_
  
> [in] Numéro de la ligne pour laquelle renvoyer les propriétés. La valeur dans le paramètre  _ulRowNumber_ peut être n’importe quelle valeur de 0, ce qui indique la première ligne du tableau, à n - 1, ce qui indique la dernière ligne du tableau. 
    
 _lppSRow_
  
> [out] Pointeur vers un pointeur vers une structure [SRow](srow.md) qui décrit la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été récupérée correctement ou une ligne pour le numéro de ligne spécifié par le paramètre  _ulRowNumber_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrEnumRow** récupère une ligne basée sur un numéro séquentiel. Ce nombre représente l’ordre d’insertion (0 indique la première ligne et le nombre de lignes moins 1 indique la dernière ligne). MAPI conserve cet ordre chronologique d’insertion de ligne pour la durée de vie de l’objet de données de table. 
  
Si le nombre spécifié dans  _ulRowNumber_ ne correspond à aucune ligne du tableau, **HrEnumRow** renvoie S_OK et définit le paramètre  _lppSRow_ sur NULL. 
  
MAPI alloue de la mémoire pour la structure **SRow** renvoyée à l’aide de la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) lors de la création de l’objet de données de table. L’appelant doit libérer cette mémoire en appelant la [fonction MAPIFreeBuffer.](mapifreebuffer.md) 
  
Pour extraire des lignes d’une table dans l’ordre dans l’ordre où elles ont été insérées, les utilisateurs d’objets de données de table appellent la **méthode HrEnumRow.** 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

