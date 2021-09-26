---
title: IMAPIViewAdviseSinkOnSaved
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIViewAdviseSink.OnSaved
api_type:
- COM
ms.assetid: c327e31a-7b62-4e21-9b69-b27442f1eaca
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 6b9fbb2eae00357fdc99965b2668f74246d44dd4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620813"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaire que le message en cours dans un formulaire a été enregistré.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet de formulaire appelle la méthode **IMAPIViewAdviseSink::OnSaved** une fois que le message en cours dans un formulaire a été enregistré avec succès. Cela permet aux visiteurs de mettre à jour leurs fenêtres pour refléter les modifications apportées au message. 
  
Pour plus d’informations sur les notifications de formulaire, voir [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

