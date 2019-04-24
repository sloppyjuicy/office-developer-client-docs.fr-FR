---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9598e0c90c16db14cdc3a46d2b2ae74e0d9a9300
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286931"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ouvre un objet dans le conteneur, en renvoyant un pointeur d'interface pour un accès supplémentaire.
  
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
  
> dans Nombre d'octets dans l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée de l'objet à ouvrir. Si _lpEntryID_ est défini sur null, le conteneur de niveau supérieur dans la hiérarchie du conteneur est ouvert. 
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) qui représente l'interface à utiliser pour accéder à l'objet. La transmission de la valeur NULL entraîne le renvoi de l'interface standard de l'objet. Pour les messages, l'interface standard est [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); pour les dossiers, il s'agit de [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). Les interfaces standard pour les objets de carnet d'adresses sont [IDistList: IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser: IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'ouverture de l'objet. Les indicateurs suivants peuvent être définis:
    
MAPI_BEST_ACCESS 
  
> Demande que l'objet soit ouvert avec les autorisations réseau maximales accordées à l'utilisateur et l'accès maximal de l'application cliente. Par exemple, si le client dispose d'une autorisation en lecture/écriture, l'objet doit être ouvert avec une autorisation en lecture/écriture; Si le client dispose d'un accès en lecture seule, l'objet doit être ouvert avec un accès en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **OpenEntry** de retourner correctement, éventuellement avant que l'objet soit entièrement disponible pour le client appelant. Si l'objet n'est pas disponible, un appel d'objet ultérieur peut déclencher une erreur. 
    
MAPI_MODIFY 
  
> Demande une autorisation en lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule et les clients ne doivent pas travailler en supposant que l'autorisation de lecture/écriture a été octroyée. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme étant supprimés de manière récupérable, c'est-à-dire qu'ils se trouvent dans la phase de durée de rétention des éléments supprimés.
    
 _lpulObjType_
  
> remarquer Pointeur vers le type de l'objet ouvert.
    
 _lppUnk_
  
> remarquer Pointeur vers un pointeur vers l'implémentation de l'interface à utiliser pour accéder à l'objet ouvert.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> Soit l'utilisateur ne dispose pas des autorisations suffisantes pour ouvrir l'objet, soit une tentative d'ouverture d'un objet en lecture seule avec une autorisation en lecture/écriture a été effectuée.
    
MAPI_E_NOT_FOUND 
  
> L'identificateur d'entrée spécifié par _lpEntryID_ ne représente pas un objet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L'identificateur d'entrée dans le paramètre _lpEntryID_ n'est pas un format reconnu par le conteneur. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer:: OpenEntry** ouvre un objet dans tout un conteneur et renvoie un pointeur vers une implémentation d'interface à utiliser pour un accès supplémentaire. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que les fournisseurs de services ne sont pas tenus de retourner une implémentation d'interface du type spécifié par l'identificateur d'interface dans le paramètre _lpInterface_ , vérifiez la valeur pointée par le paramètre _lpulObjType_ . Si nécessaire, effectuez un cast du pointeur renvoyé dans _lppUnk_ vers un pointeur du type approprié. 
  
Par défaut, les fournisseurs de services ouvrent des objets avec un accès en lecture seule, sauf si vous définissez l'indicateur MAPI_MODIFY ou MAPI_BEST_ACCESS. Lorsque l'un de ces indicateurs est défini, les fournisseurs de services tentent de renvoyer un objet modifiable. Toutefois, ne partez pas du principe que vous avez demandé un objet modifiable que l'objet ouvert dispose d'une autorisation en lecture/écriture. Planifiez la possibilité d'une modification ultérieure de l'échec ou récupérez la propriété **PR_ACCESS_LEVEL** de l'objet pour déterminer le niveau d'accès accordé par **OpenEntry**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

