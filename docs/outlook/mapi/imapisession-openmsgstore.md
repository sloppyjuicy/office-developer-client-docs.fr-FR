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
  
Ouvre une banque de messages et renvoie un pointeur [IMsgStore](imsgstoreimapiprop.md) pour un accès supplémentaire. 
  
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
  
> dans Un handle vers la fenêtre parent de la boîte de dialogue adresse commune et d'autres affichages connexes.
    
_cbEntryID_
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
_lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de la Banque de messages à ouvrir. Le paramètre _lpEntryID_ ne doit pas être null. 
    
_lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à la Banque de messages. En passant la valeur NULL, le paramètre _lppMDB_ renvoie un pointeur vers l'interface standard pour une banque de messages (**IMsgStore**).
    
_ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être utilisés:
    
  - MAPI_BEST_ACCESS: demande l'ouverture de la Banque de messages avec les autorisations réseau maximales accordées à l'utilisateur et les autorisations d'application client maximales. Par exemple, si le client dispose d'une autorisation en lecture/écriture, la Banque de messages doit être ouverte avec une autorisation en lecture/écriture; Si le client dispose d'une autorisation en lecture seule, la Banque de messages doit être ouverte en lecture seule. 
      
  - MAPI_DEFERRED_ERRORS: permet à **OpenMsgStore** de renvoyer correctement, éventuellement avant que la Banque de messages soit entièrement disponible pour le client appelant. Si la Banque de messages n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur. 
      
  - MDB\_NO_DIALOG: empêche l'affichage des boîtes de dialogue d'ouverture de session. Si cet indicateur est défini et que **OpenMsgStore** ne dispose pas des informations de configuration suffisantes pour ouvrir la Banque de messages sans l'aide de l'utilisateur, elle renvoie MAPI_E_LOGON_FAILED. Si cet indicateur n'est pas défini, le fournisseur de banque de messages peut demander à l'utilisateur de corriger un nom ou un mot de passe ou d'effectuer d'autres actions nécessaires pour établir une connexion à la Banque de messages. 
      
  - MDB\_NO_MAIL: la Banque de messages ne doit pas être utilisée pour l'envoi ou la réception de messages. Lorsque cet indicateur est défini, MAPI n'avertit pas le spouleur MAPI que cette banque de messages est ouverte.
      
  - MDB\_en ligne: en mode Exchange mis en cache, un client ou un fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion à la Banque de messages locale et ouvrir la Banque sur le serveur distant. Vous ne pouvez pas ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mise en cache, vous devez fermer la banque avant de l’ouvrir avec cet indicateur, ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d'informations Exchange sur le serveur distant à l’aide de cet indicateur.
      
  - MDB_TEMPORARY: indique à MAPI que la Banque de messages n'est pas permanente et qu'elle ne doit pas être ajoutée à la table de banque de messages. Cet indicateur est utilisé pour se connecter à la Banque de messages afin que les informations puissent être récupérées par programmation à partir de la section profil. 
      
  - MDB_WRITE: demande une autorisation d'accès en lecture/écriture à la Banque de messages.
    
_lppMDB_
  
> remarquer Pointeur vers un pointeur de la Banque de messages.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La Banque de messages a été ouverte.
    
MAPI_E_NO_ACCESS 
  
> Une tentative d'accès à une banque de messages pour laquelle l'utilisateur ne dispose pas d'autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> La Banque de messages indiquée par _lpEntryID_ n'existe pas. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n'est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n'est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi, mais le fournisseur de banque de messages contient des informations d'erreur disponibles. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour obtenir les informations d'erreur du fournisseur, appelez la méthode [IMAPISession:: GetLastError](imapisession-getlasterror.md) . Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession:: OpenMsgStore** ouvre une banque de messages particulière. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Le niveau d'autorisation par défaut pour les banques de messages est en lecture seule. Si vous définissez l'indicateur MDB_WRITE, il se peut que vous ne soyez pas autorisé à accéder en lecture/écriture. Le niveau d'accès final attribué par MAPI à la Banque de messages dépend de votre niveau d'autorisation, de la Banque de messages proprement dite et du fournisseur de banque de messages. 
  
Si vous appelez **OpenMsgStore** pour ouvrir une banque de messages avec une autorisation en lecture seule, les opérations suivantes se produisent: 
  
- La propriété **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) de la Banque ne dispose pas de\_l'ensemble de\_bits Store MODIFY_OK et Store CREATE_OK. 
    
- Les appels pour ouvrir l'un des messages ou dossiers d'une banque de messages à l'aide de [IMAPISession:: OpenEntry](imapisession-openentry.md) avec l'indicateur MAPI_MODIFY défini échoueront. 
    
- Les appels pour ouvrir l'une des propriétés des messages ou dossiers d'une banque de messages à l'aide de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) avec l'indicateur MAPI_MODIFY échoueront. 
    
- Les appels à l'une des méthodes suivantes échouent: 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Les appels aux méthodes suivantes échouent si la destination du message copié est en lecture seule, si la destination est identique à la Banque de messages source ou s'il s'agit d'une autre banque en lecture seule.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions. cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI utilise la méthode **IMAPISession:: OpenMsgStore** pour ouvrir une banque de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
- [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)

