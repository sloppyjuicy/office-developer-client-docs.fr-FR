---
title: IPersistMessageHandsOffMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.HandsOffMessage
api_type:
- COM
ms.assetid: 0e56b21d-0a2e-4fe6-83f4-c9daab2f3055
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 84f0ca88403980ff9ea1c91821a8a3d7edae74fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309715"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Fait en sorte que le formulaire libère son message actuel.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucun
  
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Le message a été correctement libéré.
    
## <a name="remarks"></a>Remarques

Les formulaires se transforment en deux états HandsOff :
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Lorsqu’un formulaire se trouve dans l’un de ces états, il est en cours de stock permanent. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsqu’une visionneuse de formulaire appelle la méthode **IPersistMessage::HandsOffMessage** alors que votre formulaire est à l’état [Normal](normal-state.md) ou [NoScribble,](noscribble-state.md) appelez de manière récursive **HandsOffMessage** sur chaque message incorporé dans le message actuel et la méthode [IPersistStorage::HandsOffStorage](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) sur chaque objet OLE incorporé dans le message actuel. Ensuite, relâchez le message actuel, ainsi que tous les messages incorporés et les objets OLE. Si votre formulaire était dans l’état Normal, transition vers l’état HandsOffFromNormal. Si votre formulaire était dans l’état NoScribble, transition vers l’état HandsOffAfterSave. Après une transition réussie, appelez la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) du message et renvoyez S_OK. 
  
Lorsqu’une visionneuse de formulaire appelle **HandsOffMessage** alors que votre formulaire est dans l’un des états HandsOff, renvoyez E_UNEXPECTED. 
  
Pour plus d’informations sur les différents états d’un formulaire, voir [États de formulaire.](form-states.md) Pour plus d’informations sur l’utilisation de l’état HandsOff des objets de stockage, voir la méthode [IPersistStorage::HandsOffStorage.](https://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[États de formulaire](form-states.md)

