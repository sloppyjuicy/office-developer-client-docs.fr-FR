---
title: ITableDataHrQueryRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrQueryRow
api_type:
- COM
ms.assetid: 66ce8f36-2b2b-4a8e-b9b2-43782d8357a1
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a513fbe235a61b331f05c7c99d11f9adc3c987ac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556223"
---
# <a name="itabledatahrqueryrow"></a>ITableData::HrQueryRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
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
  
> [in] Pointeur vers une structure de valeurs de propriété qui décrit la colonne d’index de la ligne à récupérer. Le **membre ulPropTag** de la structure de valeurs de propriété doit contenir la même balise de propriété que le paramètre _ulPropTagIndexColumn_ de l’appel à la fonction [CreateTable,](createtable.md) qui accède à l’implémentation [ITableData.](itabledataiunknown.md) 
    
 _lppSRow_
  
> [out] Pointeur vers un pointeur vers la ligne récupérée. 
    
 _lpuliRow_
  
> [in, out] Lors de l’entrée, un pointeur valide ou NULL, qui indique qu’aucune information ne doit être renvoyée. En sortie, un pointeur valide qui pointe vers le numéro de ligne de la ligne, un numéro séquentiel qui identifie la position de la ligne dans le tableau.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été récupérée avec succès.
    
MAPI_E_INVALID_PARAMETER 
  
> La structure [SPropValue](spropvalue.md) vers qui  _pointe lpSPropValue_ ne contient pas la propriété de colonne d’index. 
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrQueryRow** récupère toutes les propriétés de la ligne qui possède une colonne d’index qui correspond à la valeur de la colonne d’index incluse dans la structure de propriétés pointée par  _lpSPropValue_. **HrQueryRow renvoie** également le numéro de ligne, si l’appelant le demande, qui identifie la position de la ligne dans le tableau. 
  
Étant donné que **HrQueryRow** ne modifie pas la structure **SPropValue** pointée par _lpSPropValue_, les appelants doivent libérer la structure lorsque **HrQueryRow renvoie.** Les appelants doivent également libérer la structure **SRow** qui contient la ligne récupérée. 
  
## <a name="see-also"></a>Voir aussi



[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropValue](spropvalue.md)
  
[SRow](srow.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

