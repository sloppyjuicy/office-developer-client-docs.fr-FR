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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 611680db87c02b9370d6c1b3ac7a8d68b47f3050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574026"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre un dossier ou un message et retourne un pointeur d’interface pour l’accès des autres. 
  
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
  
> [in] Le nombre d’octets dans l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ _._
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir ou valeur NULL. Si _lpEntryID_ est défini sur NULL, **OpenEntry** ouvre le dossier racine de la banque de messages. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet ouvert. NULL de transmission des résultats de l’objet de l’interface standard ([IMAPIFolder](imapifolderimapicontainer.md) pour des dossiers) et [IMessage](imessageimapiprop.md) pour les messages renvoyé. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être utilisés :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet s’ouvre avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert à l’aide de l’autorisation de lecture/écriture ; Si le client dispose des autorisations en lecture seule, l’objet doit être ouvert à l’aide des autorisations en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenEntry** renvoyer avec succès, éventuellement, avant de l’objet est entièrement disponible au client appelant. Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec l’autorisation en lecture seule et clients ne doivent pas fonctionner en supposant que l’autorisation est accordée en lecture/écriture. 
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a été effectuée pour modifier un objet en lecture seule ou pour accéder à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes.
    
MAPI_NO_CACHE
  
> Lorsqu’une banque est ouvert en mode mis en cache, un client ou fournisseur de services peut appeler **IMsgStore::OpenEntry**, l’indicateur MAPI_NO_CACHE pour ouvrir un élément ou un dossier sur le magasin distant. Si vous ouvrez la banque de messages avec l’indicateur MDB_ONLINE sur le serveur distant, vous n’avez pas d’utiliser l’indicateur MAPI_NO_CACHE.
    
## <a name="remarks"></a>Remarques

La méthode **IMsgStore::OpenEntry** ouvre un dossier ou un message et retourne un pointeur vers une interface qui peut être utilisée pour l’accès des autres. 
  
> [!IMPORTANT]
> Lors de l’ouverture des entrées de dossier sur un magasin public, telles que les dossiers et messages, utilisez **IMsgStore::OpenEntry** au lieu de [IMAPISession::OpenEntry](imapisession-openentry.md). Ainsi, cette fonction de dossiers publics correctement lorsque plusieurs comptes Exchange sont définis dans un profil. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Dossiers et messages sont automatiquement ouverts avec des autorisations en lecture seule, sauf si vous définissez l’indicateur n’ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ . Définition de l’une de ces indicateurs ne garantit pas un type particulier d’autorisation ; les autorisations qui vous sont accordées dépendent de l’objet, votre niveau d’accès et le fournisseur de banque de messages. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Bien que **IMsgStore::OpenEntry** peut être utilisé pour ouvrir un dossier ou un message, il est généralement plus rapide d’utiliser la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) si vous avez accès au dossier parent du dossier ou du message à ouvrir. 
  
Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer si le type d’objet retourné est attendue. Si le type d’objet n’est pas le type attendu, convertir le pointeur à partir du paramètre _lppUnk_ vers un pointeur du type approprié. Par exemple, si vous ouvrez un dossier, un cast _lppUnk_ à un pointeur du type **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI utilise la méthode **IMsgStore::OpenEntry** pour ouvrir l’objet associé à un ID d’entrée.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

