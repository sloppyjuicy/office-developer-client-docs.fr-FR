---
title: IMAPISessionOpenEntry
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPISessionOpenEntry, qui ouvre un objet et retourne un pointeur d’interface pour un accès supplémentaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
ms.openlocfilehash: 72328b7a70dd60d9c2811570901de9a08c888285
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827953"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet et retourne un pointeur d’interface pour un accès supplémentaire.
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. Le passage de NULL retourne l’interface standard de l’objet. Par exemple, si l’objet à ouvrir est un message, l’interface standard est [IMessage](imessageimapiprop.md) ; pour les dossiers, il s’agit [d’IMAPIFolder](imapifolderimapicontainer.md). Les interfaces standard pour les objets de carnet d’adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet soit ouvert à l’aide des autorisations réseau maximales autorisées pour l’utilisateur et de l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert avec l’autorisation de lecture/écriture ; si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert avec une autorisation en lecture seule. 
    
MAPI_CACHE_OK
  
> Utilisez tous les moyens, y compris les carnets d’adresses hors connexion, pour effectuer la résolution de noms.
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (GAL) en mode d’échange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le fournisseur de carnets d’adresses Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de retourner correctement, éventuellement avant que l’objet soit entièrement disponible pour le client appelant. Si l’objet n’est pas disponible, l’exécution d’un appel d’objet suivant peut provoquer une erreur. 
    
MAPI_MODIFY 
  
> Demande l’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule, et les clients ne doivent pas fonctionner en partant du principe que l’autorisation de lecture/écriture est accordée. 
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le fournisseur de carnets d’adresses Exchange.
    
SHOW_SOFT_DELETES
  
> Afficher les éléments actuellement marqués comme supprimés de manière réversible (autrement dit, ils sont dans la phase de durée de rétention des éléments supprimés).
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’un objet en lecture seule ou une tentative d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> Aucun objet n’est associé à l’identificateur d’entrée passé dans le paramètre _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée passé dans le paramètre _lpEntryID_ est dans un format méconnaissable. Cette valeur est généralement retournée si le fournisseur de services qui contient l’objet n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISession::OpenEntry** ouvre un magasin de messages ou un objet carnet d’adresses, en renvoyant un pointeur vers une interface qui peut être utilisée pour accéder à l’objet. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

> [!IMPORTANT]
> Lorsque vous ouvrez des entrées de dossier sur un magasin public, comme des dossiers et des messages, utilisez [IMsgStore::OpenEntry](imsgstore-openentry.md) au lieu **d’IMAPISession::OpenEntry**. Cela garantit que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
Appelez **IMAPISession::OpenEntry** uniquement lorsque vous ne savez pas quel type d’objet vous ouvrez. Si vous savez que vous ouvrez un dossier ou un message, appelez [IMsgStore::OpenEntry](imsgstore-openentry.md). Si vous savez que vous ouvrez un conteneur de carnet d’adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md). Ces méthodes plus spécifiques sont plus rapides que **IMAPISession::OpenEntry**. 
  
MAPI ouvre tous les objets avec une autorisation en lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ . La définition de l’un de ces indicateurs ne garantit pas un type particulier d’accès; les autorisations accordées dépendent du fournisseur de services, du niveau d’accès et de l’objet. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
**L’appel d’IMAPISession::OpenEntry** et la définition _de lpEntryID_ pour pointer vers l’identificateur d’entrée d’un magasin de messages revient à appeler la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) avec l’indicateur MDB_NO_DIALOG défini. Les paramètres d’indicateur sont également équivalents, sauf que pour demander l’autorisation de lecture/écriture avec **OpenMsgStore**, vous devez définir l’indicateur MDB_WRITE au lieu de MAPI_MODIFY. 
  
Vérifiez la valeur retournée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné correspond à ce que vous attendiez. Si le type d’objet n’est pas le type attendu, castez le pointeur du paramètre  _lppUnk_ en pointeur du type approprié. Par exemple, si vous ouvrez un dossier, cast  _lppUnk_ en pointeur de type LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMAPISession::OpenEntry** pour ouvrir un objet. |
   
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

