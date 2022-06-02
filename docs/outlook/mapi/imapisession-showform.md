---
title: IMAPISessionShowForm
description: Décrit la syntaxe, les paramètres, la valeur de retour et les remarques pour IMAPISessionShowForm, qui affiche un formulaire.
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
ms.openlocfilehash: ca06fe37b7c4be2da57a4a05d34e34636f2244eb
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827918"
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
  
> [in] Handle de la fenêtre parente du formulaire.
    
 _lpMsgStore_
  
> [in] Pointeur vers le magasin de messages qui contient le dossier vers lequel pointe le paramètre  _lpParentFolder_ . 
    
 _lpParentFolder_
  
> [in] Pointeur vers le dossier dans lequel le message associé au paramètre  _ulMessageToken_ a été créé. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au message affiché dans le formulaire. Le paramètre  _lpInterface_ doit être NULL ou IID_IMessage. Le passage de la valeur NULL entraîne l’utilisation de l’interface standard [, IMessage](imessageimapiprop.md). 
    
 _ulMessageToken_
  
> [in] Jeton associé au message à afficher dans le formulaire. Le paramètre  _ulMessageToken_ doit être défini sur le contenu du paramètre  _lpulMessageToken_ de l’appel précédent à [IMAPISession::P repareForm](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> [in] Réservé; doit être NULL. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôlent comment et si le message est enregistré. Les indicateurs suivants peuvent être définis :
    
MAPI_NEW_MESSAGE 
  
> Le message n’a jamais été enregistré (autrement dit, sa méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) n’a jamais été appelée). 
    
MAPI_POST_MESSAGE 
  
> Le message doit être enregistré dans son dossier parent. Le message n’est pas traité pour l’envoi, mais il est publié dans le dossier à la place. Si cet indicateur n’est pas défini, le message est copié dans la boîte de réception et traité pour l’envoi. 
    
 _ulMessageStatus_
  
> [in] Masque de bits des indicateurs copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Les indicateurs fournissent des informations sur l’état du message. 
    
 _ulMessageFlags_
  
> [in] Masque de bits des indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Ces indicateurs fournissent des informations supplémentaires sur l’état du message. 
    
 _ulAccess_
  
> [in] Indicateur qui indique le niveau d’autorisation du message affiché dans le formulaire. Ces informations sont copiées à partir de la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> [in] Pointeur vers la classe de message du message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire a été affiché avec succès.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::ShowForm** affiche un formulaire de message préparé par la méthode **IMAPISession::P repareForm** . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous ne devez avoir qu’une seule référence au message transmis dans le paramètre _lpMessage_ de la méthode **PrepareForm**. 
  
N’oubliez pas que les implémentations de formulaire peuvent retourner des valeurs d’erreur autres que celles documentées par MAPI. Si vous pouvez utiliser ces valeurs d’erreur pour déterminer plus précisément la condition d’erreur, procédez comme suit. Sinon, gérez ces erreurs comme vous le feriez pour MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession::ShowForm** , ainsi que la méthode **PrepareForm** , pour afficher un message dans un formulaire modal. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

