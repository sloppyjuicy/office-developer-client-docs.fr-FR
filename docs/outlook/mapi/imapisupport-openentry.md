---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409614"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet et renvoie un pointeur d’interface pour un accès supplémentaire. 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
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
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet. La transmission DE NULL entraîne le retour de l’interface standard de l’objet. Par exemple, si l’objet à ouvrir est un message, l’interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il s’agit [de IMAPIFolder](imapifolderimapicontainer.md). Les interfaces standard pour les objets de carnet d’adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulOpenFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définies :
    
MAPI_BEST_ACCESS 
  
> Demande l’ouverture de l’objet avec les autorisations réseau maximales autorisées pour l’appelant. Par exemple, si l’appelant dispose d’une autorisation de lecture/écriture, l’objet doit être ouvert en lecture/écriture . Si l’appelant dispose d’une autorisation en lecture seule, l’objet doit être ouvert en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de renvoyer correctement, éventuellement avant que l’objet soit entièrement accessible à l’appelant. Si l’objet n’est pas accessible, un appel d’objet ultérieur peut entraîner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation de lecture/écriture. Par défaut, les objets sont ouverts en lecture seule et les appelants ne doivent pas travailler sur l’hypothèse que l’autorisation lecture/écriture a été accordée. 
    
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
  
> L’identificateur d’entrée transmis dans le paramètre  _lpEntryID_ est dans un format non reconnu. Cette valeur est généralement renvoyée si le fournisseur de carnet d’adresses qui contient l’objet n’est pas ouvert. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::OpenEntry** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services **appellent IMAPISupport::OpenEntry** pour récupérer un pointeur vers une interface qui peut être utilisée pour accéder à un objet particulier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **IMAPISupport::OpenEntry** uniquement lorsque vous ne connaissez pas le type d’objet que vous ouvrez. Si vous savez que vous ouvrez un dossier ou un message, appelez [IMsgStore::OpenEntry](imsgstore-openentry.md) à la place. Si vous savez que vous ouvrez un conteneur de carnet d’adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook::OpenEntry](iaddrbook-openentry.md). Ces méthodes plus spécifiques sont plus rapides que **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** ouvre tous les objets en lecture seule, sauf si vous définissez l’indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre  _ulFlags_ et si vos autorisations sont suffisantes. La définition de l’un de ces indicateurs ne garantit pas un type d’accès particulier ; Les autorisations qui vous sont accordées dépendent de votre niveau d’accès, de l’objet et du fournisseur de services qui détient l’objet. Pour déterminer le niveau d’accès de l’objet ouvert, récupérez PR_ACCESS_LEVEL **propriété** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Vérifiez la valeur renvoyée dans  _le paramètre lpulObjType_ pour déterminer que le type d’objet renvoyé est ce que vous attendiez. Si le type d’objet est comme prévu, cast le pointeur du paramètre  _lppUnk_ vers un pointeur du type approprié. Par exemple, si vous ouvrent un dossier, cast  _lppUnk_ vers un pointeur de type LPMAPIFOLDER. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

