---
title: IMAPITableAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPITable.Advise
api_type:
- COM
ms.assetid: e8b5d21e-dc14-4b61-96b3-a51bcfa0d232
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aabcb60c16c2c7c5415c997d0f2fdbdf9d2f4dc1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620841"
---
# <a name="imapitableadvise"></a>IMAPITable::Advise

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Inscrit un objet de réception de notification pour recevoir une notification d’événements spécifiés affectant la table.
  
```cpp
HRESULT Advise(
ULONG ulEventMask,
LPMAPIADVISESINK lpAdviseSink,
ULONG_PTR FAR * lpulConnection
);
```

## <a name="parameters"></a>Paramètres

 _ulEventMask_
  
> [in] Valeur indiquant le type d’événement qui générera la notification. Seule la valeur suivante est valide :
    
 `fnevTableModified`
  
 _lpAdviseSink_
  
> [in] Pointeur vers un objet de réception de notification pour recevoir les notifications suivantes. Cet objet de sink de conseil doit avoir été déjà alloué.
    
 _lpulConnection_
  
> [out] Pointeur vers une valeur autre que zéro qui représente l’inscription de notification réussie.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’inscription de la notification s’est correctement terminée.
    
MAPI_E_NO_SUPPORT 
  
> L’implémentation de tableau ne prend pas en charge les modifications apportées à ses lignes et colonnes ou ne prend pas en charge la notification.
    
## <a name="remarks"></a>Remarques

Utilisez la **méthode IMAPITable::Advise** pour inscrire un objet table implémenté dans le fournisseur pour les rappels de notification. Chaque fois qu’une modification a lieu sur l’objet table, le fournisseur vérifie quel bit de masque d’événement a été définie dans le paramètre  _ulEventMask_ et par conséquent quel type de modification s’est produit. Si un bit est paramétré, le fournisseur appelle la méthode [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) pour l’objet de sink de conseil indiqué par le paramètre  _lpAdviseSink_ pour signaler l’événement. Les données transmises dans la structure de notification à la routine **OnNotify** décrivent l’événement. 
  
L’appel **à OnNotify** peut se produire pendant l’appel qui modifie l’objet, ou à tout moment suivant. Sur les systèmes qui prendre en charge plusieurs threads d’exécution, l’appel à **OnNotify** peut se produire sur n’importe quel thread. Pour transformer un appel à **OnNotify** qui peut se produire à un moment inopportune en un appel plus sûr à gérer, un fournisseur doit utiliser la fonction [HrThisThreadAdviseSink.](hrthisthreadadvisesink.md) 
  
Pour fournir des notifications, le fournisseur qui implémente **Advise** doit conserver une copie du pointeur vers l’objet de réception de notification _lpAdviseSink_ ; pour ce faire, il appelle la méthode **IUnknown::AddRef** pour que le sink de notification conserve son pointeur d’objet jusqu’à ce que l’inscription de notification soit annulée avec un appel à la méthode [IMAPITable::Unadvise.](imapitable-unadvise.md) **L’implémentation Advise** doit affecter un numéro de connexion à l’inscription de notification et appeler **AddRef** sur ce numéro de connexion avant de le renvoyer dans _le paramètre lpulConnection._ Les fournisseurs de services peuvent libérer l’objet de sink de conseil avant l’annulation de l’inscription, mais ils ne doivent pas libérer le numéro de connexion tant que ** Unadvise ** n’a pas été appelé. 
  
Une fois qu’un appel à **Advise** a réussi et avant que ** Unadvise ** ait été appelé, les clients doivent être préparés pour que l’objet de sink de conseil soit libéré. Un client doit donc libérer son objet de sink de conseil après le retour de **Advise,** sauf s’il dispose d’une utilisation spécifique à long terme pour lui. 
  
En raison du comportement asynchrone de la notification, les implémentations qui modifient les paramètres de colonne de table peuvent recevoir des notifications avec des informations organisées dans un ordre de colonne précédent. Par exemple, une ligne de tableau peut être renvoyée pour un message qui vient d’être supprimé du conteneur. Une telle notification est envoyée lorsque la modification du paramètre de colonne a été réalisée et que des informations à son sujet ont été envoyées, mais que l’affichage de la table de notifications n’a pas encore été mis à jour avec ces informations.
  
Pour plus d’informations sur le processus de notification, voir [notification d’événement dans MAPI](event-notification-in-mapi.md). Pour plus d’informations sur les notifications de tableau, voir [À propos des notifications de tableau.](about-table-notifications.md) Pour plus d’informations sur l’utilisation des méthodes **IMAPISupport** pour prendre en charge la notification, voir [Notification d’événement de prise en charge.](supporting-event-notification.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContestTableListCtrl::NotificationOn  <br/> |MFCMAPI utilise la **méthode IMAPITable::Advise** pour s’inscrire aux notifications afin de permettre à l’affichage tableau de rester à jour.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[HrThisThreadAdviseSink](hrthisthreadadvisesink.md)
  
[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)
  
[IMAPITable::Unadvise](imapitable-unadvise.md)
  
[TABLE_NOTIFICATION](table_notification.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

