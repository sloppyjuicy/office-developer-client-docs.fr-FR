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
ms.openlocfilehash: 3874e7549ff1c20145ed23923f64981c5e22946c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63380724"
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
  
> [in] Pointeur vers une structure de valeurs de propriété qui décrit la colonne d’index de la ligne à supprimer. Le **membre ulPropTag** de la structure de valeurs de propriété doit contenir la même balise de propriété que le paramètre  _ulPropTagIndexColumn_ de l’appel à la [fonction CreateTable](createtable.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été supprimée avec succès.
    
MAPI_E_NOT_FOUND 
  
> La propriété pointée par  _le paramètre lpSPropValue_ n’identifie pas une ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété pointée par le paramètre  _lpSPropValue_ . Les données de la ligne sont supprimées et la ligne est supprimée de tous les affichages ouverts. 
  
Une fois la ligne supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. 
  
La suppression d’une ligne ne réduit pas le jeu de colonnes disponible pour les affichages existants ou les affichages ouverts par la suite, même si la ligne supprimée est la dernière ligne qui a une valeur pour une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

