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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 67dac1246a2d01557ce2d6167f5f3eb32cb57a38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592290"
---
# <a name="imapiviewadvisesinkonsubmitted"></a>IMAPIViewAdviseSink::OnSubmitted

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaires que le message actuel a été envoyé aupooler MAPI.
  
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

Après **l’appel de OnSubmitted,** vous pouvez continuer sur l’hypothèse que le message a été mis à jour. Mettez à jour vos fenêtres pour refléter les modifications qui se sont produites. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIMessageSite::SubmitMessage](imapimessagesite-submitmessage.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

