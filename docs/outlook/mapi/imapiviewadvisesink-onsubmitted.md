---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2aa1aca2816b8f0e148d35d1fcec761f621a2239
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579444"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que le message en cours a été soumis au spouleur MAPI à la visionneuse de formulaire.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Un objet form appelle la méthode **IMAPIViewAdviseSink::OnSubmitted** après qu’un appel à [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) a réussi. 
  
## <a name="notes-to-implementers"></a>Remarques à l’attention des responsables de l’implémentation

Après avoir appelé **OnSubmitted** , vous pouvez continuer sur l’hypothèse que le message a été mis à jour. Mettre à jour votre windows afin de refléter les modifications qui se sont produites. 
  
Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

