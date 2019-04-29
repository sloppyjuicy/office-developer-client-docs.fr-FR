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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412022"
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
  
> dans Masque de bits des indicateurs qui contrôle le type des chaînes transmises. L'indicateur suivant peut être défini:
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
 _lppRestriction_
  
> remarquer Pointeur vers un pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si une application cliente transmet NULL dans le paramètre _lppRestriction_ , **GetSearchCriteria** ne renvoie pas une structure **SRestriction** . 
    
 _lppContainerList_
  
> remarquer Pointeur vers un pointeur vers un tableau d'identificateurs d'entrée qui représentent des conteneurs à inclure dans la recherche. Si un client transmet NULL dans le paramètre _lppContainerList_ , **GetSearchCriteria** ne renvoie pas un tableau d'identificateurs d'entrée. 
    
 _lpulSearchState_
  
> remarquer Pointeur vers un masque de des indicateurs utilisés pour indiquer l'état actuel de la recherche. Si un client transmet NULL dans le paramètre _lpulSearchState_ , **GetSearchCriteria** ne renvoie aucun indicateur. Les indicateurs suivants peuvent être définis: 
    
SEARCH_FOREGROUND 
  
> La recherche doit s'exécuter à un niveau de priorité élevé par rapport à d'autres recherches. Si cet indicateur n'est pas défini, la recherche s'exécute à une priorité normale par rapport à d'autres recherches.
    
SEARCH_REBUILD 
  
> La recherche est en mode intensif du processeur de son fonctionnement, tentant de localiser les messages correspondant aux critères. Si cet indicateur n'est pas défini, la partie gourmande en ressources du processeur de l'opération de recherche est terminée. Cet indicateur n'a de sens que si la recherche est active (autrement dit, si l'indicateur SEARCH_RUNNING est défini).
    
SEARCH_RECURSIVE 
  
> La recherche examine les conteneurs spécifiés et tous leurs conteneurs enfants pour les entrées correspondantes. Si cet indicateur n'est pas défini, seuls les conteneurs inclus explicitement dans le dernier appel à la méthode [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) sont recherchés. 
    
SEARCH_RUNNING 
  
> La recherche est active et la table des matières du conteneur est mise à jour pour refléter les modifications apportées à la Banque de messages ou au carnet d'adresses. Si cet indicateur n'est pas défini, la recherche est inactive et la table des matières est statique.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche ont été obtenus.
    
MAPI_E_BAD_CHARWIDTH 
  
> L'indicateur MAPI_UNICODE a été défini et l'implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n'a pas été défini et l'implémentation prend en charge uniquement Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Les critères de recherche n'ont jamais été établis pour le conteneur.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer:: GetSearchCriteria** obtient les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Vous créez des critères de recherche en appelant la méthode **IMAPIContainer:: SetSearchCriteria** d'un conteneur. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les conteneurs du carnet d'adresses peuvent avoir besoin de prendre en charge **GetSearchCriteria** uniquement s'ils fournissent les fonctionnalités de recherche avancées associées à la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Pour plus d'informations sur la façon d'implémenter la fonctionnalité de recherche avancée pour les conteneurs du carnet d'adresses, consultez la rubrique implémentation de la [recherche avancée](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Une fois que vous avez terminé avec les structures de données auxquelles pointe les paramètres _lppRestriction_ et _LppContainerList_ , appelez [MAPIFreeBuffer](mapifreebuffer.md) une fois pour chaque structure à publier. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer:: GetSearchCriteria** pour obtenir des critères de recherche à partir d'un dossier à afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriété canonique PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

