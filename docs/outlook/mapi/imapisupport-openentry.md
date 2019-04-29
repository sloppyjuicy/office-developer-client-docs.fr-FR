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
  
Ouvre un objet et renvoie un pointeur d'interface pour un accès supplémentaire. 
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet. La transmission de la valeur NULL entraîne le renvoi de l'interface standard de l'objet. Par exemple, si l'objet à ouvrir est un message, l'interface standard est [IMessage](imessageimapiprop.md); pour les dossiers, il s'agit de [IMAPIFolder](imapifolderimapicontainer.md). Les interfaces standard pour les objets de carnet d'adresses sont [IDistList](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulOpenFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS 
  
> Demande que l'objet soit ouvert avec les autorisations réseau maximales accordées à l'appelant. Par exemple, si l'appelant dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert en lecture/écriture; Si l'appelant dispose d'une autorisation en lecture seule, l'objet doit être ouvert en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit totalement accessible à l'appelant. Si l'objet n'est pas accessible, un appel d'objet ultérieur peut entraîner une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts en lecture seule, et les appelants ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur vers l'objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d'un objet en lecture seule s'est produite ou une tentative d'accès à un objet pour lequel l'utilisateur ne dispose pas des autorisations suffisantes a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> Il n'y a pas d'objet associé à l'identificateur d'entrée passé dans le paramètre _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Le format de l'identificateur d'entrée transmis dans le paramètre _lpEntryID_ n'est pas reconnu. Cette valeur est généralement renvoyée si le fournisseur de carnet d'adresses qui contient l'objet n'est pas ouvert. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: OpenEntry** est implémentée pour tous les objets de prise en charge du fournisseur de services. Les fournisseurs de services appellent **IMAPISupport:: OpenEntry** pour récupérer un pointeur vers une interface qui peut être utilisé pour accéder à un objet particulier. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez **IMAPISupport:: OpenEntry** uniquement lorsque vous ne connaissez pas le type d'objet que vous ouvrez. Si vous êtes sûr que vous ouvrez un dossier ou un message, appelez [IMsgStore:: OpenEntry](imsgstore-openentry.md) à la place. Si vous êtes certain que vous ouvrez un conteneur de carnet d'adresses, un utilisateur de messagerie ou une liste de distribution, appelez [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Ces méthodes plus spécifiques sont plus rapides que **IMAPISupport:: OpenEntry**. 
  
 **IMAPISupport:: OpenEntry** ouvre tous les objets en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS dans le paramètre _ulFlags_ et que vos autorisations sont suffisantes. Le fait de définir l'un de ces indicateurs ne garantit pas un type d'accès particulier; les autorisations que vous êtes accordé dépendent de votre niveau d'accès, de l'objet et du fournisseur de services qui possède l'objet. Pour déterminer le niveau d'accès de l'objet ouvert, récupérez sa propriété **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Vérifiez la valeur renvoyée dans le paramètre _lpulObjType_ pour déterminer que le type d'objet renvoyé est ce que vous attendiez. Si le type d'objet est comme prévu, castez le pointeur du paramètre _lppUnk_ en pointeur du type approprié. Par exemple, si vous ouvrez un dossier, castez _lppUnk_ en pointeur de type LPMAPIFOLDER. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport : IUnknown](imapisupportiunknown.md)

