---
title: IMAPIContainerGetSearchCriteria
description: IMAPIContainerGetSearchCriteria obtient les critères de recherche pour le conteneur. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
ms.openlocfilehash: 8abb135bd20b39cb90bafe056d5370c3eac4376a
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65818186"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient les critères de recherche pour le conteneur.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le type des chaînes passées. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les chaînes passées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.
    
 _lppRestriction_
  
> [out] Pointeur vers un pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si une application cliente passe null dans le paramètre _lppRestriction_ , **GetSearchCriteria** ne retourne pas de structure **SRestriction** . 
    
 _lppContainerList_
  
> [out] Pointeur vers un pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche. Si un client passe null dans le paramètre _lppContainerList_ , **GetSearchCriteria** ne retourne pas de tableau d’identificateurs d’entrée. 
    
 _lpulSearchState_
  
> [out] Pointeur vers un masque de bits d’indicateurs utilisé pour indiquer l’état actuel de la recherche. Si un client passe null dans le paramètre _lpulSearchState_ , **GetSearchCriteria** ne retourne aucun indicateur. Les indicateurs suivants peuvent être définis : 
    
SEARCH_FOREGROUND 
  
> La recherche doit s’exécuter en priorité par rapport aux autres recherches. Si cet indicateur n’est pas défini, la recherche s’exécute en priorité normale par rapport aux autres recherches.
    
SEARCH_REBUILD 
  
> La recherche est en mode intensif du processeur de son opération, en essayant de localiser les messages qui correspondent aux critères. Si cet indicateur n’est pas défini, la partie gourmande en processeur de l’opération de recherche est terminée. Cet indicateur a une signification uniquement si la recherche est active (autrement dit, si l’indicateur SEARCH_RUNNING est défini).
    
SEARCH_RECURSIVE 
  
> La recherche recherche dans les conteneurs spécifiés et tous leurs conteneurs enfants les entrées correspondantes. Si cet indicateur n’est pas défini, seuls les conteneurs explicitement inclus dans le dernier appel à la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) sont recherchés. 
    
SEARCH_RUNNING 
  
> La recherche est active et la table du contenu du conteneur est mise à jour pour refléter les modifications apportées au magasin de messages ou au carnet d’adresses. Si cet indicateur n’est pas défini, la recherche est inactive et la table des matières est statique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche ont été obtenus avec succès.
    
MAPI_E_BAD_CHARWIDTH 
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Les critères de recherche n’ont jamais été établis pour le conteneur.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::GetSearchCriteria** obtient les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Vous créez des critères de recherche en appelant la méthode **IMAPIContainer::SetSearchCriteria** d’un conteneur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les conteneurs de carnets d’adresses peuvent avoir besoin de prendre en charge **GetSearchCriteria** uniquement s’ils fournissent les fonctionnalités de recherche avancées associées à la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Pour plus d’informations sur la façon d’implémenter la fonctionnalité de recherche avancée pour les conteneurs de carnets d’adresses, consultez [Implémentation de la recherche avancée](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Lorsque vous avez terminé les structures de données pointées par les paramètres  _lppRestriction_ et  _lppContainerList_ , appelez [MAPIFreeBuffer](mapifreebuffer.md) une fois pour chaque structure à libérer. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer::GetSearchCriteria** pour obtenir des critères de recherche à partir d’un dossier à afficher. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[PidTagSearch Canonical, propriété](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

