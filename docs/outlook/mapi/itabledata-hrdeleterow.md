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
ms.openlocfilehash: 989c6872e78ef78e5e0b18149a186d4f920ca603
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563463"
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
  
> [in] Pointeur vers une structure de valeur de propriété qui décrit la colonne d’index de la ligne à supprimer. Le membre **ulPropTag** de la structure de valeur de propriété doit contenir la même balise de propriété en tant que paramètre _ulPropTagIndexColumn_ de l’appel à la fonction [Create table](createtable.md) . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La ligne a été supprimée.
    
MAPI_E_NOT_FOUND 
  
> La propriété désignée par le paramètre _lpSPropValue_ n’identifie pas une ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété désignée par le paramètre _lpSPropValue_ . Les données de la ligne sont supprimées et la ligne est supprimée de toutes les vues ouvertes. 
  
Une fois que la ligne est supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. 
  
Suppression d’une ligne ne réduit pas l’ensemble de colonnes qui est disponible pour les vues existantes ou ouvert par la suite les affichages, même si la ligne supprimée est la dernière ligne ayant une valeur d’une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

