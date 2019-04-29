---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0b861a11b6bc1d590225a0c99b20f8be38edfd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436649"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d'accéder à la session MAPI actuelle associée à l'objet support. Les fournisseurs MAPI peuvent interroger leur objet de prise en charge MAPI pour cette interface. Pour plus d'informations sur les objets de prise en charge, voir [support Object Overview](support-object-overview.md).
  
|||
|:-----|:-----|
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Appelé pour obtenir un pointeur vers la session MAPI actuelle.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)
  
[Vue d'ensemble de l'objet support](support-object-overview.md)

