---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e9e0ad958acc40dd28f3d9aab9996c1b7a36f38a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591484"
---
# <a name="imapisessionshowform"></a>IMAPISession::ShowForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Affiche un formulaire.
  
```cpp
HRESULT ShowForm(
  ULONG_PTR ulUIParam,
  LPMDB lpMsgStore,
  LPMAPIFOLDER lpParentFolder,
  LPCIID lpInterface,
  ULONG ulMessageToken,
  LPMESSAGE lpMessageSent,
  ULONG ulFlags,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  ULONG ulAccess,
  LPSTR lpszMessageClass
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent du formulaire.
    
 _lpMsgStore_
  
> [in] Un pointeur vers la banque de messages qui contient le dossier indiqué par le paramètre _lpParentFolder_ . 
    
 _lpParentFolder_
  
> [in] Pointeur vers le dossier dans lequel le message associé au paramètre _ulMessageToken_ a été créé. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message qui s’affiche dans le formulaire. Le paramètre _lpInterface_ doit être NULL ou IID_IMessage. Résultats de la transmission NULL dans l’interface standard, [IMessage](imessageimapiprop.md), utilisé. 
    
 _ulMessageToken_
  
> [in] Le jeton qui est associé avec le message à afficher dans le formulaire. Le paramètre _ulMessageToken_ doit avoir le contenu du paramètre _lpulMessageToken_ à partir de l’appel précédent à [IMAPISession::PrepareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Réservé ; doit être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle comment et si le message est enregistré. Les indicateurs suivants peuvent être définis :
    
MAPI_NEW_MESSAGE 
  
> Le message n’a jamais été enregistré (autrement dit, la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) a jamais été appelée). 
    
MAPI_POST_MESSAGE 
  
> Le message doit être enregistré dans son dossier parent. Le message n’est pas traité pour l’envoi, mais est publié dans le dossier à la place. Si cet indicateur n’est pas défini, le message est copié dans la boîte d’envoi et est traité pour l’envoi. 
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Les indicateurs fournissent des informations sur l’état du message. 
    
 _ulMessageFlags_
  
> [in] Masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Ces indicateurs fournissent davantage d’informations sur l’état du message. 
    
 _ulAccess_
  
> [in] Indicateur qui indique le niveau d’autorisation pour le message qui s’affiche dans le formulaire. Ces informations sont copiées à partir de la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message de message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire est affiché avec succès.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::ShowForm** affiche un formulaire de message qui a été préparé par la méthode **IMAPISession::PrepareForm** . 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Vous devez disposer d’une seule référence au message passé dans _lpMessage_ paramètre la méthode **PrepareForm** . 
  
Sachez que les implémentations de formulaire peuvent renvoyer des valeurs d’erreur autres que ceux documentés par MAPI. Si vous pouvez utiliser ces valeurs d’erreur pour déterminer plus précise de la condition d’erreur, faites-le. Dans le cas contraire, gérer ces erreurs comme vous le feriez MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::ShowForm** , avec la méthode **PrepareForm** , pour afficher un message dans un formulaire modal.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

