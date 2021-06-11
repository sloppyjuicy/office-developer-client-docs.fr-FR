---
title: IMAPIFolderDeleteFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a476607927f3563ede94a04ccfe4f7a3749c978e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417405"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un sous-foldeur.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parameters

 _cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-folder à supprimer.
    
 _ulUIParam_
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. Le _paramètre ulUIParam_ est ignoré, sauf si l’FOLDER_DIALOG est définie dans _le paramètre ulFlags._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le  _paramètre lpProgress est_ ignoré, sauf si l’FOLDER_DIALOG est définie dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la suppression du sous-folder. Les indicateurs suivants peuvent être définies :
    
DEL_FOLDERS 
  
> Tous les sous-fichiers du sous-fichier pointé par  _lpEntryID_ doivent être supprimés. 
    
DEL_MESSAGES 
  
> Tous les messages dans le sous-fichier pointé par  _lpEntryID_ doivent être supprimés. 
    
FOLDER_DIALOG 
  
> Un indicateur de progression doit être affiché pendant la progression de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été supprimé avec succès.
    
MAPI_E_HAS_FOLDERS 
  
> Le sous-fichier en cours de suppression contient des sous-DEL_FOLDERS et l’indicateur de DEL_FOLDERS n’a pas été définie. Les sous-fichiers n’ont pas été supprimés.
    
MAPI_E_HAS_MESSAGES 
  
> Le sous-fichier supprimé contient des messages et l’DEL_MESSAGES n’a pas été définie. Le sous-fichier n’a pas été supprimé.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été supprimées avec succès. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::D eleteFolder** supprime un sous-ensemble. Par défaut, **DeleteFolder** fonctionne uniquement sur les dossiers vides, mais vous pouvez l’utiliser avec succès sur des dossiers non vides en fixant deux indicateurs : DEL_FOLDERS et DEL_MESSAGES. Seuls les dossiers vides ou les dossiers qui définissent les indicateurs DEL_FOLDERS et DEL_MESSAGES sur l’appel **DeleteFolder** peuvent être supprimés. DEL_FOLDERS tous les sous-dossiers du dossier peuvent être supprimés ; DEL_MESSAGES tous les messages du dossier peuvent être supprimés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs dossiers, effectuez l’opération aussi complètement que possible pour chaque dossier. Parfois, l’un des dossiers à supprimer n’existe pas ou a été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteFolder a** supprimé tous les messages et sous-fichiers avec succès.  <br/> |S_OK  <br/> |
|**DeleteFolder n’a** pas pu supprimer tous les messages et sous-fichiers.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder n’a** pas pu se terminer.  <br/> |Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteFolder ne** parvient pas à se terminer, ne supposez pas qu’aucun travail n’a été effectué. **DeleteFolder a** peut-être pu supprimer un ou plusieurs des messages et sous-fichiers avant de rencontrer l’erreur. 
  
Si un ou plusieurs sous-fichiers ne peuvent pas être supprimés, **DeleteFolder** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du fournisseur de magasins de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise **la méthode IMAPIFolder::D eleteFolder** pour supprimer des dossiers.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

