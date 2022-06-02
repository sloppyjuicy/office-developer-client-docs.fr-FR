---
title: IMsgStoreOpenEntry
description: IMsgStoreOpenEntry ouvre un dossier ou un message et retourne un pointeur d’interface pour un accès supplémentaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
ms.openlocfilehash: 14bc327a0783cd1517aa4c3684c5cd3378ce8b01
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65827743"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un dossier ou un message et retourne un pointeur d’interface pour un accès supplémentaire. 
  
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
  
> [in] Nombre d’octets dans l’identificateur d’entrée pointé par le paramètre  _lpEntryID_  _._
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir, ou NULL. Si  _lpEntryID_ est défini sur NULL, **OpenEntry** ouvre le dossier racine du magasin de messages. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. La transmission de la valeur NULL entraîne le retour de l’interface standard de l’objet ([IMAPIFolder](imapifolderimapicontainer.md) pour les dossiers et [IMessage](imessageimapiprop.md) pour les messages). 
    
 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet soit ouvert à l’aide des autorisations réseau maximales autorisées pour l’utilisateur et de l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert à l’aide de l’autorisation de lecture/écriture ; si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert à l’aide de l’autorisation en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de retourner correctement, éventuellement avant que l’objet soit entièrement disponible pour le client appelant. Si l’objet n’est pas disponible, l’exécution d’un appel d’objet suivant peut générer une erreur. 
    
MAPI_MODIFY 
  
> Demande l’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule, et les clients ne doivent pas fonctionner en partant du principe que l’autorisation de lecture/écriture est accordée. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’un objet en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été effectuée.
    
MAPI_NO_CACHE
  
> Lorsqu’un magasin est ouvert en mode mis en cache, un client ou un fournisseur de services peut appeler **IMsgStore::OpenEntry**, en définissant l’indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur le magasin distant. Si vous ouvrez le magasin de messages avec l’indicateur MDB_ONLINE sur le serveur distant, vous n’avez pas besoin d’utiliser l’indicateur MAPI_NO_CACHE.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::OpenEntry** ouvre un dossier ou un message et retourne un pointeur vers une interface qui peut être utilisée pour un accès supplémentaire. 
  
> [!IMPORTANT]
> Lorsque vous ouvrez des entrées de dossier sur un magasin public, comme des dossiers et des messages, utilisez **IMsgStore::OpenEntry** au lieu [d’IMAPISession::OpenEntry](imapisession-openentry.md). Cela garantit que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les dossiers et les messages sont ouverts automatiquement avec une autorisation en lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ . La définition de l’un de ces indicateurs ne garantit pas un type particulier d’autorisation ; les autorisations qui vous sont accordées dépendent du fournisseur du magasin de messages, de votre niveau d’accès et de l’objet. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Bien **qu’IMsgStore::OpenEntry** puisse être utilisé pour ouvrir un dossier ou un message, il est généralement plus rapide d’utiliser la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir. 
  
Vérifiez la valeur retournée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné correspond à ce que vous attendiez. Si le type d’objet n’est pas le type attendu, castez le pointeur du paramètre  _lppUnk_ en pointeur du type approprié. Par exemple, si vous ouvrez un dossier, cast  _lppUnk_ en pointeur de type **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMsgStore::OpenEntry** pour ouvrir l’objet associé à un ID d’entrée. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

