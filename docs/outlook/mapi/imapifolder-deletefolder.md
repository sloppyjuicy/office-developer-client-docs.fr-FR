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
ms.openlocfilehash: 02815c60b6bfc9809871af19e922913622588fc9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584316"
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du sous-dossier à supprimer.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur FOLDER_DIALOG est défini dans _ulFlags_.
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la suppression du sous-dossier. Les indicateurs suivants peuvent être définis :
    
DEL_FOLDERS 
  
> Tous les sous-dossiers du sous-dossier désignés par _lpEntryID_ doivent être supprimés. 
    
DEL_MESSAGES 
  
> Tous les messages dans le sous-dossier désignés par _lpEntryID_ doivent être supprimés. 
    
FOLDER_DIALOG 
  
> Un indicateur de progression doit s’afficher lorsque l’opération se poursuit.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le dossier spécifié a été supprimé.
    
MAPI_E_HAS_FOLDERS 
  
> Le sous-dossier en cours de suppression contient des sous-dossiers et l’indicateur DEL_FOLDERS n’a pas été défini. Les sous-dossiers n’ont pas été supprimés.
    
MAPI_E_HAS_MESSAGES 
  
> Le sous-dossier en cours de suppression contient des messages et l’indicateur DEL_MESSAGES n’a pas été défini. Le sous-dossier n’a pas été supprimé.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas toutes les entrées ont été supprimés. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::DeleteFolder** supprime un sous-dossier. Par défaut, **DeleteFolder** fonctionne uniquement pour les dossiers vides, mais vous pouvez l’utiliser avec succès dans les dossiers non vides en définissant deux indicateurs : DEL_FOLDERS et DEL_MESSAGES. Uniquement les dossiers vides ou dossiers définir des indicateurs DEL_MESSAGES et DEL_FOLDERS sur l’appel **DeleteFolder** peuvent être supprimés. DEL_FOLDERS permet à tous les sous-dossiers du dossier à supprimer ; DEL_MESSAGES permet à tous les messages du dossier à supprimer. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs dossiers, effectuez l’opération complètement que possible pour chaque dossier. Parfois, un des dossiers à supprimer n’existe pas ou a été déplacé ou copié ailleurs. N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteFolder** a supprimé tous les messages et sous-dossier.  <br/> |S_OK  <br/> |
|Impossible de supprimer tous les messages et sous-dossier **DeleteFolder** .  <br/> |MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteFolder** n’a pas pu terminer.  <br/> |Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteFolder** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée. **DeleteFolder** peut-être en mesure de supprimer un ou plusieurs des messages et les sous-dossiers avant de rencontrer l’erreur. 
  
Si un ou plusieurs sous-dossiers ne peuvent pas être supprimées, **DeleteFolder** renvoie MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du fournisseur de banque de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MsgStoreDlg.cpp  <br/> |CMsgStoreDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::DeleteFolder** pour supprimer des dossiers.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

