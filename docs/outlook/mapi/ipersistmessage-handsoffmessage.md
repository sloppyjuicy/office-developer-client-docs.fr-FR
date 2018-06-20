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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fd7e3b1d1284cdf4451330aabcce8fd0279ad5ba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784354"
---
# <a name="ipersistmessagehandsoffmessage"></a>IPersistMessage::HandsOffMessage

  
  
**S’applique à**: Outlook 
  
Le formulaire libérer le message en cours.
  
```cpp
HRESULT HandsOffMessage( void );
```

## <a name="parameters"></a>Paramètres

Aucune
  
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Le message a été publié correctement.
    
## <a name="remarks"></a>Remarques

Transition de formulaires dans les deux États HandsOff :
  
- [HandsOffAfterSave](handsoffaftersave-state.md)
    
- [HandsOffFromNormal](handsofffromnormal-state.md)
    
Lorsqu’un formulaire est dans un de ces États, il est en stocké de façon permanente. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Lorsqu’une visionneuse de formulaire appelle la méthode **IPersistMessage::HandsOffMessage** lorsque votre formulaire est dans un état [Normal](normal-state.md) ou [NoScribble](noscribble-state.md) , de manière récursive appel **HandsOffMessage** sur chaque message incorporé dans le message en cours et la [ IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) méthode sur chaque objet OLE incorporé dans le message en cours. Puis relâchez le message actuel et les messages incorporés et les objets OLE. Si votre formulaire a été dans son état Normal, la transition vers l’état HandsOffFromNormal. Si votre formulaire était dans l’état NoScribble, effectuer la transition à l’état HandsOffAfterSave. Après une transition réussie, appelez la méthode [IUnknown::Release](http://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) du message et qu’elles retournent S_OK. 
  
Lorsqu’un utilisateur du formulaire appelle **HandsOffMessage** votre formulaire est ouvert dans un des États HandsOff, retourner E_UNEXPECTED. 
  
Pour plus d’informations sur les différents États d’un formulaire, voir [Les États de formulaire](form-states.md). Pour plus d’informations sur l’utilisation de l’état HandsOff des objets de stockage, voir la méthode [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d.aspx) . 
  
## <a name="see-also"></a>Voir aussi



[IPersistMessage : IUnknown](ipersistmessageiunknown.md)


[États de formulaire](form-states.md)

