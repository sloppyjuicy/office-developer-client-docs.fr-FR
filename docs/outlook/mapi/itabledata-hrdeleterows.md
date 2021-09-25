---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 48810ea68394fa21ad666dfc8464bbf12b2c8359
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584226"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime plusieurs lignes de tableau.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la suppression. L’indicateur suivant peut être définie :
    
TAD_ALL_ROWS 
  
> Supprime toutes les lignes de la table et tous les affichages correspondants, en envoyant une notification TABLE_RELOAD unique.
    
 _lprowsetToDelete_
  
> [in] Pointeur vers un ensemble de lignes qui décrit les lignes à supprimer. Le _paramètre lprowsetToDelete_ peut être NULL si l’TAD_ALL_ROWS est définie dans le _paramètre ulFlags._ 
    
 _cRowsDeleted_
  
> [out] Nombre de lignes supprimées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes de tableau ont été supprimées avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode ITableData::HrDeleteRows** localise et supprime les lignes de tableau qui contiennent les colonnes qui correspondent à la propriété pointée par le membre **lpProps** de chaque entrée **aRow** dans le jeu de lignes. Une colonne d’index est utilisée pour identifier chaque ligne ; Cette colonne doit avoir la même balise de propriété que la balise de propriété transmise dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la [fonction CreateTable.](createtable.md) 
  
Le nombre de lignes réellement supprimées est renvoyé dans  _cRowsDeleted_. Aucune erreur n’est renvoyée si une ou plusieurs lignes sont in trouvées. 
  
Une fois les lignes supprimées, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable::Advise](imapitable-advise.md) de la table pour s’inscrire aux notifications. 
  
La suppression de lignes ne réduit pas les colonnes disponibles pour les affichages table existants ou les affichages de tableau ouverts par la suite, même si les lignes supprimées sont les dernières qui ont des valeurs pour une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

