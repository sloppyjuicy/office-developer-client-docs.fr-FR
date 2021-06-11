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
ms.openlocfilehash: 4ca828c3e03cbff886230f2af63485f7b15e8b35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416782"
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. Le _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG est définie dans _le paramètre ulFlags._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans le paramètre _ulFlags._ 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le dossier est vidé. Les indicateurs suivants peuvent être définies :
    
DEL_ASSOCIATED 
  
> Supprime tous les sous-fichiers, y compris les sous-fichiers qui contiennent des messages avec le contenu associé. L DEL_ASSOCIATED’indicateur de niveau supérieur a une signification uniquement pour le dossier de niveau supérieur sur qui l’appel agit.
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris les messages supprimés (supprimés de manière temporaire).
    
FOLDER_DIALOG 
  
> Affiche un indicateur de progression pendant la progression de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier a été vidé.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais le dossier n’a pas été complètement vidé. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::EmptyFolder** supprime tout le contenu d’un dossier sans supprimer le dossier lui-même. 
  
Pendant un **appel EmptyFolder,** les messages envoyés ne sont pas supprimés. 
  
Le contenu associé à un dossier inclut des messages qui sont utilisés pour décrire les affichages, les règles, les formulaires personnalisés et le stockage de solutions personnalisées, et peut également inclure des définitions de formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

N’appelez [pas la méthode IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) pour les messages dans le dossier qui ont été envoyés. Les messages envoyés ne sont pas supprimés. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**EmptyFolder a** correctement vidé le dossier.  <br/> |S_OK  <br/> |
|**EmptyFolder n’a** pas pu vider complètement le dossier.  <br/> |MAPI_W_PARTIAL_COMPLETION  <br/> |
|**EmptyFolder n’a** pas pu se terminer.  <br/> |Toute valeur d’erreur  <br/> |
   
Lorsque **EmptyFolder ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué. **EmptyFolder a** peut-être pu supprimer une partie du contenu du dossier avant de rencontrer l’erreur. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnEmptyFolder  <br/> |MFCMAPI utilise la **méthode IMAPIFolder::EmptyFolder** pour supprimer le contenu du dossier spécifié.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMsgStore::AbortSubmit](imsgstore-abortsubmit.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

