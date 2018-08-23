---
title: IProxyStoreObjectUnwrapNoRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject.UnwrapNoRef
api_type:
- COM
ms.assetid: 1122b6e0-e7e1-e68a-e090-435777343d04
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8539f81ed1741063d878da492d925b63c488d1a9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586430"
---
# <a name="iproxystoreobjectunwrapnoref"></a>IProxyStoreObject::UnwrapNoRef

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Obtient un pointeur vers un objet banque IMAP Internet Message Access Protocol () non qui fournit l’accès dans le fichier de dossiers personnels (PST) sous-jacent sans appel de la synchronisation et de télécharger les éléments.
  
```cpp
HRESULT IProxyStoreObject::UnwrapNoRef (     LPVOID *ppvObject ); 
```

## <a name="parameters"></a>Paramètres

 _ppvObject_
  
> [out] Pointeur vers une [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet store qui est non. 
    
## <a name="return-values"></a>Valeurs de retour

S_OK
  
- L’appel a réussi et un pointeur vers une interface non a été renvoyé dans _ppvObject_.
    
## <a name="remarks"></a>Remarques

Sans premier dévoilement une banque IMAP, l’accès à un message dans la banque peut de forcer une synchronisation qui tente de télécharger l’intégralité du message. À l’aide de la banque non permet d’accéder au message dans son état actuel sans déclencher un téléchargement.
  
Étant donné que **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après la réussite de l’appel **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) pour maintenir le décompte de références. 
  
## <a name="see-also"></a>Voir aussi



[IProxyStoreObject](iproxystoreobject.md)

