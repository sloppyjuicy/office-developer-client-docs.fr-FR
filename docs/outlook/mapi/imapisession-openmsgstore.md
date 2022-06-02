---
title: IMAPISessionOpenMsgStore
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPISessionOpenMsgStore, qui ouvre un magasin de messages et retourne un pointeur IMsgStore pour un accès supplémentaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenMsgStore
api_type:
- COM
ms.assetid: 7f73b5cf-7093-42e9-8acc-63d73df77cf5
ms.openlocfilehash: 64649bae53f6c86d99b57435316d53294c2e516b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827946"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un magasin de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire. 
  
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

## <a name="parameters"></a>Paramètres

_ulUIParam_
  
> [in] Handle de la fenêtre parente de la boîte de dialogue d’adresse commune et d’autres affichages associés.
    
_cbEntryID_
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée du magasin de messages à ouvrir. Le paramètre  _lpEntryID_ ne doit pas être NULL. 
    
_lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au magasin de messages. Le passage  _de la valeur_ NULL entraîne le retour d’un pointeur vers l’interface standard d’un magasin de messages (**IMsgStore**).
    
_ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
  - MAPI_BEST_ACCESS : demande que le magasin de messages soit ouvert avec le nombre maximal d’autorisations réseau autorisées pour l’utilisateur et le nombre maximal d’autorisations d’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, le magasin de messages doit être ouvert avec l’autorisation de lecture/écriture ; si le client dispose d’une autorisation en lecture seule, le magasin de messages doit être ouvert avec une autorisation en lecture seule. 
      
  - MAPI_DEFERRED_ERRORS : permet à **OpenMsgStore** de retourner correctement, éventuellement avant que le magasin de messages soit entièrement disponible pour le client appelant. Si le magasin de messages n’est pas disponible, l’appel d’objet suivant peut générer une erreur. 
      
  - NO_DIALOG MDB\_: empêche l’affichage des boîtes de dialogue d’ouverture de session. Si cet indicateur est défini et **qu’OpenMsgStore** ne dispose pas d’informations de configuration suffisantes pour ouvrir le magasin de messages sans l’aide de l’utilisateur, il retourne MAPI_E_LOGON_FAILED. Si cet indicateur n’est pas défini, le fournisseur du magasin de messages peut inviter l’utilisateur à corriger un nom ou un mot de passe ou à effectuer d’autres actions nécessaires pour établir une connexion au magasin de messages. 
      
  - MDB\_NO_MAIL : le magasin de messages ne doit pas être utilisé pour l’envoi ou la réception de messages. Lorsque cet indicateur est défini, MAPI n’informe pas le spouleur MAPI que ce magasin de messages est ouvert.
      
  - MDB\_ONLINE : en mode Exchange mis en cache, un client ou un fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion au magasin de messages local et ouvrir le magasin sur le serveur distant. Vous ne pouvez pas ouvrir un magasin Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.
      
  - MDB_TEMPORARY : indique à MAPI que le magasin de messages n’est pas permanent et ne doit pas être ajouté à la table du magasin de messages. Cet indicateur est utilisé pour se connecter au magasin de messages afin que les informations puissent être récupérées par programmation à partir de la section de profil. 
      
  - MDB_WRITE : demande l’autorisation de lecture/écriture sur le magasin de messages.
    
_lppMDB_
  
> [out] Pointeur vers un pointeur du magasin de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le magasin de messages a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d’accès à un magasin de messages pour lequel l’utilisateur dispose d’autorisations insuffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> Le magasin de messages indiqué par  _lpEntryID_ n’existe pas. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge la page de codes du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais le fournisseur du magasin de messages dispose d’informations d’erreur disponibles. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour obtenir les informations d’erreur du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenMsgStore** ouvre un magasin de messages particulier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le niveau d’autorisation par défaut pour les magasins de messages est en lecture seule. Si vous définissez l’indicateur de MDB_WRITE, il se peut que vous ne bénéficiez toujours pas de l’autorisation de lecture/écriture. Le dernier niveau d’accès attribué par MAPI au magasin de messages dépend de votre niveau d’autorisation, du magasin de messages lui-même et du fournisseur du magasin de messages. 
  
Si vous appelez **OpenMsgStore** pour ouvrir un magasin de messages avec une autorisation en lecture seule, les événements suivants se produisent : 
  
- La propriété STORE_SUPPORT_MASK de **demande de tirage\_** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) du magasin n’aura pas ses bits STORE\_MODIFY_OK et STORE\_CREATE_OK. 
    
- Les appels pour ouvrir l’un des messages ou dossiers du magasin de messages à l’aide [d’IMAPISession::OpenEntry](imapisession-openentry.md) avec le MAPI_MODIFY jeu d’indicateurs échouent. 
    
- Les appels pour ouvrir l’une des propriétés des messages ou dossiers du magasin de messages à l’aide [d’IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’indicateur MAPI_MODIFY échouent. 
    
- Les appels à l’une des méthodes suivantes échouent : 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Les appels aux méthodes suivantes échouent si la destination du message copié est en lecture seule, que la destination soit identique au magasin de messages source ou qu’elle soit un autre magasin en lecture seule.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenMsgStore** pour ouvrir un magasin de messages. |
   
## <a name="see-also"></a>Voir aussi

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

