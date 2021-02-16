---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435438"
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

La **méthode ITableData::HrInsertRow** insère une ligne dans un tableau à une position particulière. La nouvelle ligne est insérée après la ligne qui se trouve à la position spécifiée par le _paramètre uliRow._ 
  
Si  _uliRow est_ définie sur le nombre de lignes du tableau, la nouvelle ligne est ajouté à la fin du tableau. 
  
La propriété qui agit comme colonne d’index pour la table doit être incluse dans le membre **lpProps** de la structure [SRow](srow.md) pointée par le _paramètre lpSRow._ Cette propriété d’index, **généralement PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), est utilisée pour identifier de manière unique la ligne pour les tâches de maintenance futures.
  
Les colonnes de propriétés de la structure **SRow** ne doivent pas être dans le même ordre que les colonnes de propriétés du tableau. 
  
Une fois la ligne insérée, des notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. Aucune notification n’est envoyée si la ligne insérée n’est pas incluse dans l’affichage en raison d’une restriction. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

