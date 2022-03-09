---
title: IMAPIViewAdviseSinkOnSubmitted
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnSubmitted
api_type:
- COM
ms.assetid: a2401662-1ddc-40d8-a5a7-ceca24442bd4
ms.openlocfilehash: 771339b5b215d016be337f3f35334439bc45a863
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371526"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaire que le message actuel a été envoyé aupooler MAPI.
  
```cpp
HRESULT OnSubmitted( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

Un objet de formulaire appelle la méthode **IMAPIViewAdviseSink::OnSubmitted** après qu’un appel à [IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md) a été renvoyé avec succès. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Après **avoir appelé OnSubmitted** , vous pouvez continuer sur l’hypothèse que le message a été mis à jour. Mettez à jour vos fenêtres pour refléter les modifications qui se sont produites. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

