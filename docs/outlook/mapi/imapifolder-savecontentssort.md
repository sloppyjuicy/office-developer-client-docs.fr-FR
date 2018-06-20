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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 7c8ccada96b3e34372d488e16c85627e8b6b0cd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783738"
---
# <a name="imapifoldersavecontentssort"></a>IMAPIFolder::SaveContentsSort

  
  
**S’applique à**: Outlook 
  
Définit l’ordre de tri par défaut pour la table des matières d’un dossier.
  
```cpp
HRESULT SaveContentsSort(
  LPSSortOrderSet lpSortCriteria,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpSortCriteria_
  
> [in] Pointeur vers une structure [SSortOrderSet](ssortorderset.md) qui contient l’ordre de tri par défaut. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’ordre de tri par défaut est défini. Vous pouvez définir l’indicateur suivant :
    
RECURSIVE_SORT 
  
> L’ensemble d’ordre de tri par défaut s’applique au dossier indiqué et tous ses sous-dossiers.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’ordre de tri a été enregistré avec succès.
    
MAPI_E_NO_SUPPORT 
  
> Le fournisseur de banque de messages n’autorise pas l’enregistrement d’un ordre de tri pour les tables de son contenu de dossier.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::SaveContentsSort** établit un ordre de tri par défaut pour la table des matières d’un dossier. Autrement dit, lorsqu’un client appelle la méthode de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) du dossier après le code appelle **SaveContentsSort**, les lignes dans le tableau renvoyé contenu apparaîtra dans l’ordre établi par **SaveContentsSort**.
  
Prendre en charge tous les fournisseurs de banque de messages **SaveContentsSort**; Il est acceptable pour les fournisseurs de banque de message renvoyer des MAPI_E_NO_SUPPORT à partir de la méthode **SaveContentsSort** . 
  
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[SSortOrderSet](ssortorderset.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)

