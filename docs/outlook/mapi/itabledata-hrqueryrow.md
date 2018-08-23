---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef0dc212a6a6f761cd8dd0cae5312c548c02ae50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583819"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Récupère une ligne de tableau.
  
```cpp
HRESULT HrQueryRow(
  LPSPropValue lpSPropValue,
  LPSRow FAR * lppSRow,
  ULONG FAR * lpuliRow
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> [in] Pointeur vers une structure de valeur de propriété qui décrit la colonne d’index de la ligne à récupérer. Le membre **ulPropTag** de la structure de valeur de propriété doit contenir la même balise de propriété en tant que paramètre de l’appel à la fonction [Create table](createtable.md) , qui accède à l’implémentation [ITableData](itabledataiunknown.md) _ulPropTagIndexColumn_ . 
    
 _lppSRow_
  
> [out] Pointeur vers un pointeur vers la ligne récupérée. 
    
 _lpuliRow_
  
> [entrée, sortie] Sur entrée, un pointeur valide ou valeur NULL, ce qui indique qu’aucune information ne doit être renvoyé. Sur la sortie, un pointeur valid qui pointe vers le numéro de la ligne de la ligne, un numéro qui identifie la position de la ligne dans la table.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La ligne a été récupérée correctement.
    
MAPI_E_INVALID_PARAMETER 
  
> Le [SPropValue](spropvalue.md) structure _lpSPropValue_ pointant vers ne contient ne pas la propriété de colonne d’index. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrQueryRow** récupère toutes les propriétés de la ligne qui a une colonne d’index qui correspond à la valeur de la colonne d’index incluse dans la structure de propriété désignée par _lpSPropValue_. **HrQueryRow** renvoie également le numéro de ligne, si l’appelant demande, qui identifie la position de la ligne dans la table. 
  
Étant donné que **HrQueryRow** ne modifie pas la structure **SPropValue** désignée par _lpSPropValue_, les appelants doivent libérer la structure lorsque **HrQueryRow** renvoie. Les appelants doivent également libérer la structure **SRow** qui contient la ligne récupérée. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

