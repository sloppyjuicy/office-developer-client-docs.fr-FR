---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8127a09582c98fc82fb5be92dbf24a4e84911ada
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575784"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Renvoie l’état et le type de la table.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Paramètres

 _lpulTableStatus_
  
> [out] Pointeur vers une valeur indiquant l’état du tableau. L’une des valeurs suivantes peut être renvoyée :
    
TBLSTAT_COMPLETE 
  
> Aucune opération n’est en cours.
    
TBLSTAT_QCHANGED 
  
> Le contenu de la table a été modifié. Cette valeur d’état n’est pas renvoyée pour les modifications résultant d’opérations de tri ou de restriction.
    
TBLSTAT_RESTRICT_ERROR 
  
> Une erreur s’est produite [lors d’une opération IMAPITable::Restrict.](imapitable-restrict.md) 
    
TBLSTAT_RESTRICTING 
  
> Une **opération IMAPITable::Restrict** est en cours. 
    
TBLSTAT_SETCOL_ERROR 
  
> Une erreur s’est produite [lors d’une opération IMAPITable::SetColumns.](imapitable-setcolumns.md) 
    
TBLSTAT_SETTING_COLS 
  
> Une **opération IMAPITable::SetColumns** est en cours. 
    
TBLSTAT_SORT_ERROR 
  
> Une erreur s’est produite [lors d’une opération IMAPITable::SortTable.](imapitable-sorttable.md) 
    
TBLSTAT_SORTING 
  
> Une **opération IMAPITable::SortTable** est en cours. 
    
 _lpulTableType_
  
> [out] Pointeur vers une valeur qui indique le type du tableau. L’un des trois types de tableau suivants peut être renvoyé :
    
TBLTYPE_DYNAMIC 
  
> Le contenu de la table est dynamique ; les lignes et les valeurs de colonne peuvent changer à mesure que les données sous-jacentes changent.
    
TBLTYPE_KEYSET 
  
> Les lignes du tableau sont fixes, mais les valeurs des colonnes de ces lignes sont dynamiques et peuvent changer à mesure que les données sous-jacentes changent.
    
TBLTYPE_SNAPSHOT 
  
> La table est statique et son contenu ne change pas lorsque les données sous-jacentes changent.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’état de la table a été renvoyé avec succès.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPTable::GetStatus** récupère des informations sur le type et l’état actuel d’une table. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous pouvez utiliser **GetStatus** conjointement avec trois autres méthodes **IMAPITable** pour surveiller l’état de ces opérations et déterminer l’effet sur le tableau. Appelez **GetStatus après** avoir passé l’un des appels **IMAPITable** suivants : 
  
- [IMAPITable::Restrict](imapitable-restrict.md) pour définir une restriction. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) pour établir un ordre de tri. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir un jeu de colonnes. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI utilise la **méthode IMAPITable::GetStatus** pour signaler l’état d’une table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

