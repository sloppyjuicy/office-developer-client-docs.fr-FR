---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7be1c8e5162cdc384a157174350f313713b6e33a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630795"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la session MAPI actuelle associée à l’objet de support. Les fournisseurs MAPI peuvent interroger leur objet de support MAPI pour cette interface. Pour plus d’informations sur les objets de prise en charge, voir [Vue d’ensemble de l’objet support.](support-object-overview.md)
  
|||
|:-----|:-----|
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Appelé pour obtenir un pointeur vers la session MAPI en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)
  
[Vue d’ensemble de l’objet support](support-object-overview.md)

