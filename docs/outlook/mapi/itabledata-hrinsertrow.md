---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
ms.openlocfilehash: 08c39af45e3bcc07348243119e49e529cad465aa
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63376237"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Insère une ligne de tableau. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Paramètres

 _uliRow_
  
> [in] Numéro de ligne séquentiel qui représente une ligne spécifique. La nouvelle ligne est placée après la ligne indiquée par le numéro. Le  _paramètre uliRow_ peut contient des numéros de ligne de 0 à n, où n est le nombre total de lignes dans le tableau. La transmission de  _n dans uliRow_ permet d’annexer la ligne à la fin du tableau. 
    
 _lpSRow_
  
> [in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne à insérer. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été insérée avec succès.
    
MAPI_E_INVALID_PARAMETER 
  
> Une ligne qui a la même valeur pour sa colonne d’index que la ligne à insérer existe déjà dans le tableau.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrInsertRow** insère une ligne dans un tableau à une position particulière. La nouvelle ligne est insérée après la ligne qui se trouve à la position spécifiée par le  _paramètre uliRow_ . 
  
Si  _uliRow est_ définie sur le nombre de lignes du tableau, la nouvelle ligne est ajouté à la fin du tableau. 
  
La propriété qui agit en tant que colonne d’index pour la table doit être incluse dans le membre **lpProps** de la structure [SRow](srow.md) pointée par le  _paramètre lpSRow_ . Cette propriété d’index, **généralement PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), est utilisée pour identifier de manière unique la ligne pour les tâches de maintenance futures.
  
Les colonnes de propriétés de la structure **SRow** ne doivent pas être dans le même ordre que les colonnes de propriétés du tableau. 
  
Une fois la ligne insérée, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. Aucune notification n’est envoyée si la ligne insérée n’est pas incluse dans l’affichage en raison d’une restriction. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

