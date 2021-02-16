---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 485d3f3cd4b6be4748a2ebf2ba0d0b71f691478f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315518"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un objet de magasin IMAP (Internet Message Access Protocol) qui a été déballé et qui permet d’accéder aux éléments du fichier de dossiers personnels (PST) sans avoir à demander la synchronisation et à télécharger les éléments.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérité de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de magasin de messages  <br/> |
|Identificateur d’interface :  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtient un pointeur vers un magasin IMAP non enveloppé.  <br/> |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
   
## <a name="remarks"></a>Remarques

Appelez [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur la boutique de messages source pour obtenir l’interface **IProxyStoreObject.** Ensuite, **appelez IProxyStoreObject::UnwrapNoRef** pour obtenir l’objet store non enveloppé. Si **QueryInterface renvoie** l’erreur **MAPI_E_INTERFACE_NOT_SUPPORTED**, le magasin n’a pas été wrapped. 
  
Étant donné que **UnwrapNoRef** n’incrémente pas le nombre de références pour ce nouveau pointeur vers l’objet store non enveloppé, après avoir correctement appelé **UnwrapNoRef,** vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour conserver le nombre de références. 
  

