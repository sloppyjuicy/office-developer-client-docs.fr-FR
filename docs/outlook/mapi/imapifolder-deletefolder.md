---
title: IMAPIFolderDeleteFolder
description: IMAPIFolderDeleteFolder supprime un sous-dossier. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.DeleteFolder
api_type:
- COM
ms.assetid: 6c3e883c-80c0-4eda-8f81-8277d933a74b
ms.openlocfilehash: 2f2a43fb6f517c4ede2f4e1e268cf4ed0f966ee7
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817255"
---
# <a name="imapifolderdeletefolder"></a>IMAPIFolder::DeleteFolder

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un sous-dossier.
  
```cpp
HRESULT DeleteFolder(
  ULONG_PTR cbEntryID,
  LPENTRYID lpEntryID,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-dossier à supprimer.
    
 _ulUIParam_
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur FOLDER_DIALOG est défini dans  _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la suppression du sous-dossier. Les indicateurs suivants peuvent être définis :
    
DEL_FOLDERS 
  
> Tous les sous-dossiers du sous-dossier pointés par  _lpEntryID_ doivent être supprimés. 
    
DEL_MESSAGES 
  
> Tous les messages du sous-dossier pointés par  _lpEntryID_ doivent être supprimés. 
    
FOLDER_DIALOG 
  
> Un indicateur de progression doit être affiché pendant que l’opération se poursuit.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été supprimé avec succès.
    
MAPI_E_HAS_FOLDERS 
  
> Le sous-dossier supprimé contient des sous-dossiers et l’indicateur DEL_FOLDERS n’a pas été défini. Les sous-dossiers n’ont pas été supprimés.
    
MAPI_E_HAS_MESSAGES 
  
> Le sous-dossier supprimé contient des messages et l’indicateur DEL_MESSAGES n’a pas été défini. Le sous-dossier n’a pas été supprimé.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais toutes les entrées n’ont pas été supprimées avec succès. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::D eleteFolder** supprime un sous-dossier. Par défaut, **DeleteFolder** fonctionne uniquement sur les dossiers vides, mais vous pouvez l’utiliser correctement sur des dossiers non vides en définissant deux indicateurs : DEL_FOLDERS et DEL_MESSAGES. Seuls les dossiers vides ou les dossiers qui définissent les indicateurs DEL_FOLDERS et DEL_MESSAGES sur l’appel **DeleteFolder** peuvent être supprimés. DEL_FOLDERS permet de supprimer tous les sous-dossiers du dossier ; DEL_MESSAGES permet de supprimer tous les messages du dossier. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs dossiers, effectuez l’opération aussi complètement que possible pour chaque dossier. Parfois, l’un des dossiers à supprimer n’existe pas ou a été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, à moins qu’une défaillance ne soit hors de votre contrôle, comme un manque de mémoire, un manque d’espace disque ou une altération du magasin de messages.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteFolder** a supprimé avec succès chaque message et sous-dossier. |S_OK  <br/> |
|**DeleteFolder** n’a pas réussi à supprimer tous les messages et sous-dossiers. |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** n’a pas pu se terminer. |Toute valeur d’erreur sauf MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteFolder** ne peut pas se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **DeleteFolder** a peut-être pu supprimer un ou plusieurs messages et sous-dossiers avant de rencontrer l’erreur. 
  
Si un ou plusieurs sous-dossiers ne peuvent pas être supprimés, **DeleteFolder** retourne MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du fournisseur de magasin de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::D eleteFolder** pour supprimer des dossiers. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

