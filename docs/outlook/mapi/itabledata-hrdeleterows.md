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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784458"
---
# <a name="itabledatahrdeleterows"></a>ITableData::HrDeleteRows

  
  
**S’applique à**: Outlook 
  
Supprime plusieurs lignes de tableau.
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la suppression. Vous pouvez définir l’indicateur suivant :
    
TAD_ALL_ROWS 
  
> Supprime toutes les lignes de la table et toutes les vues correspondants, l’envoi d’une notification TABLE_RELOAD unique.
    
 _lprowsetToDelete_
  
> [in] Pointeur vers un ensemble de lignes qui décrit les lignes à supprimer. Le paramètre _lprowsetToDelete_ peut être NULL si l’indicateur TAD_ALL_ROWS est défini dans le paramètre _ulFlags_ . 
    
 _cRowsDeleted_
  
> [out] Le nombre de lignes supprimées.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les lignes de table ont été supprimés.
    
## <a name="remarks"></a>Remarques

La méthode **ITableData::HrDeleteRows** localise et supprime les lignes de la table contenant les colonnes qui correspondent à la propriété pointée pour définir les par le membre **lpProps** de chaque entrée **: UGAL** dans la ligne. Une colonne d’index est utilisée pour identifier chaque ligne ; Cette colonne doit avoir la même balise de propriété en tant que la balise de propriété passée dans le paramètre _ulPropTagIndexColumn_ dans l’appel à la fonction [Create table](createtable.md) . 
  
Le nombre de lignes qui ont été supprimées réellement est retourné dans _cRowsDeleted_. Aucune erreur n’est renvoyée si une ou plusieurs lignes est introuvable. 
  
Une fois que les lignes sont supprimées, les notifications sont envoyées à tous les clients ou fournisseurs de services qui ont une vue de la table et qui ont appelé la méthode la table [IMAPITable::Advise](imapitable-advise.md) pour inscrire les notifications. 
  
Suppression de lignes ne réduit pas les colonnes aux tableaux existants ou ouvert par la suite des affichages tableau, même si les lignes supprimées sont la dernière ayant des valeurs d’une colonne spécifique.
  
## <a name="see-also"></a>Voir aussi



[Create table](createtable.md)
  
[ITableData::HrDeleteRow](itabledata-hrdeleterow.md)
  
[ITableData::HrModifyRows](itabledata-hrmodifyrows.md)
  
[SRowSet](srowset.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[ITableData : IUnknown](itabledataiunknown.md)

