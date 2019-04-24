---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309694"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un dossier ou un message et renvoie un pointeur d'interface pour un accès supplémentaire. 
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ _._
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir ou valeur NULL. Si _lpEntryID_ est défini sur null, **OpenEntry** ouvre le dossier racine de la Banque de messages. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet ouvert. Le passage des résultats de la valeur NULL dans l'interface standard de l'objet ([IMAPIFolder](imapifolderimapicontainer.md) pour les dossiers et [IMessage](imessageimapiprop.md) pour les messages) est renvoyé. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être utilisés:
    
MAPI_BEST_ACCESS 
  
> Demande l'ouverture de l'objet à l'aide des autorisations réseau maximales autorisées pour l'utilisateur et de l'accès à l'application cliente maximale. Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert à l'aide de l'autorisation de lecture/écriture; Si le client dispose d'une autorisation en lecture seule, l'objet doit être ouvert à l'aide de l'autorisation en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit entièrement disponible pour le client appelant. Si l'objet n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule, et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture est accordée. 
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur vers l'objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d'un objet en lecture seule ou d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.
    
MAPI_NO_CACHE
  
> Lorsqu'un magasin est ouvert en mode mis en cache, un client ou un fournisseur de services peut appeler **IMsgStore:: OpenEntry**, en définissant l'indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur le magasin distant. Si vous ouvrez la Banque de messages avec l'indicateur MDB_ONLINE sur le serveur distant, il n'est pas nécessaire d'utiliser l'indicateur MAPI_NO_CACHE.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore:: OpenEntry** ouvre un dossier ou un message et renvoie un pointeur vers une interface qui peut être utilisée pour un accès supplémentaire. 
  
> [!IMPORTANT]
> Lors de l'ouverture d'entrées de dossier dans une banque publique, telles que des dossiers et des messages, utilisez **IMsgStore:: OpenEntry** au lieu de [IMAPISession:: OpenEntry](imapisession-openentry.md). Cela permet de s'assurer que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les dossiers et les messages sont automatiquement ouverts en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ . Le fait de définir l'un de ces indicateurs ne garantit pas un type d'autorisation particulier; les autorisations que vous êtes accordé dépendent du fournisseur de banque de messages, de votre niveau d'accès et de l'objet. Pour déterminer le niveau d'accès de l'objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Bien que **IMsgStore:: OpenEntry** puisse être utilisé pour ouvrir un dossier ou un message, il est généralement plus rapide d'utiliser la méthode [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir. 
  
Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d'objet renvoyé est celui que vous attendiez. Si le type d'objet n'est pas le type attendu, castez le pointeur du paramètre _lppUnk_ en pointeur du type approprié. Par exemple, si vous ouvrez un dossier, castez _lppUnk_ en pointeur de type **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMsgStore:: OpenEntry** pour ouvrir l'objet associé à un ID d'entrée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

