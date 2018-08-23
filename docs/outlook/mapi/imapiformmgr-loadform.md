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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 3e758acfa1cf0c11be666dd730d9bf589d2e9d77
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586213"
---
# <a name="imapiformmgrloadform"></a>IMAPIFormMgr::LoadForm

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Démarre un formulaire pour ouvrir un message existant.
  
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
  
> [in] Un handle vers la fenêtre parent de l’indicateur de progression est affichée pendant que le formulaire est ouvert. Le paramètre _ulUIParam_ est ignoré à moins que l’indicateur MAPI_DIALOG est défini dans le paramètre _ulFlags_ . 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le formulaire est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_DIALOG 
  
> Affiche une interface utilisateur pour fournir l’état ou demandez à l’utilisateur pour plus d’informations. Si cet indicateur n’est pas défini, aucune interface utilisateur est affichée.
    
MAPIFORM_EXACTMATCH 
  
> Seules les chaînes de classe de message qui sont une correspondance exacte doivent être résolus.
    
 _lpszMessageClass_
  
> [in] Pointeur vers une chaîne qui nomme la classe de message du message à charger. Si NULL est indiqué dans le paramètre _lpszMessageClass_ , la classe de message est déterminée à partir du message indiqué par le paramètre _pmsg_ . 
    
 _ulMessageStatus_
  
> [in] Masque de bits d’indicateurs défini par le client ou défini par le fournisseur copiées à partir de la propriété **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) du message qui fournit des informations sur l’état du message. Le paramètre _ulMessageStatus_ doit être défini si _lpszMessageClass_ n’est pas NULL ; Sinon, _ulMessageStatus_ est ignorée. 
    
 _ulMessageFlags_
  
> [in] Pointeur vers un masque de bits d’indicateurs copié à partir de la propriété **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) du message qui indique l’état actuel du message. Le paramètre _ulMessageFlags_ doit être défini si _lpszMessageClass_ n’est pas NULL ; Sinon, _ulMessageFlags_ est ignorée. 
    
 _pFolderFocus_
  
> [in] Pointeur vers le dossier qui contient directement le message. Le paramètre _pFolderFocus_ peut être NULL si un tel dossier n’existe pas (par exemple, si le message est incorporé dans un autre message). 
    
 _pMessageSite_
  
> [in] Pointeur vers le site de message du message.
    
 _pMsg_
  
> [in] Pointeur vers le message.
    
 _pViewContext_
  
> [in] Pointeur vers le contexte d’affichage pour le message. Le paramètre _pViewContext_ peut être NULL. 
    
 _riid_
  
> [in] L’identificateur d’interface (IID) de l’interface à utiliser pour l’objet de formulaire renvoyé. Le paramètre _riid_ ne doit pas être NULL. 
    
 _ppvObj_
  
> [out] Pointeur vers un pointeur vers l’interface retournée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_INTERFACE 
  
> Le formulaire ne prend pas en charge l’interface demandée.
    
MAPI_E_NOT_FOUND 
  
> La classe de message passée dans _lpszMessageClass_ ne correspond pas à la classe de message pour n’importe quel formulaire dans la bibliothèque de formulaires. 
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appeler la méthode **IMAPIFormMgr::LoadForm** pour ouvrir un formulaire pour un message existant. **LoadForm** ouvre l’objet de formulaire, charge le message dans l’objet de formulaire, définit le contexte de vue appropriée, si nécessaire et renvoie l’interface demandée pour l’objet de formulaire. 
  
Le paramètre _pFolderFocus_ pointe vers le dossier qui contient le message. Si le message est incorporé dans un autre message, _pFolderFocus_ doit être NULL. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si NULL est indiqué dans _lpszMessageClass_, l’implémentation Obtient la classe de message du message, l’état et d’indicateurs à partir du message **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), **PR_MSG_STATUS** et **PR_MESSAGE_FLAGS **propriétés. Si une chaîne de classe de message est fournie dans _lpszMessageClass_, l’implémentation doit utiliser les valeurs _ulMessageStatus_ et _ulMessageFlags_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFormFunctions.cpp  <br/> |OpenMessageNonModal  <br/> |MFCMAPI utilise la méthode **IMAPIFormMgr::LoadForm** pour charger un formulaire avant de les afficher.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Propriété canonique PidTagMessageClass](pidtagmessageclass-canonical-property.md)
  
[Propriété canonique PidTagMessageFlags](pidtagmessageflags-canonical-property.md)
  
[Propriété canonique PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)
  
[IMAPIFormMgr : IUnknown](imapiformmgriunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

