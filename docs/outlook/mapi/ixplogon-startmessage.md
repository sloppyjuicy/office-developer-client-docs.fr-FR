---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 00273d5572fa0c12a9501a1620db11ea087fd5d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351596"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le transfert d'un message entrant depuis le fournisseur de transport vers le spouleur MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpMessage_
  
> dans Pointeur vers un objet message (représentant le message entrant) qui dispose d'une autorisation en lecture/écriture, qui est utilisé par le fournisseur de transport pour accéder à ce message et le manipuler. Cet objet reste valide jusqu'à ce que le fournisseur de transport renvoie de l'appel à **IXPLogon:: StartMessage**.
    
 _lpulMsgRef_
  
> remarquer Pointeur vers une valeur de référence assignée au message. Le spouleur MAPI initialise cette valeur sur 1 avant de renvoyer le pointeur vers le fournisseur de transport.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: StartMessage** pour lancer le transfert d'un message entrant du fournisseur de transport vers le spouleur MAPI. Avant que le fournisseur de transport ne commence à utiliser le message désigné par _lpMessage_, il doit stocker une référence de message dans le paramètre _lpulMsgRef_ en vue d'une utilisation potentielle par un appel à la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) . 
  
Pendant un appel **StartMessage** , le spouleur MAPI traite les méthodes pour les objets ouverts lors du transfert du message, et traite également les pièces jointes. Ce traitement peut prendre beaucoup de temps. Les fournisseurs de transport peuvent appeler la fonction de rappel [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) pour le spouleur MAPI fréquemment pendant ce traitement afin de libérer le temps processeur pour d'autres tâches système. 
  
Tous les destinataires de la table de destinataires créés par le fournisseur de transport pour le message doivent contenir toutes les propriétés d'adressage requises. Si nécessaire, le fournisseur peut créer un destinataire personnalisé pour représenter un destinataire particulier. Toutefois, si le fournisseur peut produire une entrée de destinataire qui inclut davantage d'informations, il doit le faire. Par exemple, si un fournisseur de transport dispose de suffisamment d'informations sur le format de destinataire d'un fournisseur de carnet d'adresses pour qu'il puisse créer un identificateur d'entrée valide pour un destinataire pour ce format, il doit créer l'identificateur d'entrée.
  
Si des propriétés non transmissibles sont reçues, le fournisseur de transport ne doit pas les stocker dans le nouveau message. Toutefois, le fournisseur de transport doit stocker toutes les propriétés transmissibles qu'il reçoit dans le nouveau message.
  
Si le message entrant est un rapport de remise ou de non-remise et que le fournisseur de transport ne peut pas utiliser la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour générer le rapport à partir du message d'origine, le fournisseur doit lui-même remplir le message avec les propriétés appropriées. Toutefois, le fournisseur de transport ne peut pas définir la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message.
  
Pour enregistrer le message entrant dans la Banque de messages MAPI appropriée après traitement, le fournisseur de transport appelle la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Si le fournisseur de transport ne dispose d'aucun message à transmettre au spouleur MAPI, il peut arrêter le message entrant en retournant à partir de l'appel **StartMessage** sans appeler **SaveChanges**.
  
Tous les objets que le fournisseur de transport ouvre pendant un appel **StartMessage** doivent être libérés avant d'être renvoyés. Toutefois, le fournisseur ne doit pas publier l'objet de message que le spouleur MAPI a transmis à l'origine dans le paramètre _lpMessage_ . 
  
Si **StartMessage** renvoie une erreur, le message en cours de traitement n'a pas été enregistré et est perdu. Dans ce cas, le fournisseur de transport doit transmettre l'indicateur NOTIFY_CRITICAL_ERROR avec un appel à la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) et appeler la méthode [IXPLogon::P oll](ixplogon-poll.md) pour informer le spouleur MAPI qu'il se trouve dans une condition d'erreur grave. 
  
Pour plus d'informations, consultez [la rubrique interaction avec le spouleUR MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

