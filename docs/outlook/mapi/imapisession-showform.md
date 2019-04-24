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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8b90dee3958a20994f9a60d104ae714ad95307d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335664"
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
  
> dans Handle de la fenêtre parente du formulaire.
    
 _lpMsgStore_
  
> dans Pointeur vers la Banque de messages qui contient le dossier désigné par le paramètre _lpParentFolder_ . 
    
 _lpParentFolder_
  
> dans Pointeur vers le dossier dans lequel le message associé au paramètre _ulMessageToken_ a été créé. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder au message affiché dans le formulaire. Le paramètre _lpInterface_ doit être null ou IID_IMessage. Le passage de résultats NULL dans l'interface standard, [IMessage](imessageimapiprop.md), est utilisé. 
    
 _ulMessageToken_
  
> dans Jeton associé au message à afficher dans le formulaire. Le paramètre _ulMessageToken_ doit être défini sur le contenu du paramètre _lpulMessageToken_ à partir de l'appel précédent à [IMAPISession::P repareform](imapisession-prepareform.md).
    
 _lpMessageSent_
  
> dans MSR doit être NULL. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle comment et si le message est enregistré. Les indicateurs suivants peuvent être définis:
    
MAPI_NEW_MESSAGE 
  
> Le message n'a jamais été enregistré (la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) n'a jamais été appelée). 
    
MAPI_POST_MESSAGE 
  
> Le message doit être enregistré dans son dossier parent. Le message n'est pas traité pour l'envoi, mais il est publié dans le dossier à la place. Si cet indicateur n'est pas défini, le message est copié dans la boîte d'envoi et est traité pour l'envoi. 
    
 _ulMessageStatus_
  
> dans Masque de des indicateurs copiés à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Les indicateurs fournissent des informations sur l'état du message. 
    
 _ulMessageFlags_
  
> dans Masque de des indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . Ces indicateurs fournissent des informations supplémentaires sur l'état du message. 
    
 _ulAccess_
  
> dans Indicateur qui indique le niveau d'autorisation du message affiché dans le formulaire. Ces informations sont copiées à partir de la propriété **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
 _lpszMessageClass_
  
> dans Pointeur vers la classe de message du message affiché dans le formulaire, copié à partir de la propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)) du message associé au jeton dans le paramètre _ulMessageToken_ . 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le formulaire s'est affiché correctement.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: ShowForm** affiche un formulaire de message qui a été préparé par la méthode **IMAPISession::P repareform** . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Vous ne devez avoir qu'une seule référence au message transmis dans le paramètre _lpMessage_ de la méthode **PrepareForm** . 
  
N'oubliez pas que les implémentations de formulaire peuvent renvoyer des valeurs d'erreur autres que celles documentées par MAPI. Si vous pouvez utiliser ces valeurs d'erreur pour obtenir une détermination plus précise de la condition d'erreur, faites-le. Dans le cas contraire, gérez ces erreurs comme vous le feriez pour MAPI_E_CALL_FAILED. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageModal  <br/> |MFCMAPI utilise la méthode **IMAPISession:: ShowForm** , ainsi que la méthode **PrepareForm** , pour afficher un message dans un formulaire modal.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMAPISession::PrepareForm](imapisession-prepareform.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

