---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: dc516d8792fe87e6b9caf282146ad8ef996715c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59587845"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime une ligne de tableau.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> [in] Pointeur vers une structure de valeurs de propriété qui décrit la colonne d’index de la ligne à supprimer. Le **membre ulPropTag** de la structure de valeurs de propriété doit contenir la même balise de propriété que le paramètre _ulPropTagIndexColumn_ de l’appel à la [fonction CreateTable.](createtable.md) 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été supprimée avec succès.
    
MAPI_E_NOT_FOUND 
  
> La propriété pointée par  _le paramètre lpSPropValue_ n’identifie pas une ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété pointée par le paramètre _lpSPropValue._ Les données de la ligne sont supprimées et la ligne est supprimée de tous les affichages ouverts. 
  
Une fois la ligne supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. 
  
La suppression d’une ligne ne réduit pas le jeu de colonnes disponible pour les affichages existants ou les affichages ouverts ultérieurement, même si la ligne supprimée est la dernière ligne qui a une valeur pour une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

