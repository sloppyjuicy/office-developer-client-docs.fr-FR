---
title: IMAPISessionOpenMsgStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 19d3df004676a71e2bf6243d9288efd824d99c33
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418021"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre une magasin de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire. 
  
```cpp
HRESULT OpenMsgStore(
  ULONG_PTR ulUIParam,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Parameters

_ulUIParam_
  
> [in] Poignée vers la fenêtre parente de la boîte de dialogue d’adresse commune et autres affichages associés.
    
_cbEntryID_
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
_lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la magasin de messages à ouvrir. Le  _paramètre lpEntryID_ ne doit pas être NULL. 
    
_lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à la magasin de messages. La transmission de null entraîne  _le paramètre lppMDB_ à renvoyer un pointeur vers l’interface standard pour une banque de messages (**IMsgStore**).
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
  - MAPI_BEST_ACCESS : demande l’ouverture de la magasin de messages avec les autorisations réseau maximales autorisées pour l’utilisateur et le nombre maximal d’autorisations d’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, la boutique de messages doit être ouverte avec une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, la boutique de messages doit être ouverte avec une autorisation en lecture seule. 
      
  - MAPI_DEFERRED_ERRORS : permet à **OpenMsgStore** de renvoyer correctement, éventuellement avant que la boutique de messages ne soit entièrement disponible pour le client appelant. Si la boutique de messages n’est pas disponible, un appel d’objet ultérieur peut occasioner une erreur. 
      
  - MDB NO_DIALOG : empêche l’affichage des boîtes de dialogue \_ d’affichage. Si cet indicateur est définie et **qu’OpenMsgStore** ne dispose pas d’informations de configuration suffisantes pour ouvrir la boutique de messages sans l’aide de l’utilisateur, il renvoie MAPI_E_LOGON_FAILED. Si cet indicateur n’est pas définie, le fournisseur de la boutique de messages peut invite l’utilisateur à corriger un nom ou un mot de passe ou à effectuer d’autres actions nécessaires pour établir une connexion à la magasin de messages. 
      
  - MDB NO_MAIL : la banque de messages ne doit pas être utilisée pour \_ envoyer ou recevoir des messages. Lorsque cet indicateur est définie, MAPI n’informe pas lepooler MAPI que cette boutique de messages est ouverte.
      
  - MDB ONLINE : en mode Exchange mis en cache, un client ou un fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion à la banque de messages locale et ouvrir la banque sur le serveur \_ distant. Vous ne pouvez pas ouvrir une Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.
      
  - MDB_TEMPORARY : indique à MAPI que la magasin de messages n’est pas permanente et qu’elle ne doit pas être ajoutée à la table de la boutique de messages. Cet indicateur est utilisé pour se connecter à la magasin de messages afin que les informations soient récupérées par programme à partir de la section de profil. 
      
  - MDB_WRITE : demande l’autorisation de lecture/écriture à la boutique de messages.
    
_lppMDB_
  
> [out] Pointeur vers un pointeur de la boutique de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La magasin de messages a été ouverte avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à une magasin de messages pour laquelle l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> La magasin de messages indiquée par  _lpEntryID_ n’existe pas. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais des informations d’erreur sont disponibles pour le fournisseur de la boutique de messages. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour obtenir les informations d’erreur du fournisseur, appelez la méthode [IMAPISession::GetLastError.](imapisession-getlasterror.md) Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::OpenMsgStore** ouvre une magasin de messages spécifique. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le niveau d’autorisation par défaut pour les magasins de messages est en lecture seule. Si vous définissez l’MDB_WRITE, il se peut que vous ne soyez toujours pas autorisé à lire/écrire. Le niveau final d’accès que MAPI attribue à la magasin de messages dépend de votre niveau d’autorisation, de la boutique de messages proprement dite et du fournisseur de la boutique de messages. 
  
Si vous appelez **OpenMsgStore** pour ouvrir une magasin de messages avec une autorisation en lecture seule, les données suivantes se produisent : 
  
- La propriété **STORE_SUPPORT_MASK \_** [(PidTagStoreSupportMask)](pidtagstoresupportmask-canonical-property.md)du magasin n’aura pas ses bits d’MODIFY_OK store et store CREATE_OK \_ \_ bits. 
    
- Les appels pour ouvrir l’un des messages ou dossiers de la boutique de messages à l’aide [d’IMAPISession::OpenEntry](imapisession-openentry.md) avec l’indicateur MAPI_MODIFY échouent. 
    
- Les appels pour ouvrir l’une des propriétés des messages ou dossiers de la boutique de messages à l’aide [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’indicateur MAPI_MODIFY échouent. 
    
- Les appels à l’une des méthodes suivantes échouent : 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Les appels aux méthodes suivantes échouent si la destination du message copié est en lecture seule, que la destination soit la même que la boutique de messages source ou s’il s’agit d’un autre magasin en lecture seule.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenMsgStore** pour ouvrir une magasin de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

