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
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 50fd96acd0989459c9887770ec5a3a236f182da5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348894"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère une ligne en fonction de sa position dans le tableau. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Paramètres

 _ulRowNumber_
  
> dans Numéro de la ligne dont les propriétés doivent être renvoyées. La valeur du paramètre _ulRowNumber_ peut être n'importe quelle valeur comprise entre 0, qui indique la première ligne du tableau, à n-1, qui indique la dernière ligne du tableau. 
    
 _lppSRow_
  
> remarquer Pointeur vers un pointeur vers une structure [SRow](srow.md) qui décrit la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été récupérée correctement ou une ligne pour le numéro de ligne spécifié par le paramètre _ulRowNumber_ n'existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrEnumRow** extrait une ligne en fonction d'un numéro séquentiel. Ce nombre représente l'ordre d'insertion (0 indique la première ligne et le nombre de lignes moins 1 indique la dernière ligne). MAPI conserve cet ordre chronologique d'insertion de ligne pendant la durée de vie de l'objet de données de tableau. 
  
Si le nombre spécifié dans _ulRowNumber_ ne correspond pas à une ligne de la table, **HrEnumRow** renvoie S_OK et définit le paramètre _lppSRow_ sur null. 
  
MAPI alloue de la mémoire pour la structure **SRow** renvoyée à l'aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) lors de la création de l'objet de données de table. L'appelant doit libérer cette mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour récupérer des lignes d'un tableau dans l'ordre dans lequel elles ont été insérées, les utilisateurs de données de tableau appellent la méthode **HrEnumRow** . 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

