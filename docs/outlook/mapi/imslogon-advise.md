---
title: IMSLogonAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Advise
api_type:
- COM
ms.assetid: a3c5d937-642b-463b-b5a0-5d099e651895
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 87be00bce55fabda6271b472a9e5c446aaf8054a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784279"
---
# <a name="imslogonadvise"></a>IMSLogon::Advise

  
  
**S’applique à**: Outlook 
  
Inscrit un objet avec un fournisseur de magasin de message pour les notifications sur les modifications dans la banque de messages. La banque de messages envoie ensuite les notifications sur les modifications apportées à l’objet inscrit.
  
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
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de l’objet sur lequel les notifications doivent être générées. Cet objet peut être un dossier, un message ou tout autre objet dans la banque de messages. Vous pouvez également si MAPI définit le paramètre _cbEntryID_ à 0 et passe **null** pour _lpEntryID_, le récepteur de notifications des notifications sur les modifications dans le magasin de l’intégralité du message.
    
 _ulEventMask_
  
> [in] Un masque des types d’événements de notification de l’objet sur lequel MAPI génère des notifications d’événement. Le masque de filtre cas spécifiques. Chaque type d’événement a une structure associée qui contient des informations supplémentaires sur l’événement. Le tableau suivant répertorie les types d’événements possibles ainsi que leurs structures correspondantes.
    
|**Type d’événement notification**|**Structure correspondante**|
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
  
> [in] Pointeur vers un objet de récepteur advise appelée lorsqu’un événement se produit pour l’objet session sur lequel la notification a été demandée. Cet objet de récepteur advise doit déjà exister.
    
 _lpulConnection_
  
> [out] Pointeur vers une variable qui conserve le numéro de connexion pour l’enregistrement de notification à un retour réussi. Le numéro de connexion doit être différente de zéro.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_NO_SUPPORT 
  
> L’opération n’est pas pris en charge par MAPI ou par un ou plusieurs fournisseurs de services.
    
## <a name="remarks"></a>Remarques

Fournisseurs de magasins de message implémentent la méthode **IMSLogon::Advise** pour enregistrer un objet pour les rappels de notification. Chaque fois qu’une modification est apportée à l’objet indiqué, le fournisseur vérifie les bits de masque événement a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification s’est produite. Si un bit est défini, le fournisseur appelle la méthode de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise indiqué par le paramètre _lpAdviseSink_ pour signaler l’événement. Données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement. 
  
L’appel de **OnNotify** peut se produire lors de l’appel qui modifie l’objet, ou ultérieurement. Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread. Pour gérer en toute sécurité un appel à **OnNotify** qui peut se produire à un moment peu opportuns, une application cliente doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Pour fournir des notifications, le fournisseur de banque de messages qui implémente **Advise** doit conserver une copie du pointeur pour la _lpAdviseSink_ conseiller objet récepteur ; Pour ce faire, le fournisseur appelle la méthode [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) pour le récepteur de notifications maintenir son pointeur de l’objet jusqu'à ce que l’inscription aux notifications est annulée par un appel à la méthode [IMSLogon::Unadvise](imslogon-unadvise.md) . L’implémentation **Advise** doit affecter un numéro de connexion à l’enregistrement de notification et appelez **AddRef** sur ce numéro de connexion avant de la retourner dans le paramètre _lpulConnection_ . Fournisseurs de services peuvent libérer l’objet de récepteur advise avant l’enregistrement est annulée, mais ils ne doivent libérer le numéro de connexion jusqu'à ce que **Unadvise** a été appelée. 
  
Après qu’un appel à **Advise** a réussi et avant **Unadvise** a été appelée, les fournisseurs doivent être préparés pour l’objet de récepteur advise doit être publié. Par conséquent, un fournisseur doit libérer son objet de récepteur advise après **Advise** renvoie, à moins qu’une utilisation à long terme spécifique pour qu’il. 
  
Pour plus d’informations sur le processus de notification, reportez-vous à la section [Notification d’événement MAPI](event-notification-in-mapi.md). 
  
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMSLogon::Unadvise](imslogon-unadvise.md)
  
[Notification](notification.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

