---
title: IProxyStoreObject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IProxyStoreObject
api_type:
- COM
ms.assetid: 567bede4-39a3-bfb4-af85-ba678e2cf4a5
description: Fournit un objet de magasin IMAP qui a été déballé et qui permet d’accéder aux éléments du fichier Dossiers personnels sans télécharger les éléments.
ms.openlocfilehash: c93fb0a1ed3f5b92948eb93b449674518d9f149c
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405782"
---
# <a name="iproxystoreobject"></a>IProxyStoreObject

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fournit un objet de magasin IMAP (Internet Message Access Protocol) qui a été déballé et qui permet d’accéder aux éléments du fichier de dossiers personnels (PST) sans avoir à demander la synchronisation et à télécharger les éléments.
  
## <a name="quick-info"></a>Informations rapides

|Propriété |Valeur |
|:-----|:-----|
|Hérité de :  <br/> |[IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) <br/> |
|Fourni par :  <br/> |Fournisseur de magasin de messages  <br/> |
|Identificateur d’interface :  <br/> |**IID_IProxyStoreObject** <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
|[IProxyStoreObject::UnwrapNoRef](iproxystoreobject-unwrapnoref.md) <br/> |Obtient un pointeur vers un magasin IMAP non enveloppé. |
| *Membre d’espace réservé*  <br/> | *Non pris en charge ou documenté.*  <br/> |
   
## <a name="remarks"></a>Remarques

[Appelez IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur la boutique de messages source pour obtenir l’interface **IProxyStoreObject**. Ensuite, appelez **IProxyStoreObject::UnwrapNoRef** pour obtenir l’objet store non enveloppé. Si **QueryInterface renvoie** **l’erreur MAPI_E_INTERFACE_NOT_SUPPORTED**, le magasin n’a pas été wrapped. 
  
Comme **UnwrapNoRef** n’incrémente pas le nombre de références pour ce nouveau pointeur vers l’objet store non enveloppé, après avoir correctement appelé **UnwrapNoRef**, vous devez appeler [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour conserver le nombre de références. 
  

