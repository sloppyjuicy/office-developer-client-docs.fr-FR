---
title: IMAPIFormAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIForm.Advise
api_type:
- COM
ms.assetid: 961318d6-bebe-4f4b-98ff-921cafc68d24
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 398644605e3ad1020ce594bc8d74593fdede6ad4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567598"
---
# <a name="imapiformadvise"></a>IMAPIForm::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit une visionneuse de formulaires pour les notifications sur les événements qui affectent le formulaire.
  
```cpp
HRESULT Advise(
  LPMAPIVIEWADVISESINK pAdvise,
  ULONG FAR * pulConnection
);
```

## <a name="parameters"></a>Paramètres

 _pAdvise_
  
> [in] Un pointeur vers une vue conseille à l’objet de réception de recevoir les notifications suivantes. 
    
 _connection_
  
> [out] Pointeur vers une valeur autre que zéro qui représente une inscription de notification réussie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription a réussi.
    
E_OUTOFMEMORY 
  
> L’inscription a échoué en raison d’une mémoire insuffisante.
    
## <a name="remarks"></a>Remarques

Les visionneuses de formulaire appellent la méthode **IMAPIForm::Advise** d’un formulaire pour s’inscrire aux notifications lorsque des modifications sont apportées au formulaire. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Conservez une copie du pointeur de l’avis de vue transmis dans le paramètre  _pAdvise_ afin de pouvoir l’utiliser pour appeler la méthode [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) appropriée lorsqu’un événement se produit. Appelez la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) de l’affichage pour conserver le pointeur jusqu’à l’annulation de l’inscription de la notification. Définissez le contenu du  _paramètreconnection sur_ un nombre autre que zéro. 
  
De nombreux formulaires implémentent un objet d’aide pour gérer l’inscription et la notification ultérieure des événements. 
  
Pour plus d’informations sur le processus de notification en général, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
Pour plus d’informations sur les notifications et les [formulaires,](sending-and-receiving-form-notifications.md)voir Sending and Receiving Form Notifications .
  
## <a name="see-also"></a>Voir aussi



[IMAPIForm::Unadvise](imapiform-unadvise.md)
  
[IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)
  
[IMAPIForm : IUnknown](imapiformiunknown.md)


[Notification d’événement dans MAPI](event-notification-in-mapi.md)
  
[Envoi et réception de notifications de formulaire](sending-and-receiving-form-notifications.md)

