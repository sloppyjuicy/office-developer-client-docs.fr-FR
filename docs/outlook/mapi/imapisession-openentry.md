---
title: IMAPISessionOpenEntry
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4cde3fb71eeccd82042787e329f96309eaffa8c3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596175"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire.
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. La transmission null renvoie l’interface standard de l’objet. Par exemple, si l’objet à ouvrir est un message, l’interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il s’agit [de IMAPIFolder](imapifolderimapicontainer.md). Les interfaces standard pour les objets de carnet d’adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande l’ouverture de l’objet à l’aide des autorisations réseau maximales autorisées pour l’utilisateur et de l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert avec une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert avec une autorisation en lecture seule. 
    
MAPI_CACHE_OK
  
> Utilisez tous les moyens, y compris les carnets d’adresses en mode hors connexion, pour effectuer la résolution des noms.
    
MAPI_CACHE_ONLY
  
> Utilisez uniquement le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Par exemple, vous pouvez utiliser cet indicateur pour permettre à une application cliente d’ouvrir la liste d’adresses globale (LAL) en mode Exchange mis en cache et d’accéder à une entrée dans ce carnet d’adresses à partir du cache sans créer de trafic entre le client et le serveur. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de renvoyer correctement, éventuellement avant que l’objet soit entièrement disponible pour le client appelant. Si l’objet n’est pas disponible, un appel d’objet ultérieur peut provoquer une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture est accordée. 
    
MAPI_NO_CACHE
  
> N’utilisez pas le carnet d’adresses en mode hors connexion pour effectuer la résolution de noms. Cet indicateur est pris en charge uniquement par le Exchange de carnet d’adresses.
    
SHOW_SOFT_DELETES
  
> Afficher les éléments actuellement marqués comme supprimés (c’est-à-dire en phase de rétention des éléments supprimés).
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’un objet en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_FOUND 
  
> Il n’existe pas d’objet associé à l’identificateur d’entrée transmis dans _le paramètre lpEntryID._ 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée transmis dans le paramètre  _lpEntryID_ est dans un format non reconnu. Cette valeur est généralement renvoyée si le fournisseur de services qui contient l’objet n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISession::OpenEntry** ouvre un objet de magasin de messages ou de carnet d’adresses, renvoyant un pointeur vers une interface qui peut être utilisée pour accéder à l’objet. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

> [!IMPORTANT]
> Lors de l’ouverture d’entrées de dossiers dans une boutique publique, telles que des dossiers et des messages, utilisez [IMsgStore::OpenEntry](imsgstore-openentry.md) au lieu d’IMAPISession::OpenEntry .  Cela garantit que les dossiers publics fonctionnent correctement lorsque plusieurs Exchange sont définis dans un profil. 
  
Appelez **IMAPISession::OpenEntry** uniquement lorsque vous ne connaissez pas le type d’objet que vous ouvrez. Si vous savez que vous ouvrez un dossier ou un message, appelez [IMsgStore::OpenEntry](imsgstore-openentry.md). Si vous savez que vous ouvrez un conteneur de carnet d’adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md). Ces méthodes plus spécifiques sont plus rapides que **IMAPISession::OpenEntry**. 
  
MAPI ouvre tous les objets avec une autorisation en lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le _paramètre ulFlags._ La définition de l’un de ces indicateurs ne garantit pas un type d’accès particulier ; Les autorisations accordées dépendent du fournisseur de services, du niveau d’accès et de l’objet. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez PR_ACCESS_LEVEL **propriété** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Appeler **IMAPISession::OpenEntry** et définir  _lpEntryID_ pour qu’il pointe vers l’identificateur d’entrée d’une magasin de messages est identique à l’appel de la méthode [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) avec l’indicateur MDB_NO_DIALOG. Les paramètres d’indicateur sont également équivalents, sauf que pour demander une autorisation de lecture/écriture avec **OpenMsgStore,** vous devez définir l’indicateur MDB_WRITE au lieu de MAPI_MODIFY. 
  
Vérifiez la valeur renvoyée dans le  _paramètre lpulObjType_ pour déterminer si le type d’objet renvoyé est ce que vous attendiez. Si le type d’objet n’est pas celui attendu, castez le pointeur du paramètre  _lppUnk_ vers un pointeur du type approprié. Par exemple, si vous ouvrent un dossier, cast  _lppUnk_ vers un pointeur de type LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la **méthode IMAPISession::OpenEntry** pour ouvrir un objet.  <br/> |
   
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

