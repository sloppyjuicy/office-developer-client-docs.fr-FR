---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a2837e5470729ae3cdd0b83e17d0342620c986e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592114"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Notifie le spouleur MAPI d’un changement de statut ou une demande de service. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le type de notification. Fournisseurs de transport peuvent définir tous les indicateurs à l’exception de NOTIFY_NEWMAIL_RECEIVED ; uniquement NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de banque de messages. Les indicateurs suivants sont valides pour le paramètre _ulFlags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Enregistre une demande de modification de configuration du fournisseur de transport. 
    
NOTIFY_CRITICAL_ERROR 
  
> Une erreur irrécupérable s’est produite au fournisseur de transport. Étant donné que les deux NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s’excluent mutuellement. 
    
NOTIFY_CRITSEC 
  
> Demande une section critique pour le fournisseur de transport. Le paramètre _lpvData_ n’est pas défini et doit être NULL. 
    
NOTIFY_NEWMAIL 
  
> Le spouleur MAPI doit télécharger tous les messages reçus récemment à la prochaine heure disponible. Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Un nouveau message a été reçu dans la banque de messages. Le paramètre _lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message. Cet indicateur est utilisé pour les fournisseurs de banque de messages qui sont étroitement liés à des fournisseurs de transport et est ignoré si le fournisseur de banque est connecté avec l’indicateur MAPI_NO_MAIL. 
    
NOTIFY_NONCRIT 
  
> Publie une section critique qui a été obtenue par un appel précédent à **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_CRITSEC. Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL. 
    
NOTIFY_READYTOSEND 
  
> Le fournisseur de magasin de transport ou d’un message est prêt à envoyer des messages. Le paramètre _lpvData_ n’est pas défini et doit être défini avec la valeur NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Un message précédemment différé doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l’aide d’un appel à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . L’identificateur d’entrée du message différé est contenue dans une structure [SBinary](sbinary.md) désignée par _lpvData_. Étant donné que les deux NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ , ces indicateurs s’excluent mutuellement. 
    
 _lpvData_
  
> [in] Pointeur vers les données associées applicables à une notification. Le paramètre _lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définis (_lpvData_ est NULL lorsque _ulFlags_ est défini sur les autres types de notification) : 
    
|**paramètre _ulFlags_**|**valeur _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informations sur l’erreur.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Une structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Une structure **SBinary** qui contient l’identificateur d’entrée du message différé.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport::SpoolerNotify** est implémentée pour message stocker et transporter des objets du fournisseur de prise en charge. Ces fournisseurs appellent **SpoolerNotify** pour notifier le spouleur MAPI d’un changement de statut ou une demande de service. **SpoolerNotify** est appelé principalement par les fournisseurs de transport et peut être appelé à tout moment pendant la session. 
  
## <a name="notes-to-transport-providers"></a>Remarques pour les fournisseurs de Transport

Si vous avez modifié la configuration de votre fournisseur de transport, appelez **SpoolerNotify** et NOTIFY_CONFIG_CHANGED la valeur _ulFlags_ . **SpoolerNotify** répond en appelant la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour interroger une modification dans les types d’adresse pris en charge. 
  
Si vous avez besoin d’une section critique pour assurer le traitement ininterrompu, appelez **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_CRITSEC. Définition de cet indicateur informe le spouleur MAPI qu’elle ne doit pas appeler les méthodes [IXPLogon::Idle](ixplogon-idle.md) et [IXPLogon::Poll](ixplogon-poll.md) . Alors que vous avez une section critique ouvert, retourne MAPI_E_BUSY chaque fois que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est appelée. Lorsque vous avez terminé avec la section critique, appelez une autre **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_NONCRIT. 
  
Par exemple, si votre fournisseur de transport à distance est en cours de téléchargement des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance. Avant de vous boucle par le biais de la procédure de boîte de dialogue, vous devez déclarer une section critique. Lorsque l’utilisateur ferme la boîte de dialogue, abandon de la procédure de boîte de dialogue, vous devez libérer la section critique.
  
Lorsque vous définissez _ulFlags_ sur NOTIFY_CRITICAL_ERROR, le spouleur MAPI ne rend plus aucun appel au fournisseur à l’exception aux libérer. Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR défini à partir des méthodes [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , renvoyer avec une valeur d’erreur appropriés à partir de la **StartMessage** ou ** SubmitMessage ** d’appel immédiatement après l’appel de **SpoolerNotify** . 
  
Si votre fournisseur de transport récupérés à partir d’une condition qui provoquaient antérieurement qu’il échoue, appelez **SpoolerNotify** avec _ulFlags_ défini sur NOTIFY_READYTOSEND. Cet indicateur indique que le fournisseur est à nouveau prêt à traiter les messages. 
  
## <a name="notes-to-message-store-providers"></a>Remarques pour les fournisseurs de banque de messages

Appelez **SpoolerNotify**, en passant l’indicateur NOTIFY_READYTOSEND _ulFlags_, avant de rendre votre premier appel à [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) dans **IMessage::SubmitMessage**. Cet appel à **SpoolerNotify** doit être effectuée qu’une seule fois par session. 
  
Si votre fournisseur de banque de messages est étroitement avec un transport de fournisseur et que vous appelez **SpoolerNotify** avec la valeur _ulFlags_ NOTIFY_NEWMAIL_RECEIVED, le spouleur MAPI ouvre le nouveau message et commence à traiter la nouvelle fonction raccordement de message. Lorsque le traitement est terminé, le spouleur MAPI appelle la méthode de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer du nouveau message. 
  
Pour plus d’informations sur l’appel de **SpoolerNotify**, consultez les rubriques suivantes :
  
- [Implémentation de la méthode FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modèle de réception de message](message-reception-model.md)
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::GetReceiveFolderTable](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

