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
ms.openlocfilehash: 0f0523c01e163b57d9ed37d9b324ec858adbd685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426071"
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
  
> [in] Handle vers la fenêtre parent de l’indicateur de progression. Le _paramètre ulUIParam_ est ignoré, sauf si l’MESSAGE_DIALOG est définie dans _le paramètre ulFlags._ 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si NULL est transmis dans  _lpProgress,_ le fournisseur de magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le _paramètre lpProgress est_ ignoré, sauf si l’MESSAGE_DIALOG est définie dans le paramètre _ulFlags._ 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les messages sont supprimés. Les indicateurs suivants peuvent être définies :
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris les messages supprimés (supprimés de manière temporaire).
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression au cours de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages spécifiés ont été supprimés avec succès.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais tous les messages n’ont pas été supprimés avec succès. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIFolder::D eleteMessages** supprime les messages d’un dossier. Les messages qui n’existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec une autorisation de lecture/écriture ou qui sont actuellement envoyés ne peuvent pas être supprimés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque dossier, même si un ou plusieurs des messages ne peuvent pas être supprimés. N’arrêtez pas l’opération prématurément, sauf si une défaillance dépasse votre contrôle, par exemple un manque de mémoire, un manque d’espace disque ou une altération de la magasin de messages.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ce que ces valeurs de retour se placent dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteMessages a** correctement supprimé chaque message.  <br/> |S_OK  <br/> |
|**DeleteMessages n’a** pas pu supprimer correctement tous les messages et sous-fichiers.  <br/> |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages** n’a pas pu se terminer.  <br/> |Toute valeur d’erreur à l’exception MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteMessages n’est** pas en mesure de se terminer, ne supposez pas qu’aucun travail n’a été effectué. **DeleteMessages a** peut-être pu supprimer un ou plusieurs des messages avant de rencontrer l’erreur. 
  
 **DeleteMessages** renvoie MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation de la boutique de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise **la méthode IMAPIFolder::D eleteMessages** pour supprimer les messages spécifiés.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

