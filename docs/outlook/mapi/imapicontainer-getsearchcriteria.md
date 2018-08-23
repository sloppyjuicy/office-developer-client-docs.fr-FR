---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579962"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Obtient les critères de recherche pour le conteneur.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé. Vous pouvez définir l’indicateur suivant :
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
 _lppRestriction_
  
> [out] Pointeur vers un pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si une application cliente passe NULL dans le paramètre _lppRestriction_ , **GetSearchCriteria** ne renvoie pas une structure **SRestriction** . 
    
 _lppContainerList_
  
> [out] Pointeur vers un pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche. Si un client passe NULL dans le paramètre _lppContainerList_ , **GetSearchCriteria** ne renvoie pas un tableau d’identificateurs d’entrée. 
    
 _lpulSearchState_
  
> [out] Pointeur vers un masque binaire composé des indicateurs utilisés pour indiquer l’état actuel de la recherche. Si un client passe NULL dans le paramètre _lpulSearchState_ , **GetSearchCriteria** ne renvoie aucun indicateur. Les indicateurs suivants peuvent être définis : 
    
SEARCH_FOREGROUND 
  
> La recherche doit être exécutée à priorité élevée par rapport à d’autres critères de recherche. Si cet indicateur n’est pas défini, la recherche s’exécute à une priorité normale par rapport à d’autres critères de recherche.
    
SEARCH_REBUILD 
  
> La recherche est en mode intensive du processeur de son fonctionnement, essayez de rechercher des messages qui correspondent aux critères. Si cet indicateur n’est pas défini, le composant intensive du processeur de l’opération de la recherche est. Cet indicateur n’a une signification uniquement si la recherche est active (c'est-à-dire, si l’indicateur SEARCH_RUNNING est défini).
    
SEARCH_RECURSIVE 
  
> Recherche dans les conteneurs spécifiés et tous les conteneurs de leurs enfants pour la correspondance des entrées de la recherche. Si cet indicateur n’est pas défini, que les conteneurs explicitement incluses dans le dernier appel à la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) sont recherchés. 
    
SEARCH_RUNNING 
  
> La recherche est active et la table des matières du conteneur est mis à jour pour refléter les modifications de la banque de messages ou le carnet d’adresses. Si cet indicateur n’est pas défini, la recherche est inactive et la table des matières est statique.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Les critères de recherche a été obtenue avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.
    
MAPI_E_NOT_INITIALIZED 
  
> Critères de recherche ont été établies jamais pour le conteneur.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetSearchCriteria** Obtient les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Vous créez des critères de recherche en appelant la méthode de **IMAPIContainer::SetSearchCriteria** d’un conteneur. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Conteneurs de carnet d’adresses peuvent prendre en charge **GetSearchCriteria** uniquement s’ils fournissent les fonctionnalités de recherche avancée associées à la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Pour plus d’informations sur la façon d’implémenter la fonctionnalité de recherche avancée pour les conteneurs de carnet d’adresses, voir [Implémentation de la recherche avancée](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notes aux appelants

Lorsque vous avez terminé avec les structures de données indiqués par les paramètres _lppRestriction_ et _lppContainerList_ , appelez [MAPIFreeBuffer](mapifreebuffer.md) qu’une seule fois pour chaque structure doit être publié. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer::GetSearchCriteria** pour obtenir des critères de recherche à partir d’un dossier à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

