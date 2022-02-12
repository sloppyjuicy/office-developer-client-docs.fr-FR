---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 18f6789441d5e7cc909b00d38240af73484772a2
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62782744"
---
# <a name="imapisupportspoolernotify"></a>IMAPISupport::SpoolerNotify

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Avertit lepooler MAPI d’un changement d’état ou d’une demande de service. 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le type de notification. Les fournisseurs de transport peuvent définir tous les indicateurs à l’exception de NOTIFY_NEWMAIL_RECEIVED ; seuls NOTIFY_NEWMAIL_RECEIVED et NOTIFY_READTOSEND sont valides pour les fournisseurs de magasins de messages. Les indicateurs suivants sont valides pour  _le paramètre ulFlags_ : 
    
NOTIFY_CONFIG_CHANGE 
  
> Enregistre une demande de modification de la configuration du fournisseur de transport. 
    
NOTIFY_CRITICAL_ERROR 
  
> Une erreur irrécable s’est produite au fournisseur de transport. Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utiliser le paramètre  _lpvData_ pour les appels de fournisseur de transport, ces indicateurs s’excluent mutuellement. 
    
NOTIFY_CRITSEC 
  
> Demande une section critique pour le fournisseur de transport. Le  _paramètre lpvData_ n’est pas définie et doit être NULL. 
    
NOTIFY_NEWMAIL 
  
> Lepooler MAPI doit télécharger les messages nouvellement reçus à la prochaine heure disponible. Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL. 
    
NOTIFY_NEWMAIL_RECEIVED 
  
> Un nouveau message a été reçu dans la boutique de messages. Le  _paramètre lpvData_ pointe vers une structure [NEWMAIL_NOTIFICATION](newmail_notification.md) qui décrit le message. Cet indicateur est utilisé pour les fournisseurs de magasins de messages étroitement associés à des fournisseurs de transport et est ignoré si le fournisseur de magasins est connecté avec l’indicateur MAPI_NO_MAIL définie. 
    
NOTIFY_NONCRIT 
  
> Libère une section critique obtenue avec un appel précédent à **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_CRITSEC. Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL. 
    
NOTIFY_READYTOSEND 
  
> Le fournisseur de transport ou de magasin de messages est prêt à envoyer des messages. Le  _paramètre lpvData_ n’est pas définie et doit être définie sur NULL. 
    
NOTIFY_SENTDEFERRED 
  
> Un message différé précédemment doit maintenant être envoyé et le fournisseur de transport doit être averti lorsque le message est prêt à être remis à l’aide d’un appel à la méthode [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) . L’identificateur d’entrée du message différé est contenu dans une structure [SBinary](sbinary.md) pointée par  _lpvData_. Étant donné que NOTIFY_SENTDEFERRED et NOTIFY_CRITICAL_ERROR utiliser le  _paramètre lpvData_ , ces indicateurs s’excluent mutuellement. 
    
 _lpvData_
  
> [in] Pointeur vers les données associées applicables à une notification. Le  _paramètre lpvData_ pointe vers des données valides uniquement lorsque les indicateurs suivants sont définies (_lpvData_ est NULL lorsque  _ulFlags_ est définie sur les autres types de notification) : 
    
|**_Paramètre ulFlags_**|**_Valeur lpvData_**|
|:-----|:-----|
|NOTIFY_CRITICAL_ERROR  <br/> |Informations sur l’erreur. |
|NOTIFY_NEWMAIL_RECEIVED  <br/> |Structure **NEWMAIL_NOTIFICATION** qui contient des informations sur le message nouvellement remis. |
|NOTIFY_SENTDEFERRED  <br/> |Structure **SBinary** qui contient l’identificateur d’entrée du message différé. |
   
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La notification a réussi.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPISupport::SpoolerNotify** est implémentée pour les objets de prise en charge de fournisseur de transport et de magasin de messages. Ces fournisseurs appellent **SpoolerNotify** pour informer lepooler MAPI d’un changement d’état ou d’une demande de service. **SpoolerNotify est** principalement appelé par les fournisseurs de transport et peut être appelé à tout moment pendant la session. 
  
## <a name="notes-to-transport-providers"></a>Remarques aux fournisseurs de transport

Si vous avez modifié la configuration de votre fournisseur de transport, appelez **SpoolerNotify** et définissez  _ulFlags_ sur NOTIFY_CONFIG_CHANGED. **SpoolerNotify répond** en appelant la méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour demander une modification des types d’adresses pris en charge. 
  
Si vous avez besoin d’une section critique pour garantir un traitement ininterrompu, appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_CRITSEC. La définition de cet indicateur informe lepooler MAPI qu’il ne doit pas appeler les méthodes [IXPLogon::Idle](ixplogon-idle.md) et [IXPLogon::P élément](ixplogon-poll.md) . Bien qu’une section critique soit ouverte, MAPI_E_BUSY chaque fois que la méthode [IMAPIStatus::ValidateState](imapistatus-validatestate.md) est appelée. Lorsque vous avez terminé avec la section critique, faites un autre appel à **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_NONCRIT. 
  
Par exemple, si votre fournisseur de transport distant est en train de télécharger des messages, vous devrez peut-être autoriser un utilisateur à entrer un numéro de téléphone pour établir la connexion à distance. Avant de passer en boucle dans la procédure de la boîte de dialogue, vous devez déclarer une section critique. Lorsque l’utilisateur ferme la boîte de dialogue et termine la procédure de la boîte de dialogue, vous devez libérer la section critique.
  
Lorsque vous définissez  _ulFlags_ sur NOTIFY_CRITICAL_ERROR, lepooler MAPI ne fait aucun autre appel au fournisseur, sauf pour le libérer. Si vous appelez **SpoolerNotify** avec NOTIFY_CRITICAL_ERROR définie à partir des méthodes [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , renvoyez avec une valeur d’erreur appropriée à partir de l’appel **StartMessage** ou ** SubmitMessage ** immédiatement après l’appel **SpoolerNotify** . 
  
Si votre fournisseur de transport a récupéré d’une condition qui l’a précédemment provoqué à l’échec, appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_READYTOSEND. Cet indicateur indique que le fournisseur est à nouveau prêt à gérer les messages. 
  
## <a name="notes-to-message-store-providers"></a>Remarques pour les fournisseurs de banque de messages

Appelez **SpoolerNotify**, en passant l’indicateur NOTIFY_READYTOSEND dans  _ulFlags_, avant d’effectuer votre premier appel à [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) dans **IMessage::SubmitMessage**. Cet appel à **SpoolerNotify** doit être effectué une seule fois par session. 
  
Si votre fournisseur de magasins de messages est étroitement associé à un fournisseur de transport et que vous appelez **SpoolerNotify** avec  _ulFlags_ définie sur NOTIFY_NEWMAIL_RECEIVED, lepooler MAPI ouvre le nouveau message et commence le traitement de la nouvelle fonction de hook de message. Une fois le traitement terminé, lepooler MAPI appelle la méthode [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) pour vous informer de votre propre nouveau message. 
  
Pour plus d’informations sur **l’appel de SpoolerNotify**, consultez l’une des rubriques suivantes :
  
- [Mise en œuvre de la méthode FlushQueues](implementing-the-flushqueues-method.md)
    
- [Interaction avec le spooler MAPI](interacting-with-the-mapi-spooler.md)
    
- [Modèle de réception des messages](message-reception-model.md)
    
## <a name="see-also"></a>Voir aussi



[IMsgStore::GetReceiveFolderTable](imsgstore-notifynewmail.md)
  
[IXPLogon::StartMessage](ixplogon-startmessage.md)
  
[IXPLogon::SubmitMessage](ixplogon-submitmessage.md)
  
[IMAPISupport : IUnknown](imapisupportiunknown.md)

