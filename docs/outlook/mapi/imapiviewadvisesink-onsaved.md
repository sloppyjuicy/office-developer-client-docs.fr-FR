---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1ae94b40d984adee0f3c888f69dfdbffb1e352e1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584435"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaire le message actuel dans un formulaire a été enregistré.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet form appelle la méthode **IMAPIViewAdviseSink::OnSaved** une fois que le message actuel dans un formulaire a été enregistré avec succès. Cela permet de visionneuses pour mettre à jour leurs windows pour refléter les modifications apportées au message. 
  
Pour plus d’informations sur les notifications de formulaire, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

