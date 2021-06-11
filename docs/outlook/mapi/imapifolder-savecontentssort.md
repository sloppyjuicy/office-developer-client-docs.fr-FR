---
title: IMAPIFolderSaveContentsSort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.SaveContentsSort
api_type:
- COM
ms.assetid: 5ae3fdf0-6193-4c1f-bd2e-d69c56d69773
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c142424bb050ae287f54a87ea8a5e0ea45acb12c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411616"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit l’ordre de tri par défaut pour la table des matières d’un dossier.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _lpSortCriteria_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient l’ordre de tri par défaut. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’ordre de tri par défaut est définie. L’indicateur suivant peut être définie :
    
RECURSIVE_SORT 
  
> Le jeu d’ordre de tri par défaut s’applique au dossier indiqué et à tous ses sous-dossiers.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ordre de tri a été enregistré avec succès.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de magasins de messages ne prend pas en charge l’enregistrement d’un ordre de tri pour ses tables de contenu de dossiers.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::SaveContentsSort** établit un ordre de tri par défaut pour la table des matières d’un dossier. Autrement dit, lorsqu’un client appelle la méthode [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier après que le code appelle **SaveContentsSort,** les lignes de la table des matières retournée apparaissent dans l’ordre établi par **SaveContentsSort**.
  
Tous les fournisseurs de magasins de messages ne sont pas en charge **SaveContentsSort**; Il est acceptable que les fournisseurs de magasins de messages MAPI_E_NO_SUPPORT à partir de la **méthode SaveContentsSort.** 
  
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

