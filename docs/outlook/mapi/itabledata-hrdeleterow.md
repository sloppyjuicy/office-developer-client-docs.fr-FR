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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784462"
---
# <a name="itabledatahrdeleterow"></a>ITableData::HrDeleteRow

  
  
**S’applique à**: Outlook 
  
Supprime une ligne de tableau.
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a>Paramètres

 _lpSPropValue_
  
> [in] Pointeur vers une structure de valeur de propriété qui décrit la colonne d’index de la ligne à supprimer. Le membre **ulPropTag** de la structure de valeur de propriété doit contenir la même balise de propriété en tant que paramètre _ulPropTagIndexColumn_ de l’appel à la fonction [Create table](createtable.md) . 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La ligne a été supprimée.
    
MAPI_E_NOT_FOUND 
  
> La propriété désignée par le paramètre _lpSPropValue_ n’identifie pas une ligne dans le tableau. 
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrDeleteRow** supprime la ligne de tableau qui contient la colonne qui correspond à la propriété désignée par le paramètre _lpSPropValue_ . Les données de la ligne sont supprimées et la ligne est supprimée de toutes les vues ouvertes. 
  
Une fois que la ligne est supprimée, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. 
  
Suppression d’une ligne ne réduit pas l’ensemble de colonnes qui est disponible pour les vues existantes ou ouvert par la suite les affichages, même si la ligne supprimée est la dernière ligne ayant une valeur d’une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[Create table](createtable.md)
  
[ITableData::HrDeleteRows](itabledata-hrdeleterows.md)
  
[ITableData::HrModifyRow](itabledata-hrmodifyrow.md)
  
[SPropValue](spropvalue.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

