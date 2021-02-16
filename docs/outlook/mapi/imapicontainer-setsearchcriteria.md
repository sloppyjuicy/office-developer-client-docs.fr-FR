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
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427198"
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
  
> [in] Pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche. Si LA VALEUR NULL est passée dans le paramètre  _lpRestriction,_ les critères de recherche les plus récemment utilisés pour ce conteneur sont utilisés à nouveau. Null ne doit pas être transmis dans  _lpRestriction_ pour la première recherche dans un conteneur. 
    
 _lpContainerList_
  
> [in] Pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche. Si un client transmet la valeur NULL dans le paramètre  _lpContainerList,_ les identificateurs d’entrée utilisés le plus récemment pour rechercher ce conteneur sont utilisés pour la nouvelle recherche. Un client ne doit pas transmettre null dans  _lpContainerList_ pour la première recherche dans un conteneur. 
    
 _ulSearchFlags_
  
> [in] Masque de bits d’indicateurs qui contrôlent la façon dont la recherche est effectuée. Les indicateurs suivants peuvent être définies :
    
BACKGROUND_SEARCH 
  
> La recherche doit s’exécuter selon une priorité normale par rapport aux autres recherches. Cet indicateur ne peut pas être définie en même temps que l’FOREGROUND_SEARCH’indicateur.
    
FOREGROUND_SEARCH 
  
> La recherche doit s’exécuter avec une priorité élevée par rapport aux autres recherches. Cet indicateur ne peut pas être définie en même temps que l’BACKGROUND_SEARCH’indicateur.
    
NON_CONTENT_INDEXED_SEARCH
  
> La recherche ne doit pas utiliser l’indexation de contenu pour rechercher des entrées correspondantes. Cet indicateur n’est valide que pour les magasins Exchange.
    
RECURSIVE_SEARCH 
  
> La recherche doit inclure les conteneurs spécifiés dans le  _paramètre lpContainerList_ et tous leurs conteneurs enfants. Cet indicateur ne peut pas être définie en même temps que l’SHALLOW_SEARCH’indicateur. 
    
RESTART_SEARCH 
  
> La recherche doit être lancée s’il s’agit du premier appel à **SetSearchCriteria,** ou redémarré si la recherche est inactive. Cet indicateur ne peut pas être définie en même temps que l’STOP_SEARCH’indicateur.
    
SHALLOW_SEARCH 
  
> La recherche doit uniquement rechercher les entrées correspondantes dans les conteneurs spécifiés dans le _paramètre lpContainerList._ Cet indicateur ne peut pas être définie en même temps que l’RECURSIVE_SEARCH’indicateur. 
    
STOP_SEARCH 
  
> La recherche doit être arrêtée. Cet indicateur ne peut pas être définie en même temps que l’RESTART_SEARCH’indicateur.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les critères de recherche ont été correctement définis.
    
MAPI_E_TOO_COMPLEX 
  
> Le fournisseur de services ne prend pas en charge les critères de recherche spécifiés.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIContainer::SetSearchCriteria** établit des critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche. Un dossier de résultats de recherche contient des liens vers les messages qui répondent aux critères de recherche . les messages réels sont toujours stockés à leur emplacement d’origine. Les seules données uniques contenues dans un dossier de résultats de recherche sont sa table des matières. La table des matières d’un dossier de résultats de recherche contient le contenu fusionné de la magasin de messages après l’application de la restriction de recherche. 
  
Une opération de recherche ne fonctionne que sur cette table des matières fusionnée ; il ne recherche pas dans d’autres dossiers de résultats de recherche. Les résultats de la recherche retournent uniquement les messages qui correspondent aux critères de recherche . la hiérarchie de dossiers n’est pas renvoyée.
  
Le contrôle est renvoyé au client une fois la recherche terminée.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les conteneurs de carnet d’adresses établissent des critères de recherche en appliquant des restrictions à leurs tables de contenu. Pour plus d’informations sur les critères de recherche et les conteneurs de carnet d’adresses, voir [Implementing Advanced Searching](implementing-advanced-searching.md).
  
Vous devez prendre en charge les opérations d’ouverture, de copie, de déplacement et de suppression sur les messages dans les dossiers de résultats de recherche, et non sur le dossier de résultats de recherche lui-même. N’autorisez pas la création ou la copie de messages dans un dossier de résultats de recherche. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour rechercher des destinataires de message, définissez  _lpRestriction_ de façon à pointer vers une restriction de sous-objet avec le membre **ulSubObject** dans la structure [SSubRestriction](ssubrestriction.md) définie sur **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Pour rechercher des pièces jointes, définissez le membre **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Définissez **le membre lpRes** pour qu’il pointe vers une restriction de propriété qui décrit les critères de recherche pour les destinataires ou les pièces jointes. 
  
Par exemple, pour rechercher des pièces jointes dont l’extension est .mss, définissez **ulSubObject** sur **PR_MESSAGE_ATTACHMENTS** et **lpRes** sur une restriction de propriété qui correspond à **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) avec .mss.
  
La définition FOREGROUND_SEARCH’indicateur dans le  _paramètre ulSearchFlags_ peut entraîner une diminution des performances du système. 
  
Vous pouvez utiliser **SetSearchCriteria** pour modifier les critères de recherche d’une recherche déjà en cours. Vous pouvez spécifier de nouvelles restrictions, de nouvelles listes de dossiers à rechercher et une nouvelle priorité de recherche, telle que la mise à niveau d’une recherche vers une priorité plus élevée. Les modifications apportées à la priorité de recherche n’entraînent pas le redémarrage d’une recherche existante, mais d’autres modifications apportées aux critères de recherche le peuvent. 
  
Lorsque vous utilisez un dossier de résultats de recherche, vous pouvez supprimer le dossier ou le laisser ouvert pour une utilisation ultérieure. Si vous supprimez le dossier de résultats de recherche, seuls les liens de messages sont supprimés. Les messages réels restent dans leurs dossiers parents. 
  
Pour plus d’informations sur les dossiers de résultats de recherche, voir [Dossiers de recherche MAPI.](mapi-search-folders.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI utilise la méthode **IMAPIContainer::SetSearchCriteria** pour écrire des critères de recherche pour un dossier après qu’un utilisateur l’a modifié.  <br/> |
   
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

