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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: cd93866ae8823eb5897318fc2dda4e8432d974b0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578464"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ouvre un objet dans le conteneur, en retournant un pointeur d’interface pour l’accès des autres.
  
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
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet à ouvrir. Si _lpEntryID_ est défini sur NULL, le conteneur de niveau supérieur dans la hiérarchie du conteneur est ouvert. 
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) qui représente l’interface à utiliser pour accéder à l’objet. Transmission NULL génère l’identificateur de l’interface standard de l’objet retourné. Pour les messages, l’interface standard est [IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md); pour les dossiers, il est [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Pour les objets de carnet d’adresses sont des interfaces de la norme [IDistList : IMAPIContainer](idistlistimapicontainer.md) pour une liste de distribution et [IMailUser : IMAPIProp](imailuserimapiprop.md) pour un utilisateur de messagerie. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont l’objet est ouvert. Les indicateurs suivants peuvent être définis :
    
MAPI_BEST_ACCESS 
  
> Demande que l’objet est ouvert avec les autorisations de réseau maximale autorisées pour l’accès des utilisateurs et le nombre maximal de clients application. Par exemple, si le client a l’autorisation de lecture/écriture, l’objet doit être ouvert avec l’autorisation de lecture/écriture ; Si le client dispose d’un accès en lecture seule, l’objet doit être ouvert avec accès en lecture seule. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet **OpenEntry** renvoyer avec succès, éventuellement, avant de l’objet est entièrement disponible au client appelant. Si l’objet n’est pas disponible, l’émission d’un appel d’objet suivantes peut déclencher une erreur. 
    
N' 
  
> Demandes d’autorisation de lecture/écriture. Par défaut, les objets sont ouverts avec un accès en lecture seule et clients ne doivent pas fonctionner en supposant que bénéficie des autorisations en lecture/écriture. 
    
SHOW_SOFT_DELETES
  
> Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.
    
 _lpulObjType_
  
> [out] Pointeur vers le type de l’objet ouvert.
    
 _lppUnk_
  
> [out] Pointeur vers un pointeur vers l’implémentation d’interface à utiliser pour accéder à l’objet ouvert.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’objet a été ouvert avec succès.
    
MAPI_E_NO_ACCESS 
  
> L’utilisateur dispose des autorisations suffisantes pour ouvrir l’objet ou un utilisateur a tenté d’ouvrir un objet en lecture seule avec une autorisation en lecture-écriture.
    
MAPI_E_NOT_FOUND 
  
> L’identificateur d’entrée spécifié par _lpEntryID_ ne représente pas un objet. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> L’identificateur d’entrée dans le paramètre _lpEntryID_ n’est pas un format reconnu par le conteneur. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIContainer::OpenEntry** ouvre un objet dans un conteneur et retourne un pointeur vers une implémentation de l’interface à utiliser pour l’accès des autres. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Étant donné que les fournisseurs de services ne sont pas tenus de retourner une implémentation de l’interface du type spécifié par l’identificateur d’interface dans le paramètre _lpInterface_ , vérifiez la valeur indiquée par le paramètre _lpulObjType_ . Si nécessaire, effectuer un cast du pointeur renvoyé dans _lppUnk_ à un pointeur du type approprié. 
  
Par défaut, les fournisseurs de services ouvrent des objets avec accès en lecture seule, sauf si vous définissez l’indicateur MAPI_BEST_ACCESS ou ne. Lorsqu’une de ces indicateurs est définie, essaient de fournisseurs de services renvoyer un objet modifiable. Toutefois, ne supposent que vous avez demandé un objet modifiable que l’objet ouvert a l’autorisation de lecture/écriture. Soit prévoir le risque d’une modification ultérieure échec ou récupérer la propriété l’objet **PR_ACCESS_LEVEL** déterminer le niveau d’accès accordé par **OpenEntry**.
  
## <a name="see-also"></a>Voir aussi



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

