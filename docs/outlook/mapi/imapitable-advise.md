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
ms.openlocfilehash: cd6b119bd88fccf80bf2488592a24b3398e6e8af
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594242"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un objet de récepteur advise pour recevoir une notification d’événements spécifiés affectant la table.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulEventMask_
  
> [in] Valeur qui indique le type d’événement qui génère la notification. Uniquement la valeur suivante est valide :
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de récepteur advise pour recevoir les notifications ultérieures. Cet objet de récepteur advise doit déjà affectée.
    
 _lpulConnection_
  
> [out] Pointeur vers une valeur différente de zéro qui représente l’enregistrement de notification réussie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de notification est terminée.
    
MAPI_E_NO_SUPPORT 
  
> L’implémentation de la table ne prend pas en charge les modifications apportées à ses lignes et colonnes ou ne prend pas en charge la notification.
    
## <a name="remarks"></a>Remarques

Utilisez la méthode **IMAPITable::Advise** pour inscrire un objet table implémenté dans le fournisseur pour les rappels de notification. Chaque fois qu’une modification est apportée à l’objet table, le fournisseur vérifie les bits de masque événement a été défini dans le paramètre _ulEventMask_ et donc le type de modification s’est produite. Si un bit est défini, le fournisseur appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de récepteur advise indiqué par le paramètre _lpAdviseSink_ pour signaler l’événement. Données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement. 
  
L’appel de **OnNotify** peut se produire lors de l’appel qui modifie l’objet, ou à tout moment suivante. Sur les systèmes qui prennent en charge plusieurs threads d’exécution, l’appel de **OnNotify** peut se produire sur n’importe quel thread. Pour activer un appel à **OnNotify** qui peut se produire à un moment peu opportuns en un seul qui est plus sûr de gérer un moyen, un fournisseur doit utiliser la fonction [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) . 
  
Pour fournir des notifications, le fournisseur implémentation **Advise** doit conserver une copie du pointeur pour la _lpAdviseSink_ conseille objet récepteur ; Pour ce faire, il appelle la méthode **IUnknown::AddRef** pour le récepteur de notifications maintenir son pointeur de l’objet jusqu'à ce que l’inscription aux notifications est annulée par un appel à la méthode [IMAPITable::Unadvise](imapitable-unadvise.md) . L’implémentation **Advise** doit affecter un numéro de connexion à l’enregistrement de notification et appelez **AddRef** sur ce numéro de connexion avant de la retourner dans le paramètre _lpulConnection_ . Fournisseurs de services peuvent libérer l’objet de récepteur advise avant l’enregistrement est annulée, mais ils ne doivent libérer jusqu'à ce que le numéro de connexion ** Unadvise ** a été appelée. 
  
Après un appel à **Advise** a réussi et avant ** Unadvise ** a été appelée, les clients doivent être préparés pour l’objet de récepteur advise doit être publié. Un client doit donc libérer son objet de récepteur advise après **Advise** renvoie à moins qu’une utilisation à long terme spécifique pour qu’il. 
  
En raison du comportement de notification asynchrone, implémentations de modifier les paramètres de colonne de table peuvent recevoir des notifications avec des informations organisées dans un ordre de la colonne précédente. Par exemple, une ligne de tableau peut être retournée pour un message qui vient d’être supprimé du conteneur. Une notification est envoyée lorsque la colonne paramètre a été modifié et informations envoyées, mais que l’affichage de tableau de notification n’a pas été mis à jour avec ces informations encore.
  
Pour plus d’informations sur le processus de notification, voir [Notification d’événement MAPI](event-notification-in-mapi.md). Pour obtenir des informations spécifiques sur la notification de la table, voir [Sur les Notifications de Table](about-table-notifications.md). Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Prise en charge de Notification d’événement](supporting-event-notification.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI utilise la méthode **IMAPITable::Advise** pour enregistrer les notifications autoriser l’affichage tableau restent en cours.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

