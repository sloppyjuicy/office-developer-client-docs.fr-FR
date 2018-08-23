---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: cda3de1719ec1b7cfca1a9ecdad7bc3b59a8b17d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571149"
---
# <a name="imapitablegetstatus"></a>IMAPITable::GetStatus

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Renvoie l’état et le type de la table.
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a>Paramètres

 _lpulTableStatus_
  
> [out] Pointeur vers une valeur indiquant l’état de la table. Une des valeurs suivantes peut être renvoyée :
    
TBLSTAT_COMPLETE 
  
> Aucune opération n’est en cours.
    
TBLSTAT_QCHANGED 
  
> Le contenu de la table ont changé expectantly. Cette valeur d’état n’est pas retournée pour que les modifications qui résultent des opérations de tri ou de restriction.
    
TBLSTAT_RESTRICT_ERROR 
  
> Une erreur s’est produite pendant une opération [IMAPITable](imapitable-restrict.md) . 
    
TBLSTAT_RESTRICTING 
  
> Une opération **IMAPITable** est en cours. 
    
TBLSTAT_SETCOL_ERROR 
  
> Une erreur s’est produite pendant une opération [IMAPITable::SetColumns](imapitable-setcolumns.md) . 
    
TBLSTAT_SETTING_COLS 
  
> Une opération **IMAPITable::SetColumns** est en cours. 
    
TBLSTAT_SORT_ERROR 
  
> Une erreur s’est produite pendant une opération [IMAPITable::SortTable](imapitable-sorttable.md) . 
    
TBLSTAT_SORTING 
  
> Une opération **IMAPITable::SortTable** est en cours. 
    
 _lpulTableType_
  
> [out] Pointeur vers une valeur qui indique le type de la table. Un des types de trois tableau suivantes peut être renvoyé :
    
TBLTYPE_DYNAMIC 
  
> Le contenu de la table est dynamique ; les lignes et les valeurs de colonne peuvent changer en tant que les modifications de données sous-jacente.
    
TBLTYPE_KEYSET 
  
> Les lignes dans le tableau sont fixe, mais les valeurs de colonnes dans les lignes sont dynamiques et peuvent changer lorsque les modifications de données sous-jacente.
    
TBLTYPE_SNAPSHOT 
  
> Le tableau est statique et son contenu n’est pas modifié lorsque les données sous-jacentes changent.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’état de la table a été renvoyée avec succès.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPTable::GetStatus** récupère des informations sur le type et l’état actuel d’une table. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous pouvez utiliser **GetStatus** conjointement avec les trois autres méthodes **IMAPITable** pour surveiller l’état de ces opérations et de déterminer l’incidence sur le tableau. Appelez **GetStatus** après avoir effectué une des appels **IMAPITable** suivants : 
  
- [IMAPITable](imapitable-restrict.md) pour définir une restriction. 
    
- [IMAPITable::SortTable](imapitable-sorttable.md) pour établir un ordre de tri. 
    
- [IMAPITable::SetColumns](imapitable-setcolumns.md) pour définir un ensemble de colonnes. 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::GetStatus  <br/> |MFCMAPI utilise la méthode **IMAPITable::GetStatus** pour indiquer l’état d’une table.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPITable::Restrict](imapitable-restrict.md)
  
[IMAPITable::SetColumns](imapitable-setcolumns.md)
  
[IMAPITable::SortTable](imapitable-sorttable.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

