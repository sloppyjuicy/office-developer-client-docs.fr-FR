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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409334"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un dossier ou un message et renvoie un pointeur d’interface pour un accès supplémentaire. 
  
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
  
> [in] Nombre d’bytes dans l’identificateur d’entrée pointé par  _le paramètre lpEntryID_  _._
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir, ou NULL. Si  _lpEntryID_ est définie sur NULL, **OpenEntry** ouvre le dossier racine de la magasin de messages. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. La transmission DE NULL entraîne le retour de l’interface standard de l’objet[(IMAPIFolder](imapifolderimapicontainer.md) pour les dossiers et [IMessage](imessageimapiprop.md) pour les messages). 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande l’ouverture de l’objet à l’aide des autorisations réseau maximales autorisées pour l’utilisateur et de l’accès maximal à l’application cliente. Par exemple, si le client dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert à l’aide d’une autorisation de lecture/écriture . Si le client dispose d’une autorisation en lecture seule, l’objet doit être ouvert à l’aide d’une autorisation en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de renvoyer correctement, éventuellement avant que l’objet soit entièrement disponible pour le client appelant. Si l’objet n’est pas disponible, effectuer un appel d’objet ultérieur peut occasioner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec une autorisation en lecture seule et les clients ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture est accordée. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’un objet en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_NO_CACHE
  
> Lorsqu’une boutique est ouverte en mode mis en cache, un client ou un fournisseur de services peut appeler **IMsgStore::OpenEntry**, en paramétrie de l’indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur la boutique distante. Si vous ouvrez la magasin de messages avec l’indicateur MDB_ONLINE sur le serveur distant, vous n’avez pas besoin d’utiliser l’MAPI_NO_CACHE de messagerie.
    
## <a name="remarks"></a>Remarques

La **méthode IMsgStore::OpenEntry** ouvre un dossier ou un message et renvoie un pointeur vers une interface qui peut être utilisée pour un accès supplémentaire. 
  
> [!IMPORTANT]
> Lors de l’ouverture d’entrées de dossiers dans une boutique publique, telles que des dossiers et des messages, utilisez **IMsgStore::OpenEntry** au lieu d’IMAPISession::OpenEntry . [](imapisession-openentry.md) Cela garantit que les dossiers publics fonctionnent correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Les dossiers et messages sont automatiquement ouverts avec une autorisation de lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags._ La définition de l’un de ces indicateurs ne garantit pas un type d’autorisation particulier ; Les autorisations qui vous sont accordées dépendent du fournisseur de la boutique de messages, de votre niveau d’accès et de l’objet. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Bien que **IMsgStore::OpenEntry** puisse être utilisé pour ouvrir n’importe quel dossier ou message, il est généralement plus rapide d’utiliser la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir. 
  
Vérifiez la valeur renvoyée dans le  _paramètre lpulObjType_ pour déterminer si le type d’objet renvoyé est ce que vous attendiez. Si le type d’objet n’est pas le type attendu, cast le pointeur du paramètre  _lppUnk_ vers un pointeur du type approprié. Par exemple, si vous ouvrent un dossier, cast  _lppUnk_ vers un pointeur de type **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMsgStore::OpenEntry** pour ouvrir l’objet associé à un ID d’entrée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

