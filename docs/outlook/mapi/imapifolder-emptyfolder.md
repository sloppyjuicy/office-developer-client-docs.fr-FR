---
title: IMAPIFolderEmptyFolder
description: IMAPIFolderEmptyFolder supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.EmptyFolder
api_type:
- COM
ms.assetid: 4cfcb498-9182-4906-bd6f-d9bc387bc88b
ms.openlocfilehash: 363cb97f2fbbda377b4824f86350b248bcf4d0e7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812214"
---
# <a name="imapifolderemptyfolder"></a>IMAPIFolder::EmptyFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime tous les messages et sous-dossiers d’un dossier sans supprimer le dossier lui-même.
  
```cpp
HRESULT EmptyFolder(
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont le dossier est vidé. Les indicateurs suivants peuvent être définis :
    
DEL_ASSOCIATED 
  
> Supprime tous les sous-dossiers, y compris les sous-dossiers qui contiennent des messages avec le contenu associé. L’indicateur DEL_ASSOCIATED a une signification uniquement pour le dossier de niveau supérieur sur lequel l’appel agit.
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux supprimés de manière réversible.
    
FOLDER_DIALOG 
  
> Affiche un indicateur de progression pendant que l’opération se poursuit.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été vidé avec succès.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais le dossier n’a pas été complètement vidé. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::EmptyFolder** supprime tout le contenu d’un dossier sans supprimer le dossier lui-même. 
  
Pendant un appel **EmptyFolder** , les messages envoyés ne sont pas supprimés. 
  
Le contenu associé à un dossier inclut des messages qui sont utilisés pour décrire les vues, les règles, les formulaires personnalisés et le stockage de solutions personnalisées, et peuvent également inclure des définitions de formulaires. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

N’appelez pas la méthode [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour les messages du dossier qui ont été envoyés. Les messages envoyés ne sont pas supprimés. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**EmptyFolder** a correctement vidé le dossier. |S_OK  <br/> |
|**EmptyFolder** n’a pas pu vider complètement le dossier. |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder** n’a pas pu se terminer. |Toute valeur d’erreur  <br/> |
   
Lorsque **EmptyFolder** ne parvient pas à se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **EmptyFolder** a peut-être pu supprimer une partie du contenu du dossier avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::EmptyFolder** pour supprimer le contenu du dossier spécifié. |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

