---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 693569c5b7ce6915bc30857445dca5b7e55c63c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613764"
---
# <a name="itabledatahrmodifyrows"></a>ITableData::HrModifyRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Insère plusieurs lignes de tableau, en remplaçant éventuellement les lignes existantes.
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpSRowSet_
  
> [in] Pointeur vers une structure [SRowSet](srowset.md) qui contient l’ensemble de lignes à ajouter, en remplaçant les lignes existantes si nécessaire. L’une des structures de valeurs de propriétés pointées par le membre **lpProps** de chaque structure [SRow](srow.md) dans le jeu de lignes doit contenir la colonne d’index, la même valeur spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la fonction [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes ont été insérées ou modifiées avec succès.
    
MAPI_E_INVALID_PARAMETER 
  
> Une ou plusieurs lignes transmises n’ont pas de colonne d’index. Si cette erreur est renvoyée, aucune ligne n’est modifiée.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrModifyRows insère** les lignes décrites par la structure [SRowSet](srowset.md) pointée vers le _paramètre lpSRowSet._ Si la valeur de colonne d’index d’une ligne du jeu de lignes correspond à la valeur d’une ligne existante du tableau, la ligne existante est remplacée. S’il n’existe aucune ligne qui corresponde à celle incluse dans la structure **SRowSet,** **HrModifyRows** ajoute la ligne à la fin du tableau. 
  
Tous les affichages de la table sont modifiés pour inclure les lignes pointées par  _lpSRowSet_. Toutefois, si une restriction est en place sur un affichage qui exclut une ligne, il se peut qu’elle ne soit pas visible pour l’utilisateur. 
  
Les colonnes des lignes pointées par  _lpSRowSet_ ne doivent pas être dans le même ordre que les colonnes du tableau. L’appelant peut également inclure en tant que propriétés de colonnes qui ne figurent pas actuellement dans le tableau. Pour les affichages **existants, HrModifyRows** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel. Pour les affichages futurs, **HrModifyRows** inclut les nouvelles colonnes dans le jeu de colonnes. 
  
Une fois **que HrModifyRows** a ajouté les lignes, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. MAPI envoie TABLE_ROW_ADDED ou TABLE_ROW_MODIFIED notifications pour chaque ligne, jusqu’à huit lignes. Si plus de huit lignes sont affectées par l’appel **HrModifyRows,** MAPI envoie une seule notification TABLE_CHANGED à la place. 
  
## <a name="see-also"></a>Voir aussi



[SRowSet](srowset.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

