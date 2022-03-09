---
title: IMsgStoreNotifyNewMail
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMsgStore.NotifyNewMail
api_type:
- COM
ms.assetid: d0d003b0-f12f-4422-b71f-26886169461f
ms.openlocfilehash: cc1c390d94a3ac3f678d9403281a4163272af08a
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63377518"
---
# <a name="imsgstorenotifynewmail"></a>IMsgStore::GetReceiveFolderTable

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Informe la banque de messages un nouveau message est arriv�. Cette m�thode est appel�e uniquement par le spouleur MAPI.
  
```cpp
HRESULT NotifyNewMail(
  LPNOTIFICATION lpNotification
);
```

## <a name="parameters"></a>Paramètres

 _lpNotification_
  
> [in] Pointeur vers une structure [NOTIFICATION](notification.md) qui d�crit la notification de nouveau message. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La banque de messages a �t� correctement inform�e.
    
## <a name="remarks"></a>Remarques

La m�thode **IMsgStore::NotifyNewMail** est appel�e par le spouleur MAPI pour informer la banque de messages qu'un message est pr�t pour la livraison. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Lorsque **NotifyNewMail** est appel�, envoyer une notification de nouveau courrier � tous les clients inscrits. Vous pouvez envoyer la notification en appelant [IMAPISupport::Notify](imapisupport-notify.md), si vous choisissez d'utiliser les m�thodes de l'objet de prise en charge, ou � l'aide de votre propre impl�mentation. Un client enregistr� est celui qui a appel� [IMsgStore::Advise](imsgstore-advise.md) et d�finissez le param�tre  _lpEntryID_ NULL et le param�tre  _ulEventMask_ pour  _fnevNewMail_. 
  
Ne modifiez pas ou ne lib�rer de la m�moire pour la structure [NOTIFICATION](notification.md) qui d�crit la notification de nouveau courrier. Copiez la structure **NOTIFICATION** en appelant la fonction utilitaire [ScCopyNotifications](sccopynotifications.md) pour rendre utilisent les informations de ses membres. 
  
## <a name="see-also"></a>Voir aussi



[IMAPISupport::Subscribe](imapisupport-subscribe.md)
  
[IMAPISupport::Unsubscribe](imapisupport-unsubscribe.md)
  
[Notification](notification.md)
  
[ScCopyNotifications](sccopynotifications.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)

