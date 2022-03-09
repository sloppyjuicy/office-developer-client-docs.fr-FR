---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
ms.openlocfilehash: f6fb611f5d42e36ee940a5a9eb94787056a119ad
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375425"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que lepooler MAPI a un message à remettre au fournisseur de transport.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le message est envoyé. L’indicateur suivant peut être définie :
    
BEGIN_DEFERRED 
  
> Lepooler MAPI appelle un fournisseur de transport avec un message qui a été différé précédemment. L’identificateur d’entrée du message est identique au moment où il a été différé. Le message a été différé en passant son identificateur d’entrée aupooler MAPI à l’aide de la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> [in] Pointeur vers un objet de message (représentant le message à remettre) qui dispose d’une autorisation de lecture/écriture, que le fournisseur de transport utilise pour accéder à ce message et le manipuler. Cet objet reste valide jusqu’au retour du fournisseur de transport à partir d’un appel ultérieur à la [méthode IXPLogon::EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> [out] Pointeur vers une variable dans laquelle le fournisseur de transport renvoie la valeur de référence qu’il a affectée à ce message. Lepooler MAPI transmet cette valeur de référence dans les appels suivants pour ce message. Lepooler MAPI initialise la valeur sur 0 avant de la renvoyer au fournisseur de transport.
    
 _lpulReturnParm_
  
> [out] Pointeur vers une variable qui correspond à la valeur MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR’erreur renvoyée par **SubmitMessage**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BUSY 
  
> Le fournisseur de transport ne peut pas gérer le message, car il effectue une autre opération. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu’aucun traitement ne s’est produit et que lepooler MAPI ne doit pas appeler **EndMessage**. Lepooler MAPI tentera à nouveau **l’appel SubmitMessage** ultérieurement. 
    
MAPI_E_CANCEL 
  
> Bien que le fournisseur de transport a demandé aupooler MAPI de resoumettre le message lors d’un appel **SpoolerNotify** précédent, les conditions ont depuis été modifiées et le message ne doit pas être resenté. Lepooler MAPI va continuer pour gérer autre chose. 
    
MAPI_E_NETWORK_ERROR 
  
> Une erreur réseau a empêché l’exécution de l’opération. Le  _paramètre lpulReturnParm_ doit être définie sur le nombre de secondes qui s’écouléeront avant que lepooler MAPI ne retransmettre le message. 
    
MAPI_E_NOT_ME 
  
> Le fournisseur de transport ne peut pas gérer ce message. Lepooler MAPI doit essayer de trouver un autre fournisseur de transport pour celui-ci. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu’aucun traitement ne s’est produit et que lepooler MAPI ne doit pas appeler **EndMessage**.
    
MAPI_E_WAIT 
  
> Un problème temporaire empêche le fournisseur de transport de gérer le message. Le  _paramètre lpulReturnParm_ doit être définie sur le nombre de secondes qui s’écouléeront avant que lepooler MAPI ne retransmettre le message. 
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPLogon::SubmitMessage** lorsqu’il a un message à remettre au fournisseur de transport. Le message est transmis au fournisseur de transport à l’aide du  _paramètre lpMessage_ . 
  
Si le fournisseur est prêt à accepter le message, il doit renvoyer une valeur de référence à l’aide du paramètre  _lpulMsgRef_ , traiter l’objet transmis et renvoyer la valeur appropriée (généralement S_OK). Si le fournisseur n’est pas prêt à gérer le transfert, il doit renvoyer une valeur d’erreur et, éventuellement, une autre valeur de retour MAPI dans  _lpulReturnParm_ pour indiquer le temps d’attente dupooler MAPI avant de renvoyer le message. 
  
L’implémentation de cette méthode par un fournisseur de transport peut :
  
- Placez le message dans une file d’attente interne pour attendre la transmission, éventuellement en copiant le message dans le stockage local, puis renvoyez-le.
    
- Essayez d’effectuer la transmission réelle et de la renvoyer une fois la transmission terminée, avec succès ou sans succès.
    
- Déterminez s’il faut envoyer le message après avoir vérifié la ressource impliquée. Dans ce cas, si la ressource est gratuite, le fournisseur peut verrouiller la ressource, préparer le message et l’envoyer. Si la ressource est occupée, le fournisseur peut préparer le message et différer l’envoi à une heure ultérieure.
    
La technique préférée pour la transmission des messages dépend du fournisseur de transport et du nombre attendu de processus concurrents pour les ressources système. 
  
Lors **d’un appel SubmitMessage** , le fournisseur de transport contrôle le transfert des données de message à partir de l’objet de message. Toutefois, le fournisseur de transport doit affecter une valeur de référence au message, à laquelle il renvoie un pointeur dans  _lpulMsgRef_, avant de transférer des données. Il le fait car, à tout moment au cours du processus, lepooler MAPI peut appeler la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) avec l’indicateur NOTIFY_CANCEL_MESSAGE pour signaler au fournisseur qu’il doit libérer tous les objets ouverts et arrêter le transfert des messages. 
  
Le fournisseur de transport ne doit pas envoyer de propriétés nontransmitables du message. Lorsqu’elle trouve une telle propriété, elle doit continuer pour traiter la propriété suivante. Le fournisseur doit faire tout son possible pour ne pas afficher MAPI_P1 du destinataire dans le cadre du contenu du message transmis . le fournisseur doit utiliser ces informations de destinataire uniquement à des fins d’adressan. MAPI_P1 destinataires sont des destinataires générés en interne qui sont utilisés pour renvoyer des messages ; ils ne doivent pas être transmis. Utilisez plutôt les autres destinataires pour transmettre des informations sur les destinataires. L’objectif de cette disposition est de permettre aux destinataires de renvoyer la même table de destinataires que les destinataires d’origine.
  
Au cours **d’un appel SubmitMessage** , lepooler MAPI traite les méthodes pour les objets ouverts lors du transfert du message et traite les pièces jointes. Ce traitement peut prendre beaucoup de temps. Les fournisseurs de transport peuvent appeler fréquemment la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) pour lepooler MAPI pendant ce traitement pour libérer du temps processeur pour d’autres tâches système. 
  
Tous les destinataires du message sont visibles dans la table des destinataires du message que lepooler MAPI a transmis à l’origine. Le fournisseur de transport doit traiter uniquement les destinataires qu’il peut gérer (en fonction de l’identificateur d’entrée, du type d’adresse ou des deux) et dont la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) n’est pas déjà définie sur TRUE. Si **PR_RESPONSIBILITY** est déjà définie sur TRUE, un autre fournisseur de transport a géré ce destinataire. Lorsque le fournisseur termine un traitement suffisant d’un destinataire pour déterminer s’il peut gérer les messages pour ce destinataire, il doit définir la propriété **PR_RESPONSIBILITY** de ce destinataire sur TRUE dans le message transmis. En règle générale, le fournisseur effectue cette détermination une fois la remise du message terminée. 
  
En règle générale, le fournisseur de transport ne revient pas d’un appel **SubmitMessage** tant qu’il n’a pas terminé le transfert des données de message. Si aucune erreur n’est renvoyée, l’appel suivant dupooler MAPI au fournisseur est un appel à la méthode [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
  
Si **SubmitMessage renvoie** une erreur, lepooler MAPI libère le message en cours de traitement sans enregistrer les modifications. Si le fournisseur de transport requiert l’enregistrer, il doit appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message avant de le renvoyer. 
  
En cas d’erreurs qui se produisent en raison de problèmes de transport, lepooler MAPI conserve le message, mais il retarde le resoumettre le message au fournisseur de transport en fonction de la valeur renvoyée dans  _lpulReturnParm_. Le fournisseur de transport doit remplir cette valeur si sa valeur de retour de **SubmitMessage** est MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Si une condition d’erreur grave se produit, le fournisseur de transport doit appeler la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’NOTIFY_CRITICAL_ERROR’indicateur. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

