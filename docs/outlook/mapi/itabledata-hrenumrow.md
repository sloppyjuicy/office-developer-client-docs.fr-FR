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
ms.openlocfilehash: 140efe0b2d1b428a94b5bb2919d461779613932a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564681"
---
# <a name="itabledatahrenumrow"></a>ITableData::HrEnumRow

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupère une ligne en fonction de sa position dans le tableau. 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a>Paramètres

 _ulRowNumber_
  
> [in] Le numéro de la ligne pour laquelle retourner les propriétés. La valeur dans le paramètre _ulRowNumber_ peut être n’importe quelle valeur comprise entre 0, ce qui indique la première ligne dans le tableau, à n - 1, ce qui indique la dernière ligne dans le tableau. 
    
 _lppSRow_
  
> [out] Pointeur vers un pointeur vers une structure [SRow](srow.md) qui décrit la ligne cible. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La ligne a été récupérée avec succès, ou une ligne pour le numéro de la ligne spécifiée par le paramètre _ulRowNumber_ n’existe pas. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrEnumRow** récupère une ligne basée sur un numéro séquentiel. Ce nombre représente l’ordre d’insertion (0 indique que la première ligne et le nombre de lignes moins 1 indique la dernière ligne). MAPI gère cet ordre chronologique d’insertion de ligne pour la durée de vie de l’objet de données de table. 
  
Si le numéro spécifié dans _ulRowNumber_ ne correspond pas à une ligne dans le tableau, **HrEnumRow** renvoie S_OK et définit le paramètre _lppSRow_ sur NULL. 
  
MAPI alloue de la mémoire pour la structure **SRow** retournée à l’aide de la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) lors de la création de l’objet de données de table. L’appelant doit libérer cette mémoire en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Pour récupérer des lignes d’une table dans l’ordre qu’ils ont été insérés, les utilisateurs de tableau données objet appeler la méthode **HrEnumRow** . 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

