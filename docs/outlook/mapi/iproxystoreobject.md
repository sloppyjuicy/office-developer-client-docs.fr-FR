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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395307"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un objet de banque IMAP Internet Message Access Protocol () qui a été non et qui permet d’accéder aux éléments dans le fichier de dossiers personnels (PST) sans appel de la synchronisation et de télécharger les éléments.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Hérité :  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de banque de messages  <br/> |
|Identificateur de l’interface :  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtient un pointeur vers une banque IMAP non.  <br/> |
| *Membres de l’espace réservé*  <br/> | *Non pris en charge ou documentés.*  <br/> |
   
## <a name="remarks"></a>Remarques

Appeler [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur la banque de messages source pour obtenir l’interface **IProxyStoreObject** . Appelez ensuite **IProxyStoreObject::UnwrapNoRef** pour obtenir l’objet store non. Si **QueryInterface** renvoie l’erreur **MAPI_E_INTERFACE_NOT_SUPPORTED**, puis la banque n’a pas été encapsulée. 
  
Étant donné que **UnwrapNoRef** n’incrémente pas le décompte de références pour ce nouveau pointeur à l’objet store non, après la réussite de l’appel **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour maintenir le décompte de références. 
  

