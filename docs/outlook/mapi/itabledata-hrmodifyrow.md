---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408998"
---
# <a name="itabledatahrmodifyrow"></a>ITableData::HrModifyRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Insère une nouvelle ligne de tableau, éventuellement en remplaçant une ligne existante.
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Parameters

 _lpSRow_
  
> [in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à ajouter ou à remplacer une ligne existante. L’une des structures de valeurs de propriétés pointées par le membre **lpProps** de la structure **SRow** doit contenir la colonne d’index, la même valeur que celle spécifiée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la fonction [CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été insérée ou modifiée avec succès.
    
MAPI_E_INVALID_PARAMETER 
  
> La ligne transmise ne comprend pas de colonne d’index.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrModifyRow** insère la ligne décrite par la structure **SRow** pointée par _le paramètre lpSRow._ Si une ligne qui a la même valeur pour sa colonne d’index que la ligne vers qui  _pointe lpSRow_ existe déjà dans le tableau, la ligne existante est remplacée. S’il n’existe aucune ligne qui corresponde à celle incluse dans la structure **SRow,** **HrModifyRow** ajoute la ligne à la fin du tableau. 
  
Tous les affichages du tableau sont modifiés pour inclure la ligne pointée par  _lpSRow_. Toutefois, si une restriction est en place dans un affichage qui exclut la ligne, il se peut qu’elle ne soit pas visible pour l’utilisateur. 
  
Les colonnes de la ligne pointées par  _lpSRow_ ne doivent pas être dans le même ordre que les colonnes du tableau. L’appelant peut également inclure en tant que propriétés de colonnes qui ne figurent pas actuellement dans le tableau. Pour les affichages existants, **HrModifyRow** rend ces nouvelles colonnes disponibles, mais ne les inclut pas dans le jeu de colonnes actuel. Pour les affichages futurs, **HrModifyRow** inclut les nouvelles colonnes dans le jeu de colonnes. 
  
Une fois **que HrModifyRow** a ajouté la ligne, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

