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
ms.openlocfilehash: 9aa038958e26652ae7ead728ab15d068e080dc69
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579885"
---
# <a name="itabledatahrinsertrow"></a>ITableData::HrInsertRow

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Insère une ligne de tableau. 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a>Paramètres

 _uliRow_
  
> [in] Un numéro de ligne séquentiel qui représente une ligne spécifique. La nouvelle ligne est placée après la ligne qui indique le nombre. Le paramètre _uliRow_ peut contenir des numéros de ligne de n à 0, où n est le nombre total de lignes dans le tableau. En passant n _uliRow_ ajoute la ligne à la fin de la table. 
    
 _lpSRow_
  
> [in] Pointeur vers une structure [SRow](srow.md) qui décrit la ligne doit être inséré. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La ligne a été insérée correctement.
    
MAPI_E_INVALID_PARAMETER 
  
> Une ligne qui possède la même valeur pour la colonne d’index que la ligne doit être inséré déjà existe dans le tableau.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrInsertRow** insère une ligne dans une table à un emplacement particulier. La nouvelle ligne est insérée après la ligne qui se trouve dans la position spécifiée par le paramètre _uliRow_ . 
  
Si _uliRow_ est défini sur le nombre de lignes dans le tableau, la nouvelle ligne est ajoutée à la fin de la table. 
  
La propriété agit en tant que la colonne d’index pour la table doit être incluse dans le membre **lpProps** de la structure [SRow](srow.md) désigné par le paramètre _lpSRow_ . Cette propriété index, généralement **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), sert à identifier de manière unique la ligne pour les tâches de maintenance future.
  
Les colonnes de propriétés dans la structure **SRow** n’ont pas à se trouver dans le même ordre que les colonnes de propriétés dans le tableau. 
  
Une fois que la ligne est insérée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. Aucune notification n’est envoyée si la ligne insérée n’est pas incluse dans l’affichage en raison d’une restriction. 
  
## <a name="see-also"></a>Voir aussi



[SRow](srow.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

