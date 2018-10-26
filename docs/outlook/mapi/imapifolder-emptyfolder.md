---
title: IMAPIFolderEmptyFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 287577babc9a40b771aa9917211ba5dcbf8190ad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584939"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime tous les messages et les sous-dossiers d’un dossier sans supprimer le dossier proprement dit.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est vidé. Les indicateurs suivants peuvent être définis :
    
DEL_ASSOCIATED 
  
> Supprime tous les sous-dossiers, y compris les sous-dossiers qui contiennent des messages avec contenu associé. L’indicateur DEL_ASSOCIATED a de signification seulement pour l’appel agit sur le dossier de niveau supérieur.
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux récupérable.
    
FOLDER_DIALOG 
  
> Affiche un indicateur de progression pendant que l’opération s’effectue.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été vidé avec succès.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais le dossier n’a pas été vidé complètement. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::EmptyFolder** supprime tout contenu d’un dossier sans supprimer le dossier proprement dit. 
  
Pendant un appel **EmptyFolder** , les messages envoyés ne sont pas supprimés. 
  
Contenu associé d’un dossier comprennent les messages qui sont utilisés pour décrire les affichages, les règles, les formulaires personnalisés et du stockage des solutions personnalisées et peuvent également inclure des définitions de formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

N’appelez pas la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour les messages qui ont été envoyés dans le dossier. Les messages envoyés ne sont pas supprimés. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**EmptyFolder** a vidé avec succès le dossier.  <br/> |S_OK  <br/> |
|**EmptyFolder** n’a pas pu vider entièrement le dossier.  <br/> |MAPI_W_PARTIAL_COMPLETION SE PRODUIT  <br/> |
|**EmptyFolder** n’a pas pu terminer.  <br/> |Une valeur d’erreur  <br/> |
   
Lorsque **EmptyFolder** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée. **EmptyFolder** peut-être en mesure de supprimer le contenu du dossier avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::EmptyFolder** pour supprimer le contenu du dossier spécifié.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

