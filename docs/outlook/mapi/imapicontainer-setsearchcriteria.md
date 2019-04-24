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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350966"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit les critères de recherche pour le conteneur.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpRestriction_
  
> dans Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si la valeur NULL est transmise au paramètre _lpRestriction_ , les critères de recherche utilisés le plus récemment pour ce conteneur sont réutilisés. NULL ne doit pas être passé dans _lpRestriction_ pour la première recherche dans un conteneur. 
    
 _lpContainerList_
  
> dans Pointeur vers un tableau d'identificateurs d'entrée qui représentent des conteneurs à inclure dans la recherche. Si un client transmet NULL dans le paramètre _lpContainerList_ , les identificateurs d'entrée utilisés le plus récemment pour rechercher ce conteneur sont utilisés pour la nouvelle recherche. Un client ne doit pas transmettre NULL dans _lpContainerList_ pour la première recherche dans un conteneur. 
    
 _ulSearchFlags_
  
> dans Masque de des indicateurs qui contrôlent le mode d'exécution de la recherche. Les indicateurs suivants peuvent être définis:
    
BACKGROUND_SEARCH 
  
> La recherche doit être exécutée à une priorité normale par rapport à d'autres recherches. Cet indicateur ne peut pas être défini en même temps que l'indicateur FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> La recherche doit s'exécuter à un niveau de priorité élevé par rapport à d'autres recherches. Cet indicateur ne peut pas être défini en même temps que l'indicateur BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> La recherche ne doit pas utiliser l'indexation de contenu pour rechercher des entrées correspondantes. Cet indicateur est valide uniquement pour les banques Exchange.
    
RECURSIVE_SEARCH 
  
> La recherche doit inclure les conteneurs spécifiés dans le paramètre _lpContainerList_ et tous leurs conteneurs enfants. Cet indicateur ne peut pas être défini en même temps que l'indicateur SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> La recherche doit être lancée s'il s'agit du premier appel à **SetSearchCriteria**ou si la recherche est inactive. Cet indicateur ne peut pas être défini en même temps que l'indicateur STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> La recherche doit rechercher uniquement dans les conteneurs spécifiés dans le paramètre _lpContainerList_ pour les entrées correspondantes. Cet indicateur ne peut pas être défini en même temps que l'indicateur RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> La recherche doit être arrêtée. Cet indicateur ne peut pas être défini en même temps que l'indicateur RESTART_SEARCH.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche ont été correctement définis.
    
MAPI_E_TOO_COMPLEX 
  
> Le fournisseur de services ne prend pas en charge les critères de recherche spécifiés.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer:: SetSearchCriteria** établit les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche; les messages réels sont toujours stockés dans leurs emplacements d'origine. Les seules données uniques contenues dans un dossier de résultats de recherche est sa table des matières. La table de contenu d'un dossier Search-Results a le contenu fusionné de la Banque de messages une fois que la restriction de recherche a été appliquée. 
  
Une opération de recherche ne fonctionne que sur cette table de contenu fusionné; il ne recherche pas dans d'autres dossiers de résultats de recherche. Les résultats de la recherche renvoient uniquement les messages qui correspondent aux critères de recherche; la hiérarchie de dossiers n'est pas renvoyée.
  
Le contrôle est renvoyé au client lorsque la recherche est terminée.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les conteneurs du carnet d'adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu. Pour plus d'informations sur les critères de recherche et les conteneurs du carnet d'adresses, consultez la rubrique implémentation de la [recherche avancée](implementing-advanced-searching.md).
  
Vous devez prendre en charge les opérations d'ouverture, de copie, de déplacement et de suppression des messages dans les dossiers de résultats de recherche, et non dans le dossier de résultats de recherche lui-même. Ne pas autoriser la création ou la copie de messages dans un dossier de résultats de recherche. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour rechercher des destinataires de message, définissez _lpRestriction_ de sorte qu'il pointe vers une restriction de sous-objet avec le membre **ulSubObject** dans la structure [SSubRestriction](ssubrestriction.md) définie sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Pour rechercher des pièces jointes, définissez le membre **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Définissez le membre **lpRes** de sorte qu'il pointe vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes. 
  
Par exemple, pour rechercher des pièces jointes portant l'extension. MSS, définissez **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** et **lpRes** sur une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) avec. MSS.
  
La définition de l'indicateur FOREGROUND_SEARCH dans le paramètre _ulSearchFlags_ peut entraîner une diminution des performances du système. 
  
Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d'une recherche déjà en cours. Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de recherche, telle que la mise à niveau d'une recherche vers une priorité plus élevée. Les modifications apPortées à la priorité de recherche ne provoquent pas le redémarrage d'une recherche existante, mais d'autres modifications des critères de recherche peuvent. 
  
Lorsque vous utilisez un dossier Search-Results, vous pouvez supprimer le dossier ou le laisser ouvert en vue d'une utilisation ultérieure. Si vous supprimez le dossier Search-Results, seuls les liens de message sont supprimés. Les messages réels restent dans leurs dossiers parents. 
  
Pour plus d'informations sur les dossiers de résultats de recherche, consultez la rubrique [MAPI Search Folders](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer:: SetSearchCriteria** pour écrire des critères de recherche pour un dossier après qu'un utilisateur l'a modifié.  <br/> |
   
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

