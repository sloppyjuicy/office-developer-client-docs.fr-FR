---
title: IMAPIContainerSetSearchCriteria
description: IMAPIContainerSetSearchCriteria établit des critères de recherche pour le conteneur. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
ms.openlocfilehash: 5c7fef282455c85e932b1633c78093db3ca8cead
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817878"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit des critères de recherche pour le conteneur.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si NULL est passé dans le paramètre _lpRestriction_ , les critères de recherche qui ont été utilisés le plus récemment pour ce conteneur sont à nouveau utilisés. NULL ne doit pas être passé dans  _lpRestriction_ pour la première recherche dans un conteneur. 
    
 _lpContainerList_
  
> [in] Pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche. Si un client passe null dans le paramètre _lpContainerList_ , les identificateurs d’entrée utilisés le plus récemment pour rechercher ce conteneur sont utilisés pour la nouvelle recherche. Un client ne doit pas passer null dans  _lpContainerList_ pour la première recherche dans un conteneur. 
    
 _ulSearchFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent la façon dont la recherche est effectuée. Les indicateurs suivants peuvent être définis :
    
BACKGROUND_SEARCH 
  
> La recherche doit s’exécuter en priorité normale par rapport aux autres recherches. Cet indicateur ne peut pas être défini en même temps que l’indicateur FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> La recherche doit s’exécuter en priorité par rapport aux autres recherches. Cet indicateur ne peut pas être défini en même temps que l’indicateur BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> La recherche ne doit pas utiliser l’indexation de contenu pour rechercher les entrées correspondantes. Cet indicateur n’est valide que pour Exchange magasins.
    
RECURSIVE_SEARCH 
  
> La recherche doit inclure les conteneurs spécifiés dans le paramètre _lpContainerList_ et tous leurs conteneurs enfants. Cet indicateur ne peut pas être défini en même temps que l’indicateur SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> La recherche doit être lancée s’il s’agit du premier appel à **SetSearchCriteria** ou redémarrée si la recherche est inactive. Cet indicateur ne peut pas être défini en même temps que l’indicateur STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> La recherche doit uniquement rechercher les entrées correspondantes dans les conteneurs spécifiés dans le paramètre _lpContainerList_ . Cet indicateur ne peut pas être défini en même temps que l’indicateur RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> La recherche doit être arrêtée. Cet indicateur ne peut pas être défini en même temps que l’indicateur RESTART_SEARCH.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche ont été correctement définis.
    
MAPI_E_TOO_COMPLEX 
  
> Le fournisseur de services ne prend pas en charge les critères de recherche spécifiés.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::SetSearchCriteria** établit des critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche ; les messages réels sont toujours stockés dans leurs emplacements d’origine. Les seules données uniques contenues dans un dossier de résultats de recherche sont sa table de contenu. La table de contenu d’un dossier de résultats de recherche contient le contenu fusionné du magasin de messages une fois la restriction de recherche appliquée. 
  
Une opération de recherche fonctionne uniquement sur cette table de contenu fusionnée ; il ne recherche pas dans d’autres dossiers de résultats de recherche. Les résultats de la recherche retournent uniquement les messages qui correspondent aux critères de recherche ; la hiérarchie des dossiers n’est pas retournée.
  
Le contrôle est retourné au client une fois la recherche terminée.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les conteneurs de carnets d’adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu. Pour plus d’informations sur les critères de recherche et les conteneurs de carnets [d’adresses, consultez Implémentation d’une recherche avancée](implementing-advanced-searching.md).
  
Vous devez prendre en charge les opérations d’ouverture, de copie, de déplacement et de suppression sur les messages dans les dossiers de résultats de recherche, et non sur le dossier de résultats de recherche lui-même. N’autorisez pas la création ou la copie de messages dans un dossier de résultats de recherche. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour rechercher des destinataires de message, définissez  _lpRestriction_ pour qu’il pointe vers une restriction de sous-objet avec le membre **ulSubObject** dans la structure [SSubRestriction](ssubrestriction.md) défini sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Pour rechercher des pièces jointes, définissez le membre **ulSubObject** **sur PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Définissez le membre **lpRes** pour qu’il pointe vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes. 
  
Par exemple, pour rechercher les pièces jointes de fichier qui ont l’extension .mss, définissez **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** et **lpRes** sur une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) avec .mss.
  
La définition de l’indicateur FOREGROUND_SEARCH dans le paramètre _ulSearchFlags_ peut entraîner une diminution des performances du système. 
  
Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d’une recherche déjà en cours. Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de recherche, comme la mise à niveau d’une recherche vers une priorité plus élevée. Les modifications apportées à la priorité de recherche n’entraînent pas le redémarrage d’une recherche existante, mais d’autres modifications apportées aux critères de recherche peuvent le faire. 
  
Lorsque vous utilisez un dossier de résultats de recherche, vous pouvez supprimer le dossier ou le laisser ouvert pour une utilisation ultérieure. Si vous supprimez le dossier de résultats de recherche, seuls les liens de message sont supprimés. Les messages réels restent dans leurs dossiers parents. 
  
Pour plus d’informations sur les dossiers de résultats de recherche, consultez [Dossiers de recherche MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer::SetSearchCriteria** pour écrire des critères de recherche pour un dossier après qu’un utilisateur l’a modifié. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

