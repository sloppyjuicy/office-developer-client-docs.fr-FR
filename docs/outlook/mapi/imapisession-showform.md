---
title: IMAPISessionShowForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.ShowForm
api_type:
- COM
ms.assetid: 233cf936-34db-42d4-b5e3-17a93acb2009
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fbe1087c2d7036aeb7b02b019cf6bec84e43d139
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561529"
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
  
> [in] Poignée vers la fenêtre parent du formulaire.
    
 _lpMsgStore_
  
> [in] Pointeur vers la magasin de messages qui contient le dossier pointé par _le paramètre lpParentFolder._ 
    
 _lpParentFolder_
  
> [in] Pointeur vers le dossier dans lequel le message associé au paramètre  _ulMessageToken_ a été créé. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message affiché dans le formulaire. Le  _paramètre lpInterface_ doit être NULL ou IID_IMessage. La transmission DE NULL entraîne l’utilisation [de l’interface standard, IMessage.](imessageimapiprop.md) 
    
 _ulMessageToken_
  
> [in] Jeton associé au message à afficher dans le formulaire. Le  _paramètre ulMessageToken_ doit être paramétré sur le contenu du paramètre  _lpulMessageToken_ de l’appel précédent à [IMAPISession::P repareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Réservé ; doit être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle comment et si le message est enregistré. Les indicateurs suivants peuvent être définies :
    
MAPI_NEW_MESSAGE 
  
> Le message n’a jamais été enregistré (autrement dit, sa méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) n’a jamais été appelée). 
    
MAPI_POST_MESSAGE 
  
> Le message doit être enregistré dans son dossier parent. Le message n’est pas traitée pour l’envoi, mais est publié dans le dossier à la place. Si cet indicateur n’est pas définie, le message est copié dans la boîte d’envoi et est traitée pour l’envoi. 
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._ Les indicateurs fournissent des informations sur l’état du message. 
    
 _ulMessageFlags_
  
> [in] Masque de bits d’indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._ Ces indicateurs fournissent des informations supplémentaires sur l’état du message. 
    
 _ulAccess_
  
> [in] Indicateur qui indique le niveau d’autorisation pour le message affiché dans le formulaire. Ces informations sont copiées à partir **de la propriété PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._ 
    
 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message du message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken._ 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été affiché avec succès.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::ShowForm** affiche un formulaire de message qui a été préparé par la méthode **IMAPISession::P repareForm.** 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous ne devez avoir qu’une seule référence au message transmis dans le paramètre _lpMessage_ de la méthode **PrepareForm.** 
  
N’ignorez pas que les implémentations de formulaire peuvent renvoyer des valeurs d’erreur autres que celles documentées par MAPI. Si vous pouvez utiliser ces valeurs d’erreur pour déterminer plus précisément la condition d’erreur, faites-le. Sinon, traitez ces erreurs comme vous le feriez pour MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::ShowForm,** ainsi que la méthode **PrepareForm,** pour afficher un message sous forme modale.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

