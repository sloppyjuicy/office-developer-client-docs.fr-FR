---
title: IMAPIFolderDeleteMessages
description: IMAPIFolderDeleteMessages supprime un ou plusieurs messages. Cet article décrit sa syntaxe, ses paramètres, sa valeur de retour et ses remarques.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIFolder.DeleteMessages
api_type:
- COM
ms.assetid: 5a16e62b-9d33-41cd-af2b-9abd403b6f2e
ms.openlocfilehash: b8f6b4dfba33b8e39323afb9fd98a07d27b20ed3
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812242"
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
  
> [in] Handle de la fenêtre parente de l’indicateur de progression. Le paramètre  _ulUIParam_ est ignoré, sauf si l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _lpProgress_
  
> [in] Pointeur vers un objet de progression qui affiche un indicateur de progression. Si null est passé dans  _lpProgress_, le fournisseur du magasin de messages affiche un indicateur de progression à l’aide de l’implémentation de l’objet de progression MAPI. Le paramètre  _lpProgress_ est ignoré, sauf si l’indicateur MESSAGE_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont les messages sont supprimés. Les indicateurs suivants peuvent être définis :
    
DELETE_HARD_DELETE
  
> Supprime définitivement tous les messages, y compris ceux supprimés de manière réversible.
    
MESSAGE_DIALOG 
  
> Affiche un indicateur de progression à mesure que l’opération se poursuit.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le ou les messages spécifiés ont été supprimés avec succès.
    
MAPI_W_PARTIAL_COMPLETION 
  
> L’appel a réussi, mais tous les messages n’ont pas été supprimés avec succès. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIFolder::D eleteMessages** supprime les messages d’un dossier. Les messages qui n’existent pas, qui ont été déplacés ailleurs, qui sont ouverts avec l’autorisation de lecture/écriture ou qui sont actuellement envoyés ne peuvent pas être supprimés. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque l’opération de suppression implique plusieurs messages, effectuez l’opération aussi complètement que possible pour chaque dossier, même si un ou plusieurs messages ne peuvent pas être supprimés. N’arrêtez pas l’opération prématurément, à moins qu’une défaillance ne soit hors de votre contrôle, comme un manque de mémoire, un manque d’espace disque ou une altération du magasin de messages.
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Attendez-vous à ces valeurs de retour dans les conditions suivantes.
  
|**Condition**|**Valeur renvoy�e**|
|:-----|:-----|
|**DeleteMessages** a correctement supprimé chaque message. |S_OK  <br/> |
|**DeleteMessages n’a** pas réussi à supprimer tous les messages et sous-dossiers. |MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND  <br/> |
|**DeleteMessages n’a** pas pu se terminer. |Toute valeur d’erreur sauf MAPI_E_NOT_FOUND  <br/> |
   
Lorsque **DeleteMessages** n’est pas en mesure de se terminer, ne partez pas du principe qu’aucun travail n’a été effectué. **DeleteMessages** a peut-être pu supprimer un ou plusieurs des messages avant de rencontrer l’erreur. 
  
 **DeleteMessages** retourne MAPI_W_PARTIAL_COMPLETION ou MAPI_E_NOT_FOUND, en fonction de l’implémentation du magasin de messages. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|FolderDlg.cpp  <br/> |CFolderDlg::OnDeleteSelectedItem  <br/> |MFCMAPI utilise la méthode **IMAPIFolder::D eleteMessages** pour supprimer les messages spécifiés. |
   
## <a name="see-also"></a>Voir aussi



[ENTRYID](entryid.md)
  
[ENTRYLIST](entrylist.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

