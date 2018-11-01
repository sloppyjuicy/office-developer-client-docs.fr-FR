---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6234fc737857a7e35f562703802f81ff154b3ee6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591014"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet et retourne un pointeur d’interface pour l’accès supplémentaire.
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. Passage de NULL renvoie interface standard de l’objet. Par exemple, si l’objet à ouvrir est un message, l’interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il est [IMAPIFolder](imapifolderimapicontainer.md). Les interfaces standards pour les objets de carnet d’adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et les [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet doit être ouvert avec l’autorisation en lecture seule. 
    
MAPI_CACHE_OK
  
> Utiliser tous les moyens, y compris des carnets d’adresses en mode hors connexion, pour effectuer la résolution de noms.
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour autoriser une application cliente ouvrir la liste d’adresses globale (LAG) en mode exchange mis en cache et accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer le trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenEntry** renvoyer avec succès, éventuellement, avant de l’objet est entièrement disponible au client appelant. Si l’objet n’est pas disponible, un appel d’objet suivantes permettre provoquer une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que l’autorisation est accordée en lecture/écriture. 
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnet d’adresses Exchange.
    
SHOW_SOFT_DELETES
  
> Afficher les éléments qui sont actuellement marqués comme logicielles supprimés (autrement dit, ils sont dans la rétention des éléments supprimés phase de temps).
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour modifier un objet en lecture seule ou tentative d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_E_NOT_FOUND 
  
> Il n’est pas un objet associé à l’identificateur d’entrée passé dans le paramètre _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée passé dans le paramètre _lpEntryID_ est dans un format non reconnaissable. Cette valeur est généralement renvoyée si le fournisseur de services qui contient l’objet n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

Le s’ouvre à la méthode **IMAPISession::OpenEntry** un message doit être stockée ou adresses objet book, qui retourne un pointeur vers une interface qui peut servir à accéder à l’objet. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

> [!IMPORTANT]
> Lors de l’ouverture des entrées de dossier sur un magasin public, telles que les dossiers et messages, utilisez [IMsgStore::OpenEntry](imsgstore-openentry.md) au lieu de **IMAPISession::OpenEntry**. Ainsi, cette fonction de dossiers publics correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
Appelez **IMAPISession::OpenEntry** uniquement lorsque vous ne connaissez pas le type d’objet que vous ouvrez. Si vous savez que vous ouvrez un dossier ou un message, appelez [IMsgStore::OpenEntry](imsgstore-openentry.md). Si vous savez que vous ouvrez un conteneur de carnet d’adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md). Ces méthodes plus spécifiques sont plus rapides que **IMAPISession::OpenEntry**. 
  
MAPI ouvre tous les objets avec des autorisations en lecture seule, sauf si vous définissez l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ . Définition de l’une de ces indicateurs ne garantit pas un type particulier d’accès ; les autorisations qui sont accordées dépendent de l’objet, le niveau d’accès et le fournisseur de services. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Appel de **IMAPISession::OpenEntry** et le paramètre _lpEntryID_ pour pointer vers l’identificateur d’entrée d’une banque de messages est identique à l’appel de la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) avec l’indicateur MDB_NO_DIALOG défini. Les paramètres d’indicateur sont également équivalentes, exception faite que pour demander l’autorisation en lecture/écriture avec **OpenMsgStore**, vous devez définir l’indicateur MDB_WRITE au lieu de ne. 
  
Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné est attendue. Si le type d’objet n’est pas le type escomptés, convertir le pointeur à partir du paramètre _lppUnk_ vers un pointeur du type approprié. Par exemple, si vous ouvrez un dossier, un cast _lppUnk_ à un pointeur du type LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenEntry** pour ouvrir un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

