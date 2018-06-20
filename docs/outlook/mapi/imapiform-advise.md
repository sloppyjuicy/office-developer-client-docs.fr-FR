---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b5347205e10b44d62a7e11cbe2f4179970f1bd64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783744"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**S’applique à**: Outlook 
  
Enregistre une visionneuse de formulaire pour les notifications concernant les événements qui affectent le formulaire.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Paramètres

 _pAdvise_
  
> [in] Un pointeur vers un affichage de notification objet sink de recevoir des notifications ultérieures. 
    
 _pulConnection_
  
> [out] Pointeur vers une valeur différente de zéro qui représente un enregistrement de notification réussie.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’inscription a réussi.
    
E_OUTOFMEMORY 
  
> L’enregistrement a échoué en raison de mémoire insuffisante.
    
## <a name="remarks"></a>Remarques

Visionneuses de formulaire appellent méthode de **IMAPIForm::Advise** d’un formulaire à l’enregistrement d’une notification lorsque des modifications se produisent au formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Conserver une copie de l’affichage de notification pointeur du récepteur transmis dans le paramètre _pAdvise_ afin que vous pouvez l’utiliser pour appeler la méthode [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) appropriée lorsqu’un événement se produit. Appel de l’affichage de notification méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) du récepteur conserver le pointeur jusqu'à l’annulation de l’inscription aux notifications. Définir le contenu du paramètre _pulConnection_ à un nombre différent de zéro. 
  
De nombreux formulaires implémentent un objet d’assistance pour gérer l’enregistrement et la notification ultérieure d’événements. 
  
Pour plus d’informations sur le processus de notification en général, voir [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur les formulaires et de notification, consultez [envoi et réception des Notifications](sending-and-receiving-form-notifications.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notification d’événement MAPI](event-notification-in-mapi.md)
  
[Envoyer et recevoir des Notifications de formulaire](sending-and-receiving-form-notifications.md)

