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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d9235da7e7ec6ec244ee1a75f4795e9c77ec28bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579948"
---
# <a name="ixplogonstartmessage"></a>IXPLogon::StartMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lance le transfert d’un message entrant à partir du fournisseur de transport pour le spouleur MAPI.
  
```cpp
HRESULT StartMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] R�serv� ; doit �tre �gal � z�ro.
    
 _lpMessage_
  
> [in] Pointeur vers un objet de message (représentant le message entrant) ayant l’autorisation de lecture/écriture, qui est utilisée par le fournisseur de transport pour accéder et manipuler ce message. Cet objet restera valide jusqu'à une fois que le fournisseur de transport renvoie à partir de l’appel vers **IXPLogon::StartMessage**.
    
 _lpulMsgRef_
  
> [out] Pointeur vers une valeur de référence affectée au message. Le spouleur MAPI initialise cette valeur sur 1 avant qu’il retourne le pointeur vers le fournisseur de transport.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::StartMessage** pour initialiser le transfert d’un message entrant à partir du fournisseur de transport pour le spouleur MAPI. Avant que le fournisseur de transport commence à utiliser le message vers lequel pointé _lpMessage_, il doit stocker une référence de message dans le paramètre _lpulMsgRef_ pour son utilisation par un appel à la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) . 
  
Pendant un appel **StartMessage** , le spouleur MAPI traite des méthodes pour les objets ouverts lors du transfert du message, et il traite également les pièces jointes. Ce traitement peut prendre beaucoup de temps. Fournisseurs de transport peuvent appeler la fonction de rappel [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) pour le spouleur MAPI fréquemment lors du traitement de ce temps processeur pour les autres tâches du système de publication. 
  
Tous les destinataires dans la table de destinataires créés par le fournisseur de transport pour le message doivent contenir toutes les propriétés d’adressage requises. Si nécessaire, le fournisseur peut construire un destinataire personnalisé pour représenter un destinataire particulier. Toutefois, si le fournisseur peut générer une entrée du destinataire qui comprend plus d’informations, il doit utiliser. Par exemple, si un fournisseur de transport a suffisamment d’informations sur le format de destinataire d’un fournisseur de carnet d’adresses que cette application peut créer un identificateur d’entrée valide pour un destinataire pour ce format, il doit créer l’identificateur d’entrée.
  
Si toutes les propriétés nontransmittable sont reçues, le fournisseur de transport ne doit pas les stocker dans le nouveau message. Toutefois, le fournisseur de transport doit stocker toutes les propriétés transmissible qu’il reçoit dans le nouveau message.
  
Si le message entrant est un rapport de remise ou d’un rapport de non-remise et le fournisseur de transport ne peut pas utiliser la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour générer un rapport à partir du message d’origine, le fournisseur doit se remplir le message avec les propriétés appropriées. Toutefois, le fournisseur de transport ne peut pas définir la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) du message.
  
Pour enregistrer le message entrant dans la banque de message MAPI appropriée après le traitement, le fournisseur de transport appelle la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Si le fournisseur de transport ne dispose pas de tous les messages à transmettre à la spouleur MAPI, il peut arrêter le message entrant en retour de l’appel de **StartMessage** sans appeler **SaveChanges**.
  
Tous les objets qui le fournisseur de transport s’ouvre pendant un appel **StartMessage** doivent être libérés avant le retour. Toutefois, le fournisseur ne doit pas libérer l’objet de message le spouleur MAPI transmis à l’origine dans le paramètre _lpMessage_ . 
  
Si **StartMessage** renvoie une erreur, le message en cours est publié sans avoir enregistré les modifications et est perdu. Dans ce cas, le fournisseur de transport doit passer l’indicateur NOTIFY_CRITICAL_ERROR par un appel à la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) et appelez la méthode [IXPLogon::Poll](ixplogon-poll.md) pour notifier le spouleur MAPI qu’il est une condition d’erreur grave. 
  
Pour plus d’informations, consultez [interaction avec le spouleur MAPI](interacting-with-the-mapi-spooler.md). 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)
  
[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[IXPLogon::Poll](ixplogon-poll.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

