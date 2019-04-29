---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416453"
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
  
> dans Masque de des indicateurs qui contrôle la suppression. L'indicateur suivant peut être défini:
    
TAD_ALL_ROWS 
  
> Supprime toutes les lignes de la table et de toutes les vues correspondantes, en envoyant une seule notification TABLE_RELOAD.
    
 _lprowsetToDelete_
  
> dans Pointeur vers un jeu de lignes qui décrit les lignes à supprimer. Le paramètre _lprowsetToDelete_ peut être null si l'indicateur TAD_ALL_ROWS est défini dans le paramètre _ulFlags_ . 
    
 _cRowsDeleted_
  
> remarquer Nombre de lignes supprimées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les lignes de tableau ont été supprimées avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData:: HrDeleteRows** localise et supprime les lignes de table qui contiennent les colonnes qui correspondent à la propriété sur laquelle pointe le membre **LpProps** de chaque **aRow** entrée du jeu de lignes. Une colonne d'index est utilisée pour identifier chaque ligne; Cette colonne doit avoir la même balise de propriété que la balise de propriété passée dans le paramètre _ulPropTagIndexColumn_ dans l'appel à la fonction [CreateTable](createtable.md) . 
  
Le nombre de lignes réellement supprimées est renvoyé dans _cRowsDeleted_. Aucune erreur n'est renvoyée si une ou plusieurs lignes sont introuvables. 
  
Une fois les lignes supprimées, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode [IMAPITable:: Advise](imapitable-advise.md) pour s'inscrire aux notifications. 
  
La suppression de lignes ne réduit pas les colonnes disponibles pour les affichages de tableau existants ou les vues de table ouvertes par la suite, même si les lignes supprimées sont les dernières qui contiennent des valeurs pour une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[CreateTable](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

