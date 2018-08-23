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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: fdf75787153f9a85e6a7bcddff44cf2c468a7975
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595033"
---
# <a name="imapisessionopenmsgstore"></a>IMAPISession::OpenMsgStore

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre une banque de messages et retourne un pointeur [IMsgStore](imsgstoreimapiprop.md) pour davantage d’accès. 
  
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
  
> [in] Un handle vers la fenêtre parent de la boîte de dialogue commune adresse et d’autres liées affiche.
    
_cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
_lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la banque de messages à ouvrir. Le paramètre _lpEntryID_ ne doit pas être NULL. 
    
_lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder au magasin de message. Passage de NULL entraîne le paramètre _lppMDB_ renvoyer un pointeur vers l’interface standard pour une banque de messages (**IMsgStore**).
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
  - MAPI_BEST_ACCESS : Demandes que la banque de messages s’ouvre avec les autorisations de réseau maximum autorisé pour l’utilisateur et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, la banque de messages doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, la banque de messages doit être ouvert avec l’autorisation en lecture seule. 
      
  - MAPI_DEFERRED_ERRORS : Permet **OpenMsgStore** retournée correctement, éventuellement avant le message magasin est totalement disponible au client appelant. Si la banque de messages n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur. 
      
  - MDB\_NO_DIALOG : empêche l’affichage des boîtes de dialogue d’ouverture de session. Si cet indicateur est défini et **OpenMsgStore** contient des informations de configuration insuffisante pour ouvrir la banque de messages sans l’aide de l’utilisateur, elle renvoie MAPI_E_LOGON_FAILED. Si cet indicateur n’est pas défini, le fournisseur de banque de message peut inviter l’utilisateur pour corriger un nom ou le mot de passe ou pour effectuer d’autres actions qui sont nécessaires pour établir une connexion avec la banque de messages. 
      
  - MDB\_NO_MAIL : la banque de messages ne doit pas être utilisée pour envoyer ou recevoir de courrier. Lorsque cet indicateur est défini, MAPI ne notifie pas les le spouleur MAPI que cette banque de messages est en cours d’ouverture.
      
  - MDB\_en ligne : en Mode Exchange mis en cache, un client ou fournisseur de services peut appeler cette méthode avec MDB_ONLINE pour remplacer la connexion à la base de messages locale et ouvrez le magasin sur le serveur distant. Impossible d’ouvrir une banque Exchange en mode mis en cache et en mode non mis en cache en même temps dans la même session MAPI. Si vous avez déjà ouvert la banque de messages mis en cache, vous devez soit fermer le magasin avant d’ouvrir avec cet indicateur ou ouvrir une nouvelle session MAPI où vous pouvez ouvrir la banque d’informations Exchange sur le serveur distant à l’aide de cet indicateur.
      
  - MDB_TEMPORARY : Demande à MAPI que la banque de messages n’est pas définitive et ne doit pas être ajoutée à la table. Cet indicateur est utilisé pour vous connecter à la banque de messages afin que les informations peuvent être récupérées par programme dans la section de profil. 
      
  - MDB_WRITE : Demandes de lecture/écriture autorisation de la banque de messages.
    
_lppMDB_
  
> [out] Pointeur vers un pointeur de la banque de messages.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La banque de messages a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour accéder à une banque de messages pour lesquels l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> La banque de messages indiquée par _lpEntryID_ n’existe pas. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge de la page de codes du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais le fournisseur de banque de messages a des informations d’erreur disponibles. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour obtenir les informations d’erreur à partir du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md).
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenMsgStore** ouvre une banque de messages donnée. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Le niveau d’autorisation par défaut pour les banques de messages est en lecture seule. Si vous définissez l’indicateur MDB_WRITE, vous toujours ne pourrez pas être autorisation en lecture-écriture. Le dernier niveau d’accès MAPI attribue à la banque de messages dépend de votre niveau d’autorisation, la banque de messages lui-même et le fournisseur de banque de messages. 
  
Si vous appelez **OpenMsgStore** pour ouvrir une banque de messages avec une autorisation en lecture seule, les éléments suivants se produisent : 
  
- La banque de **PR\_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) propriété n’aura pas son magasin\_MODIFY_OK et le magasin de\_CREATE_OK bits set. 
    
- Les appels pour ouvrir un des dossiers ou des messages de la banque de messages à l’aide de [IMAPISession::OpenEntry](imapisession-openentry.md) avec l’indicateur n’échoue. 
    
- Les appels pour ouvrir une des propriétés des dossiers ou des messages de la banque de messages à l’aide de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec l’indicateur n’échoue. 
    
- Les appels à une des méthodes suivantes échoueront : 
    
  - [IMAPIFolder::CreateMessage](imapifolder-createmessage.md)
    
  - [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md)
    
  - [IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
    
  - [IMAPIFolder::DeleteFolder](imapifolder-deletefolder.md)
    
  - [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md)
    
  - [IMAPIProp::SetProps](imapiprop-setprops.md)
    
  - [IMAPIProp::DeleteProps](imapiprop-deleteprops.md)
  
- Appels aux méthodes suivantes échoueront si la destination pour le message copié est en lecture seule, si la destination est la même que la banque de messages source ou un autre magasin en lecture seule.
    
  - [IMAPIFolder::CopyMessages](imapifolder-copymessages.md)
    
  - [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md)
    
  - [IMAPIProp::CopyTo](imapiprop-copyto.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |CallOpenMsgStore  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenMsgStore** pour ouvrir une banque de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
- [IMAPISession::GetLastError](imapisession-getlasterror.md)
- [IMAPISession::OpenEntry](imapisession-openentry.md)
- [IMAPIProp::OpenProperty](imapiprop-openproperty.md)
- [IMAPISession : IUnknown](imapisessioniunknown.md)
- [MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
- [Utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md)

