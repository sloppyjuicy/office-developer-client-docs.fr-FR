---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 93fb82c6274a1703376d7a9e15f37088e132dc23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585891"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit les critères de recherche pour le conteneur.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si NULL est indiqué dans le paramètre _lpRestriction_ , les critères de recherche qui ont été utilisés récemment pour ce conteneur sont utilisés à nouveau. NULL ne doit pas être passé dans _lpRestriction_ pour la première recherche dans un conteneur. 
    
 _lpContainerList_
  
> [in] Pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche. Si un client passe NULL dans le paramètre _lpContainerList_ , les identificateurs d’entrée plus récemment utilisés pour rechercher ce conteneur sont utilisés pour la recherche. Un client ne doit pas passer NULL dans _lpContainerList_ pour la première recherche dans un conteneur. 
    
 _ulSearchFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent la façon dont la recherche est effectuée. Les indicateurs suivants peuvent être définis :
    
BACKGROUND_SEARCH 
  
> La recherche doit être exécutée à une priorité normale par rapport à d’autres critères de recherche. Cet indicateur ne peut pas être défini en même temps que l’indicateur FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> La recherche doit être exécutée à priorité élevée par rapport à d’autres critères de recherche. Cet indicateur ne peut pas être défini en même temps que l’indicateur BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> La recherche ne doit pas utiliser l’indexation de contenu pour rechercher des entrées correspondantes. Cet indicateur n’est valide pour les banques Exchange.
    
RECURSIVE_SEARCH 
  
> La recherche doit inclure les conteneurs spécifiés dans le paramètre _lpContainerList_ et tous les conteneurs de leurs enfants. Cet indicateur ne peut pas être défini en même temps que l’indicateur SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> La recherche doit être lancée s’il s’agit du premier appel à **SetSearchCriteria**ou redémarrée si la recherche est inactive. Cet indicateur ne peut pas être défini en même temps que l’indicateur STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> La recherche porte uniquement dans les conteneurs spécifiés dans le paramètre _lpContainerList_ pour la correspondance des entrées. Cet indicateur ne peut pas être défini en même temps que l’indicateur RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> La recherche doit être arrêtée. Cet indicateur ne peut pas être défini en même temps que l’indicateur RESTART_SEARCH.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche a été défini.
    
MAPI_E_TOO_COMPLEX 
  
> Le fournisseur de services ne gère pas les critères de recherche spécifiée.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::SetSearchCriteria** établit les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche ; les messages réels sont toujours stockés dans leurs emplacements d’origine. Les données uniquement uniques qui se trouve dans un dossier de résultats de recherche sont sa table des matières. La table des matières d’un dossier de résultats de recherche a le contenu de la banque de messages fusionné après que la restriction de recherche a été appliquée. 
  
Une opération de recherche fonctionne uniquement sur ce tableau contenu fusionné ; Il ne recherche pas les autres dossiers de résultats de recherche. Les résultats de recherche retournent uniquement les messages qui correspondent aux critères de recherche ; la hiérarchie de dossiers n’est pas retournée.
  
Contrôle est renvoyé au client lors de la recherche est terminée.
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Conteneurs de carnet d’adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu. Pour plus d’informations sur les critères de recherche et les conteneurs de carnet d’adresses, voir [Implémentation de la recherche avancée](implementing-advanced-searching.md).
  
Doit prendre en charge open, copier, déplacer et supprimer des opérations sur les messages dans les dossiers de résultats de recherche, et non sur le dossier de résultats de recherche proprement dite. Ne pas autoriser les messages créés dans ou copiées dans un dossier de résultats de recherche. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour rechercher des destinataires du message, la valeur _lpRestriction_ pour pointer vers une restriction sous-objet avec le membre **ulSubObject** de la structure [SSubRestriction](ssubrestriction.md) défini sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Pour rechercher des pièces jointes, la valeur du membre **ulSubObject** **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Définissez le membre **lpRes** pour pointer vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes. 
  
Par exemple, pour rechercher des pièces jointes ayant l’extension .mss, la valeur **ulSubObject** **PR_MESSAGE_ATTACHMENTS** et **lpRes** à une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) avec. mss.
  
Définition de l’indicateur FOREGROUND_SEARCH dans le paramètre _ulSearchFlags_ peut entraîner une diminution des performances du système. 
  
Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d’une recherche en cours. Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de la recherche, tels que la mise à niveau d’une recherche à une priorité plus élevée. Modifications apportées à la priorité de la recherche ne provoquent pas une recherche existante à redémarrer, mais les autres modifications apportées aux critères de recherche peuvent. 
  
Lorsque vous êtes à l’aide d’un dossier de résultats de recherche, vous pouvez supprimer le dossier ou laissez-le restent ouverts pour une utilisation ultérieure. Si vous ne supprimez pas le dossier de résultats de recherche, uniquement les liaisons de message sont supprimés. Les messages restent dans leurs dossiers parents. 
  
Pour plus d’informations sur les dossiers des résultats de recherche, voir [Dossiers de recherche MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer::SetSearchCriteria** pour écrire les critères de recherche pour un dossier après qu’un utilisateur a le modifiée.  <br/> |
   
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

