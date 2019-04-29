---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: c9401c163c74ab303ec39c147e0432d1979426b8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418812"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un objet de récepteur de notifications pour recevoir des notifications d'événements spécifiés affectant la table.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulEventMask_
  
> dans Valeur indiquant le type d'événement qui générera la notification. Seule la valeur suivante est valide:
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> dans Pointeur vers un objet de récepteur de notification pour recevoir les notifications suivantes. Cet objet de récepteur de notifications doit déjà avoir été alloué.
    
 _lpulConnection_
  
> remarquer Pointeur vers une valeur différente de zéro qui représente l'enregistrement de notification réussi.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'enregistrement des notifications est terminé.
    
MAPI_E_NO_SUPPORT 
  
> L'implémentation du tableau ne prend pas en charge les modifications apportées à ses lignes et colonnes, ou ne prend pas en charge la notification.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable:: Advise** pour inscrire un objet table implémenté dans le fournisseur pour les rappels de notification. Chaque fois qu'une modification est apportée à l'objet table, le fournisseur vérifie le bit de masque d'événement qui a été défini dans le paramètre _ulEventMask_ et, par conséquent, le type de modification qui a eu lieu. Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) pour l'objet de récepteur de notifications indiqué par le paramètre _lpAdviseSink_ pour signaler l'événement. Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l'événement. 
  
L'appel à **OnNotify** peut se produire pendant l'appel qui modifie l'objet ou à tout moment suivant. Sur les systèmes qui prennent en charge plusieurs threads d'exécution, l'appel à **OnNotify** peut se produire sur n'importe quel thread. Pour un moyen d'activer un appel vers **OnNotify** qui peut se produire à un moment inopportun en un seul à gérer, un fournisseur doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Pour fournir des notifications, le fournisseur qui met en œuvre l' **avis** doit conserver une copie du pointeur vers l'objet récepteur _lpAdviseSink_ . pour ce faire, il appelle la méthode **IUnknown:: AddRef** pour le récepteur de notifications afin de maintenir son pointeur d'objet jusqu'à ce que l'enregistrement de notification soit annulé avec un appel à la méthode [IMAPITable::](imapitable-unadvise.md) Unadvise. L'implémentation de l' **avis** doit affecter un numéro de connexion à l'enregistrement des notifications et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans le paramètre _lpulConnection_ . Les fournisseurs de services peuvent libérer l'objet récepteur de notification avant l'annulation de l'inscription, mais ils ne doivent pas libérer le numéro de connexion tant que l'appel à * * Unadvise * * n'a pas été appelé. 
  
Une fois qu'un **** appel à Advise a réussi et avant que * * Unadvise * * ait été appelé, les clients doivent être préparés pour que l'objet de récepteur de notifications soit publié. Un client doit donc libérer son objet de récepteur d' **** AVERTISSEMENT une fois qu'il a été renvoyé, sauf s'il a une utilisation à long terme spécifique pour lui. 
  
En raison du comportement asynchrone de la notification, les implémentations qui modifient les paramètres de colonne de tableau peuvent recevoir des notifications avec des informations organisées dans un ordre de colonne précédent. Par exemple, une ligne de tableau peut être renvoyée pour un message qui vient d'être supprimé du conteneur. Une telle notification est envoyée lorsque le paramètre de colonne a été modifié et que les informations relatives à ce dernier sont envoyées, mais que la vue de table de notification n'a pas encore été mise à jour avec ces informations.
  
Pour plus d'informations sur le processus de notification, consultez la rubrique [notifications d'événements dans MAPI](event-notification-in-mapi.md). Pour obtenir des informations spécifiques sur la notification de table, consultez la rubrique [à propos des notifications de table](about-table-notifications.md). Pour plus d'informations sur l'utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, consultez la rubrique [prise en](supporting-event-notification.md)charge des notifications d'événements.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContestTableListCtrl:: NotificationOn  <br/> |MFCMAPI utilise la méthode **IMAPITable:: Advise** pour enregistrer les notifications afin d'autoriser la vue de la table à rester en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

