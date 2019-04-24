---
title: IXPLogonSubmitMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.SubmitMessage
api_type:
- COM
ms.assetid: a261ba0d-cb56-4935-b745-1d4bbd0b8b9d
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: ae124cb94cff5be0a655386d31f1bf2c82f66a85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351589"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique que le spouleur MAPI a un message pour le fournisseur de transport à livrer.
  
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
  
> dans Masque de des indicateurs qui contrôle le mode d'envoi du message. L'indicateur suivant peut être défini:
    
BEGIN_DEFERRED 
  
> Le spouleur MAPI appelle un fournisseur de transport avec un message qui a été précédemment différé. L'identificateur d'entrée du message est le même que lorsqu'il a été différé. Le message a été différé en transmettant son identificateur d'entrée au spouleur MAPI à l'aide de la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) avec l'indicateur NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> dans Pointeur vers un objet message (représentant le message à livrer) qui dispose d'une autorisation en lecture/écriture, que le fournisseur de transport utilise pour accéder à ce message et le manipuler. Cet objet reste valide jusqu'à ce que le fournisseur de transport renvoie d'un appel ultérieur à la méthode [IXPLogon:: EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> remarquer Pointeur vers une variable dans laquelle le fournisseur de transport renvoie la valeur de référence qu'il a affectée à ce message. Le spouleur MAPI transmet cette valeur de référence dans les appels suivants pour ce message. Le spouleur MAPI initialise la valeur sur 0 avant de la renvoyer au fournisseur de transport.
    
 _lpulReturnParm_
  
> remarquer Pointeur vers une variable qui correspond à la valeur d'erreur MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR renvoyée par **SubmitMessage**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_BUSY 
  
> Le fournisseur de transport ne peut pas gérer le message, car il effectue une autre opération. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu'aucun traitement ne s'est produit et que le spouleur MAPI ne doit pas appeler **EndMessage**. Le spouleur MAPI tentera à nouveau l'appel **SubmitMessage** ultérieurement. 
    
MAPI_E_CANCEL 
  
> Bien que le fournisseur de transport ait demandé que le spouleur MAPI resoumette le message lors d'un appel **SpoolerNotify** précédent, les conditions ont été modifiées et le message ne doit pas être renvoyé. Le spouleur MAPI va prendre en charge d'autres éléments. 
    
MAPI_E_NETWORK_ERROR 
  
> Une erreur réseau A empêché la réussite de l'opération. Le paramètre _lpulReturnParm_ doit être défini sur le nombre de secondes qui doivent s'écouler avant que le spouleur MAPI n'envoie le message. 
    
MAPI_E_NOT_ME 
  
> Le fournisseur de transport ne peut pas gérer ce message. Le spouleur MAPI doit essayer de trouver un autre fournisseur de transport pour lui. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu'aucun traitement ne s'est produit et que le spouleur MAPI ne doit pas appeler **EndMessage**.
    
MAPI_E_WAIT 
  
> Un problème temporaire empêche le fournisseur de transport de gérer le message. Le paramètre _lpulReturnParm_ doit être défini sur le nombre de secondes qui doivent s'écouler avant que le spouleur MAPI n'envoie le message. 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon:: SubmitMessage** lorsqu'il a un message que le fournisseur de transport doit livrer. Le message est transmis au fournisseur de transport à l'aide du paramètre _lpMessage_ . 
  
Si le fournisseur est prêt à accepter le message, il doit renvoyer une valeur de référence à l'aide du paramètre _lpulMsgRef_ , traiter l'objet passé et renvoyer la valeur appropriée (généralement S_OK). Si le fournisseur n'est pas prêt à gérer le transfert, il doit renvoyer une valeur d'erreur et, éventuellement, une autre valeur de retour MAPI dans _lpulReturnParm_ pour indiquer la durée pendant laquelle le spouleur MAPI doit attendre avant de renvoyer le message. 
  
L'implémentation d'un fournisseur de transport de cette méthode peut effectuer les opérations suivantes:
  
- Placez le message dans une file d'attente interne pour attendre la transmission, éventuellement en copiant le message vers un emplacement de stockage local, et renvoyez-le.
    
- Tentative d'exécution de la transmission et du retour à la fin de la transmission, que celle-ci soit réussie ou non.
    
- Déterminez s'il faut envoyer le message après avoir vérifié la ressource concernée. Dans ce cas, si la ressource est libre, le fournisseur peut verrouiller la ressource, préparer le message et l'envoyer. Si la ressource est occupée, le fournisseur peut préparer le message et l'envoyer ultérieurement.
    
La technique préférée pour la transmission des messages dépend du fournisseur de transport et du nombre de processus attendus pour les ressources système. 
  
Pendant un appel **SubmitMessage** , le fournisseur de transport contrôle le transfert des données de message à partir de l'objet message. Toutefois, le fournisseur de transport doit affecter une valeur de référence au message, à laquelle il renvoie un pointeur dans _lpulMsgRef_, avant de transférer les données. Elle le fait car, à tout moment pendant le processus, le spouleur MAPI peut appeler la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) avec l'indicateur NOTIFY_CANCEL_MESSAGE défini pour signaler au fournisseur qu'il doit libérer les objets ouverts et arrêter le transfert des messages. 
  
Le fournisseur de transport ne doit pas envoyer de propriétés non transmissibles du message. Lorsqu'elle trouve une telle propriété, elle doit passer au traitement de la propriété suivante. Le fournisseur doit s'efforcer de ne pas afficher les informations de destinataire MAPI_P1 dans le cadre du contenu du message transmis; le fournisseur doit utiliser ces informations de destinataire uniquement à des fins d'adressage. Les destinataires MAPI_P1 sont des destinataires générés en interne qui sont utilisés pour le renvoi de messages; elles ne doivent pas être transmises. À la place, utilisez les autres destinataires pour transmettre les informations des destinataires. L'objectif de cette organisation est de permettre aux destinataires de renvoyer les mêmes tables de destinataires que les destinataires d'origine.
  
Pendant un appel **SubmitMessage** , le spouleur MAPI traite les méthodes pour les objets ouverts lors du transfert du message et traite les pièces jointes. Ce traitement peut prendre beaucoup de temps. Les fournisseurs de transport peuvent appeler la méthode [IMAPISupport:: SpoolerYield](imapisupport-spooleryield.md) pour le spouleur MAPI fréquemment pendant ce traitement afin de libérer le temps processeur pour d'autres tâches système. 
  
Tous les destinataires de message sont visibles dans la table des destinataires du message que le spouleur MAPI a transmis à l'origine. Le fournisseur de transport doit traiter uniquement les destinataires qu'il peut gérer, en fonction de l'identificateur d'entrée, du type d'adresse ou des deux, et que la propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) n'est pas encore définie sur true. Si **PR_RESPONSIBILITY** est déjà défini sur true, un autre fournisseur de transport a géré ce destinataire. Lorsque le fournisseur termine un traitement suffisant d'un destinataire pour déterminer s'il peut gérer les messages pour ce destinataire, il doit définir la propriété **PR_RESPONSIBILITY** de ce destinataire sur true dans le message transmis. En règle générale, le fournisseur effectue cette détermination une fois la remise du message terminée. 
  
En règle générale, le fournisseur de transport ne renvoie pas d'appel **SubmitMessage** tant qu'il n'a pas terminé le transfert des données de message. Si aucune erreur n'est renvoyée, l'appel suivant depuis le spouleur MAPI vers le fournisseur est un appel à la méthode [IXPLogon:: EndMessage](ixplogon-endmessage.md) . 
  
Si **SubmitMessage** renvoie une erreur, le spouleur MAPI libère le message sans enregistrer les modifications. Si le fournisseur de transport exige l'enregistrement des modifications apportées aux messages, il doit appeler la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur le message avant de renvoyer. 
  
Si des erreurs se produisent en raison de problèmes de transport, le spouleur MAPI conserve le message, mais il retarde le renvoi du message au fournisseur de transport en fonction de la valeur renvoyée dans _lpulReturnParm_. Le fournisseur de transport doit remplir cette valeur si sa valeur renvoyée par **SubmitMessage** est MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Si une condition d'erreur grave survient, le fournisseur de transport doit appeler la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) avec l'indicateur NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

