---
title: IXPLogonStartMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.StartMessage
api_type:
- COM
ms.assetid: 83c349f7-dcac-4268-befe-fb2bc0cd9c50
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c8f15397e42bd3936676281fc8d98e3a6b85d1a6
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62464642"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI.
  
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
  
> [in] Pointeur vers un objet de message (représentant le message entrant) qui dispose d’une autorisation de lecture/écriture, qui est utilisé par le fournisseur de transport pour accéder à ce message et le manipuler. Cet objet reste valide jusqu’à ce que le fournisseur de transport retourne de l’appel à **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Pointeur vers une valeur de référence affectée au message. Lepooler MAPI initialise cette valeur sur 1 avant de retourner le pointeur au fournisseur de transport.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::StartMessage** pour initier le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI. Avant que le fournisseur de transport ne commence à utiliser le message pointé par  _lpMessage_, il doit stocker une référence de message dans le paramètre _lpulMsgRef_ pour une utilisation potentielle par un appel à la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) . 
  
Lors **d’un appel StartMessage** , lepooler MAPI traite les méthodes pour les objets ouverts lors du transfert du message et traite également les pièces jointes. Ce traitement peut prendre beaucoup de temps. Les fournisseurs de transport peuvent appeler fréquemment la fonction de rappel [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) pour lepooler MAPI pendant ce traitement pour libérer du temps processeur pour d’autres tâches système. 
  
Tous les destinataires de la table des destinataires créée par le fournisseur de transport pour le message doivent contenir toutes les propriétés d’adressare requises. Si nécessaire, le fournisseur peut construire un destinataire personnalisé pour représenter un destinataire particulier. Toutefois, si le fournisseur peut produire une entrée de destinataire qui inclut plus d’informations, il doit le faire. Par exemple, si un fournisseur de transport dispose de suffisamment d’informations sur le format de destinataire d’un fournisseur de carnet d’adresses pour créer un identificateur d’entrée valide pour un destinataire pour ce format, il doit créer l’identificateur d’entrée.
  
Si des propriétés nontransmitables sont reçues, le fournisseur de transport ne doit pas les stocker dans le nouveau message. Toutefois, le fournisseur de transport doit stocker toutes les propriétés transmises qu’il reçoit dans le nouveau message.
  
Si le message entrant est un rapport de remise ou de remise et que le fournisseur de transport ne peut pas utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour générer le rapport à partir du message d’origine, le fournisseur doit lui-même remplir le message avec les propriétés appropriées. Toutefois, le fournisseur de transport ne peut pas définir la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message.
  
Pour enregistrer le message entrant dans la magasin de messages MAPI appropriée après le traitement, le fournisseur de transport appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Si le fournisseur de transport n’a aucun message à transmettre aupooler MAPI, il peut arrêter le message entrant en revenant de l’appel **StartMessage** sans appeler **SaveChanges**.
  
Tous les objets que le fournisseur de transport ouvre lors d’un appel **StartMessage** doivent être libérés avant d’être retournés. Toutefois, le fournisseur ne doit pas libérer l’objet message que lepooler MAPI a transmis à l’origine dans le _paramètre lpMessage_ . 
  
Si **StartMessage renvoie** une erreur, le message en cours est libéré sans que les modifications ne sont enregistrées et est perdu. Dans ce cas, le fournisseur de transport doit transmettre l’indicateur NOTIFY_CRITICAL_ERROR avec un appel à la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et appeler la méthode [IXPLogon::P élément](ixplogon-poll.md) pour informer lepooler MAPI qu’il se trouve dans une condition d’erreur grave. 
  
Pour plus d’informations, [voir Interaction avec le spooler MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

