---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2b09596fda35b85b753180ecf4c4b47c92c491a8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59561487"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Enregistre un objet auprès d’un fournisseur de magasins de messages pour les notifications concernant les modifications apportées à la boutique de messages. La boutique de messages envoie ensuite des notifications concernant les modifications apportées à l’objet inscrit.
  
```cpp
HRESULT Advise(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulEventMask,
  LPMAPIADVISESINK lpAdviseSink,
  ULONG FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _cbEntryID_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par _le paramètre lpEntryID._ 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées. Cet objet peut être un dossier, un message ou tout autre objet de la boutique de messages. Sinon, si MAPI définit le paramètre  _cbEntryID_ sur 0 et transmet la valeur **null** pour  _lpEntryID_, le récepteur de notifications fournit des notifications sur les modifications apportées à l’ensemble de la banque de messages.
    
 _ulEventMask_
  
> [in] Masque d’événement des types d’événements de notification qui se produisent pour l’objet sur lequel MAPI générera des notifications. Le masque filtre des cas spécifiques. Chaque type d’événement est associé à une structure qui contient des informations supplémentaires sur l’événement. Le tableau suivant répertorie les types d’événements possibles ainsi que leurs structures correspondantes.
    
|**Type d’événement de notification**|**Structure correspondante**|
|:-----|:-----|
|fnevCriticalError  <br/> |[ERROR_NOTIFICATION](error_notification.md) <br/> |
|fnevNewMail  <br/> |[NEWMAIL_NOTIFICATION](newmail_notification.md) <br/> |
|fnevObjectCreated  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectDeleted  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectModified  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectCopied  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevObjectMoved  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevSearchComplete  <br/> |[OBJECT_NOTIFICATION](object_notification.md) <br/> |
|fnevStatusObjectModified  <br/> |[STATUS_OBJECT_NOTIFICATION](status_object_notification.md) <br/> |
   
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification à appeler lorsqu’un événement se produit pour l’objet de session sur lequel la notification a été demandée. Cet objet de sink de conseil doit déjà exister.
    
 _lpulConnection_
  
> [out] Pointeur vers une variable qui, en cas de retour réussi, contient le numéro de connexion pour l’inscription de la notification. Le numéro de connexion doit être non zéro.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas prise en charge par MAPI ou par un ou plusieurs fournisseurs de services.
    
## <a name="remarks"></a>Remarques

Les fournisseurs de magasins de messages implémentent la méthode **IMSLogon::Advise** pour inscrire un objet pour les rappels de notification. Chaque fois qu’une modification se produit sur l’objet indiqué, le fournisseur vérifie quel bit de masque d’événement a été définie dans le paramètre  _ulEventMask_ et, par conséquent, quel type de modification s’est produit. Si un bit est paramétré, le fournisseur appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de sink de conseil indiqué par le paramètre  _lpAdviseSink_ pour signaler l’événement. Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement. 
  
L’appel **à OnNotify** peut se produire pendant l’appel qui modifie l’objet, ou à tout moment ultérieur. Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut se produire sur n’importe quel thread. Pour gérer en toute sécurité un appel à **OnNotify** qui peut se produire à un moment inopportune, une application cliente doit utiliser la fonction [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Pour fournir des notifications, le fournisseur de magasin de messages qui implémente **Advise** doit conserver une copie du pointeur vers l’objet de réception de notification _lpAdviseSink_ ; pour ce faire, le fournisseur appelle la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour que le sink de notification conserve son pointeur d’objet jusqu’à ce que l’inscription de notification soit annulée avec un appel à la méthode [IMSLogon::Unadvise.](imslogon-unadvise.md) **L’implémentation Advise** doit affecter un numéro de connexion à l’inscription de notification et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans _le paramètre lpulConnection._ Les fournisseurs de services peuvent libérer l’objet de sink de conseil avant l’annulation de l’inscription, mais ils ne doivent pas libérer le numéro de connexion tant **qu’Unadvise** n’a pas été appelé. 
  
Une fois qu’un appel à **Advise** a réussi et avant l’appel **d’Unadvise,** les fournisseurs doivent être préparés pour que l’objet de sink de conseil soit libéré. Par conséquent, un fournisseur doit libérer son objet de sink de conseil après le retour de **Advise,** sauf s’il dispose d’une utilisation spécifique à long terme pour lui. 
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notification](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

