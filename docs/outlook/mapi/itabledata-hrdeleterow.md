---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b187cccc4505256b7ab4d580c30eeb2e15ebf574
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421675"
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
  
> dans Pointeur vers une structure de valeur de propriété qui décrit la colonne d'index de la ligne à supprimer. Le membre **ulPropTag** de la structure de la valeur de la propriété doit contenir la même balise property que le paramètre _ulPropTagIndexColumn_ de l'appel à la fonction [CreateTable](createtable.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été supprimée.
    
MAPI_E_NOT_FOUND 
  
> La propriété désignée par le paramètre _lpSPropValue_ n'identifie pas une ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété désignée par le paramètre _lpSPropValue_ . Les données de la ligne sont supprimées et la ligne est supprimée de toutes les vues ouvertes. 
  
Une fois la ligne supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications. 
  
La suppression d'une ligne ne réduit pas le jeu de colonnes disponible pour les affichages existants ou les vues ouvertes par la suite, même si la ligne supprimée est la dernière ligne contenant une valeur pour une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

