---
title: IMAPIFormMgrLoadForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.LoadForm
api_type:
- COM
ms.assetid: 5ca500c3-c737-45a5-b0fc-473b75c1d68d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7e445646477ad1fc56b41141b541358d9b9f9616
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418784"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un formulaire pour ouvrir un message existant.
  
```cpp
HRESULT LoadForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR lpszMessageClass,
  ULONG ulMessageStatus,
  ULONG ulMessageFlags,
  LPMAPIFOLDER pFolderFocus,
  LPMAPIMESSAGESITE pMessageSite,
  LPMESSAGE pmsg,
  LPMAPIVIEWCONTEXT pViewContext,
  REFIID riid,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Handle de la fenêtre parente de l'indicateur de progression qui est affiché pendant l'ouverture du formulaire. Le paramètre _ulUIParam_ est ignoré sauf si l'indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture du formulaire. Les indicateurs suivants peuvent être définis:
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l'État ou inviter l'utilisateur à fournir des informations supplémentaires. Si cet indicateur n'est pas défini, aucune interface utilisateur n'est affichée.
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message correspondant à une correspondance exacte doivent être résolues.
    
 _lpszMessageClass_
  
> dans Pointeur vers une chaîne qui nomme la classe de message du message à charger. Si la valeur NULL est transmise au paramètre _lpszMessageClass_ , la classe de message est déterminée à partir du message désigné par le paramètre _PMSG_ . 
    
 _ulMessageStatus_
  
> dans Masque de bits des indicateurs définis par le client ou par le fournisseur, copié à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message qui fournit des informations sur l'état du message. Le paramètre _ulMessageStatus_ doit être défini si _LPSZMESSAGECLASS_ est non null; Sinon, _ulMessageStatus_ est ignoré. 
    
 _ulMessageFlags_
  
> dans Pointeur vers un masque de des indicateurs copiés à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message qui indique l'état actuel du message. Le paramètre _ulMessageFlags_ doit être défini si _LPSZMESSAGECLASS_ est non null; Sinon, _ulMessageFlags_ est ignoré. 
    
 _pFolderFocus_
  
> dans Pointeur vers le dossier qui contient directement le message. Le paramètre _pFolderFocus_ peut être null si ce dossier n'existe pas (par exemple, si le message est incorporé dans un autre message). 
    
 _pMessageSite_
  
> dans Pointeur vers le site de messagerie du message.
    
 _PMSG_
  
> dans Pointeur vers le message.
    
 _pViewContext_
  
> dans Pointeur vers le contexte d'affichage du message. Le paramètre _pViewContext_ peut être null. 
    
 _riid_
  
> dans Identificateur d'interface (IID) de l'interface à utiliser pour l'objet de formulaire renvoyé. Le paramètre _riid_ ne doit pas être null. 
    
 _ppvObj_
  
> remarquer Pointeur vers un pointeur vers l'interface renvoyée.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> Le formulaire ne prend pas en charge l'interface demandée.
    
MAPI_E_NOT_FOUND 
  
> La classe de message passée dans _lpszMessageClass_ ne correspond pas à la classe de message d'un formulaire de la bibliothèque de formulaires. 
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaires appellent la méthode **IMAPIFormMgr:: LoadForm** pour ouvrir un formulaire pour un message existant. **LoadForm** ouvre l'objet Form, charge le message dans l'objet Form, configure le contexte d'affichage approprié, si nécessaire, et renvoie l'interface demandée pour l'objet Form. 
  
Le paramètre _pFolderFocus_ pointe vers le dossier qui contient le message. Si le message est incorporé dans un autre message, _pFolderFocus_ doit être null. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si NULL est passé dans _lpszMessageClass_, l'implémentation obtient la classe de message, l'État et les indicateurs du message à partir des messages **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** et **PR_MESSAGE_FLAGS **propriétés. Si une chaîne de classe de message est fournie dans _lpszMessageClass_, l'implémentation doit utiliser les valeurs dans _ulMessageStatus_ et _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions. cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr:: LoadForm** pour charger un formulaire avant de l'afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

