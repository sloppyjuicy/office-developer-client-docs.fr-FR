---
title: IMAPIGetSession  IUnknown
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
description: Permet d’accéder à la session MAPI actuelle associée à l’objet de support. Les fournisseurs MAPI peuvent interroger leur objet de support MAPI pour cette interface.
ms.openlocfilehash: 186ebb458cb11e66f37e07324a43217e82f04390
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63764544"
---
# <a name="imapigetsession--iunknown"></a>IMAPIGetSession : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet d’accéder à la session MAPI actuelle associée à l’objet de support. Les fournisseurs MAPI peuvent interroger leur objet de support MAPI pour cette interface. Pour plus d’informations sur les objets de prise en charge, voir [Vue d’ensemble de l’objet Support](support-object-overview.md).
  
|Propriété |Valeur |
|:-----|:-----|
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIGetSession  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[GetMAPISession](imapigetsession-getmapisession.md) <br/> |Appelé pour obtenir un pointeur vers la session MAPI en cours. |
   
## <a name="see-also"></a>Voir aussi



[GetMAPISession](imapigetsession-getmapisession.md)
  
[IMAPISupport](imapisupportiunknown.md)


[Interfaces MAPI](mapi-interfaces.md)
  
[Vue d’ensemble de l’objet support](support-object-overview.md)

