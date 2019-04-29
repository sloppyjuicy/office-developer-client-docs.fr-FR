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
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423768"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit le spouleur MAPI de la modification de l'État ou d'une demande de service. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui indique le type de notification. Les fournisseurs de transport peuvent définir tous les indicateurs à l'exception de NOTIFY_NEWMAIL_RECEIVED; Seuls NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de banque de messages. Les indicateurs suivants sont valides pour le paramètre _ulFlags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Enregistre une demande de modification de la configuration du fournisseur de transport. 
    
NOTIFY_CRITICAL_ERROR 
  
> Une erreur irrécupérable s'est produite au fournisseur de transport. Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s'excluent mutuellement. 
    
NOTIFY_CRITSEC 
  
> Demande une section critique pour le fournisseur de transport. Le paramètre _lpvData_ n'est pas défini et doit être null. 
    
NOTIFY_NEWMAIL 
  
> Le spouleur MAPI doit télécharger les messages nouvellement reçus à la prochaine heure disponible. Le paramètre _lpvData_ n'est pas défini et doit être défini sur null. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Un nouveau message a été reçu dans la Banque de messages. Le paramètre _lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message. Cet indicateur est utilisé pour les fournisseurs de banques de messages étroitement couplés avec les fournisseurs de transport et est ignoré si le fournisseur de banque est connecté avec l'indicateur MAPI_NO_MAIL défini. 
    
NOTIFY_NONCRIT 
  
> Libère une section critique obtenue avec un appel précédent à **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_CRITSEC. Le paramètre _lpvData_ n'est pas défini et doit être défini sur null. 
    
NOTIFY_READYTOSEND 
  
> Le fournisseur de banque de messages ou de transport est prêt à envoyer des messages. Le paramètre _lpvData_ n'est pas défini et doit être défini sur null. 
    
NOTIFY_SENTDEFERRED 
  
> Un message précédemment différé doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l'aide d'un appel à la méthode [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) . L'identificateur d'entrée du message différé est contenu dans une structure [SBinary](sbinary.md) désignée par _lpvData_. Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utilisent le paramètre _lpvData_ , ces indicateurs s'excluent mutuellement. 
    
 _lpvData_
  
> dans Pointeur vers les données associées applicables à une notification. Le paramètre _lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définis (_lpvData_ est NULL lorsque _ulFlags_ est défini sur les autres types de notification): 
    
|**paramètre _ulFlags_**|**valeur _lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informations sur l'erreur.  <br/> |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Une structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis.  <br/> |
|NOTIFY_SENTDEFERRED  <br/> |Une structure **SBinary** qui contient l'identificateur d'entrée du message différé.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPISupport:: SpoolerNotify** est implémentée pour les objets de prise en charge du magasin de messages et du fournisseur de transport. Ces fournisseurs appellent **SpoolerNotify** pour informer le spouleur MAPI de la modification de l'État ou d'une demande de service. **SpoolerNotify** est appelé principalement par les fournisseurs de transport et peut être appelé à tout moment pendant la session. 
  
## <a name="notes-to-transport-providers"></a>Remarques relatives aux fournisseurs de transport

Si vous avez modifié votre configuration de fournisseur de transport, appelez **SpoolerNotify** et définissez _ulFlags_ sur NOTIFY_CONFIG_CHANGED. **SpoolerNotify** répond en appelant la méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pour demander une modification dans les types d'adresses pris en charge. 
  
Si vous avez besoin d'une section critique pour garantir un traitement ininterrompu, appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_CRITSEC. La définition de cet indicateur informe le spouleur MAPI qu'il ne doit pas appeler les méthodes [IXPLogon:: Idle](ixplogon-idle.md) et [IXPLogon::P oll](ixplogon-poll.md) . Une fois que vous avez une section critique ouverte, renvoyez MAPI_E_BUSY à chaque appel de la méthode [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . Une fois que vous avez terminé la section critique, effectuez un autre appel à **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_NONCRIT. 
  
Par exemple, si votre fournisseur de transport distant est en train de télécharger des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance. Avant d'effectuer une boucle dans la procédure de la boîte de dialogue, vous devez déclarer une section critique. Lorsque l'utilisateur ferme la boîte de dialogue en terminant la procédure de la boîte de dialogue, vous devez libérer la section critique.
  
Lorsque vous définissez _ulFlags_ sur NOTIFY_CRITICAL_ERROR, le spouleur MAPI ne procède à aucun autre appel du fournisseur à l'exception de sa publication. Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR défini à partir des méthodes [IXPLogon:: StartMessage](ixplogon-startmessage.md) ou [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) , revenez avec une valeur d'erreur appropriée à partir de l'appel **StartMessage** ou * * SubmitMessage * * immédiatement après l'appel de **SpoolerNotify** . 
  
Si votre fournisseur de transport récupère à partir d'une condition qui l'a déjà causée, appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_READYTOSEND. Cet indicateur indique que le fournisseur est à nouveau prêt à gérer les messages. 
  
## <a name="notes-to-message-store-providers"></a>Remarques aux fournisseurs de banques de messages

Appelez **SpoolerNotify**, en passant l'indicateur NOTIFY_READYTOSEND dans _ulFlags_, avant d'effectuer votre premier appel à [IMAPISupport::P Reparesubmit](imapisupport-preparesubmit.md) dans **IMessage:: SubmitMessage**. Cet appel à **SpoolerNotify** ne doit être effectué qu'une seule fois par session. 
  
Si votre fournisseur de banque de messages est étroitement couplé à un fournisseur de transport et que vous appelez **SpoolerNotify** avec _ULFLAGS_ défini sur NOTIFY_NEWMAIL_RECEIVED, le spouleur MAPI ouvre le nouveau message et commence à traiter la nouvelle fonction de raccordement de message. Une fois le traitement terminé, le spouleur MAPI appelle la méthode [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer de votre propre nouveau message. 
  
Pour plus d'informations sur l'appel de **SpoolerNotify**, reportez-vous à l'une des rubriques suivantes:
  
- [Implémentation de la méthode FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modèle de réception des messages](message-reception-model.md)
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::GetReceiveFolderTable](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

