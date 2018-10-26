---
title: IMAPIFolderDeleteMessages
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: bd0439c71df7083e3c4787a5d317fa11d2b99c61
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578632"
---
# <a name="imapifolderdeletemessages"></a>IMAPIFolder::DeleteMessages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Supprime un ou plusieurs messages.
  
```cpp
HRESULT DeleteMessages(
  LPENTRYLIST lpMsgList,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _lpMsgList_
  
> [in] Pointeur vers une structure [ENTRYLIST](entrylist.md) qui contient le nombre de messages à supprimer et un tableau de structures [ENTRYID](entryid.md) qui identifient les messages. 
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est indiqué dans _lpProgress_, le fournisseur de banque de message affiche un indicateur de progression à l’aide de l’implémentation d’objet de progression MAPI. Le paramètre _lpProgress_ est ignoré à moins que l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les messages sont supprimés. Les indicateurs suivants peuvent être définis :
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux récupérable.
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’ou les messages spécifié ont été supprimés.
    
MAPI_W_PARTIAL_COMPLETION SE PRODUIT 
  
> L’appel a réussi, mais pas tous les messages ont été supprimés. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::DeleteMessages** supprime les messages à partir d’un dossier. Impossible de supprimer les messages qui n’existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec l’autorisation de lecture/écriture ou qui sont actuellement soumis. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs messages, effectuer l’opération complètement que possible pour chaque dossier, même si un ou plusieurs des messages ne peuvent pas être supprimées. N’arrêtez pas l’opération prématurément, sauf si une panne se produit qui est votre volonté, telles que le manque de mémoire, manque d’espace disque ou l’endommagement de la banque de messages.
  
## <a name="notes-to-callers"></a>Notes aux appelants

Prévoyez ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteMessages** a supprimé tous les messages.  <br/> |S_OK  <br/> |
|Impossible de supprimer tous les messages et sous-dossier **DeleteMessages** .  <br/> |MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** n’a pas pu terminer.  <br/> |Une valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteMessages** n’aboutit pas, ne supposez pas qu’aucun travail n’a été effectuée. **DeleteMessages** peut-être en mesure de supprimer un ou plusieurs des messages avant de rencontrer l’erreur. 
  
 **DeleteMessages** renvoie MAPI_W_PARTIAL_COMPLETION se produit ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la banque de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::DeleteMessages** pour supprimer les messages spécifiés.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de Macros pour la gestion des erreurs](using-macros-for-error-handling.md)

