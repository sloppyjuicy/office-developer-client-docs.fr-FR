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
ms.openlocfilehash: 2ec78331fd013777f001d39bd7e978a67abb5342
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407605"
---
# <a name="imapiviewadvisesinkonsaved"></a>IMAPIViewAdviseSink::OnSaved

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit la visionneuse de formulaires que le message actif d'un formulaire a été enregistré.
  
```cpp
HRESULT OnSaved( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Un objet Form appelle la méthode **IMAPIViewAdviseSink:: OnSaved** une fois que le message actif dans un formulaire a été enregistré avec succès. Cela permet aux utilisateurs de mettre à jour leurs fenêtres afin de refléter les modifications apportées au message. 
  
Pour plus d'informations sur les notifications de formulaire, consultez la rubrique [envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)

