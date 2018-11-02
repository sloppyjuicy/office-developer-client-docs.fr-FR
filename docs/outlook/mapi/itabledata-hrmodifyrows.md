---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 06356d60b43d7e5be61d944c07001570bdd5c678
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571107"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Insère plusieurs lignes de tableau, remplaçant éventuellement les lignes existantes.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpSRowSet_
  
> [in] Un pointeur vers une structure [SRowSet](srowset.md) qui contient l’ensemble de lignes à ajouter, en remplaçant les lignes existantes, si nécessaire. Une des structures de valeur de propriété pointés pour définir les par le membre **lpProps** de chaque structure [SRow](srow.md) dans la ligne doit contenir la colonne d’index, la même valeur que celle qui a été spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la [ CREATE TABLE](createtable.md) fonction. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes insérées ou modifiées avec succès.
    
MAPI_E_INVALID_PARAMETER 
  
> Un ou plusieurs des lignes dans le passé ne dispose pas d’une colonne d’index. Si cette erreur est renvoyée, aucune ligne n’est modifiés.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrModifyRows** insère les lignes décrites par la structure [SRowSet](srowset.md) désignée par le paramètre _lpSRowSet_ . Si la valeur de colonne d’index d’une ligne dans le jeu de lignes correspond à la valeur d’une ligne existante dans le tableau, la ligne existante est remplacée. Si aucune ligne n’existe qui correspond à celui qui est inclus dans la structure **SRowSet** , **HrModifyRows** ajoute la ligne à la fin de la table. 
  
Toutes les vues de la table sont modifiées pour inclure les lignes désignés par _lpSRowSet_. Toutefois, si un affichage a une restriction place excluant une ligne, il peut être pas visible à l’utilisateur. 
  
Les colonnes dans les lignes désignés par _lpSRowSet_ n’ont pas à se trouver dans le même ordre que les colonnes dans le tableau. L’appelant peut également inclure en tant que propriétés de colonnes qui ne sont pas actuellement dans le tableau. Pour des vues existantes, **HrModifyRows** rend ces nouvelles colonnes disponibles, mais n’inclut pas les dans la colonne en cours. Pour les affichages futures, **HrModifyRows** inclut les nouvelles colonnes dans la colonne. 
  
Une fois que **HrModifyRows** a ajouté les lignes, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. MAPI envoie des notifications TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED pour chaque ligne, jusqu'à huit lignes. Si plus de huit lignes sont affectées par l’appel **HrModifyRows** , MAPI envoie une notification TABLE_CHANGED unique à la place. 
  
## <a name="see-also"></a>Voir aussi



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

