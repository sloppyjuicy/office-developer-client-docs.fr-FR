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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 28e7874d1e61c0a4fe0ad702f206ca03a9a1096a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575874"
---
# <a name="ixplogonsubmitmessage"></a>IXPLogon::SubmitMessage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique qu’un message pour le fournisseur de transport fournir le spouleur MAPI.
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMsgRef,
  ULONG FAR * lpulReturnParm
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont le message est envoyé. Vous pouvez définir l’indicateur suivant :
    
BEGIN_DEFERRED 
  
> Le spouleur MAPI appelle un fournisseur de transport avec un message qui a été différé précédemment. L’identificateur d’entrée du message est la même que lorsqu’il a été différé. Le message a été différé en passant son identificateur d’entrée sur le spouleur MAPI à l’aide de la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_SENTDEFERRED. 
    
 _lpMessage_
  
> [in] Pointeur vers un objet de message (représentant le message à remettre) ayant l’autorisation de lecture/écriture, qui repose sur le fournisseur de transport pour accéder et manipuler ce message. Cet objet restera valide jusqu'à une fois que le fournisseur de transport renvoie à partir d’un appel suivant à la méthode [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
    
 _lpulMsgRef_
  
> [out] Un pointeur vers une variable dans laquelle le fournisseur de transport renvoie la valeur de référence, elle attribuée à ce message. Le spouleur MAPI transmet la valeur de cette référence dans les appels suivants pour ce message. Le spouleur MAPI initialise la valeur 0 avant leur renvoi le fournisseur de transport.
    
 _lpulReturnParm_
  
> [out] Pointeur vers une variable qui correspond à la valeur d’erreur MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR retournée par **SubmitMessage**.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi et renvoyé la valeur attendue ou les valeurs.
    
MAPI_E_BUSY 
  
> Le fournisseur de transport ne peut pas gérer le message, car il effectue une autre opération. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu’aucun traitement s’est produite et que le spouleur MAPI ne doit pas appeler **EndMessage**. Le spouleur MAPI essaiera l’appel **SubmitMessage** ultérieurement. 
    
MAPI_E_CANCEL 
  
> Bien que le fournisseur de transport demandé que le spouleur MAPI de resoumettre sur un appel **SpoolerNotify** précédent, étant donné que les conditions ont changé et le message ne doit pas être renvoyé. Le spouleur MAPI va continuer pour gérer autre chose. 
    
MAPI_E_NETWORK_ERROR 
  
> Une erreur réseau a empêché la réussite de l’opération. Le paramètre _lpulReturnParm_ doit être défini pour le nombre de secondes devant s’écouler avant le spouleur MAPI renvoie le message. 
    
MAPI_E_NOT_ME 
  
> Le fournisseur de transport ne peut pas gérer ce message. Le spouleur MAPI doit essayer de rechercher un autre fournisseur de transport. Un fournisseur doit utiliser cette valeur de retour pour indiquer qu’aucun traitement s’est produite et que le spouleur MAPI ne doit pas appeler **EndMessage**.
    
MAPI_E_WAIT 
  
> Un problème temporaire empêche le fournisseur de transport de gestion du message. Le paramètre _lpulReturnParm_ doit être défini pour le nombre de secondes devant s’écouler avant le spouleur MAPI renvoie le message. 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPLogon::SubmitMessage** lorsqu’il a un message pour le fournisseur de transport fournir. Le message est transmis au fournisseur de transport à l’aide du paramètre _lpMessage_ . 
  
Si le fournisseur est prêt à accepter le message, il doit renvoyer une valeur de référence en utilisant le paramètre _lpulMsgRef_ , processus de l’objet passé et renvoyer la valeur appropriée (généralement S_OK). Si le fournisseur n’est pas prêt à gérer le transfert, elle doit renvoyer une valeur d’erreur et, éventuellement, MAPI une autre valeur de retour dans _lpulReturnParm_ pour indiquer la durée pendant laquelle le spouleur MAPI doit attendre avant de soumettre le message. 
  
Implémentation d’un fournisseur de transport de cette méthode peut procédez comme suit :
  
- Placez le message dans une file d’attente pour la transmission, éventuellement copier le message vers un stockage local, interne et retourner.
    
- Essayez d’effectuer la transmission réelle et renvoyer une fois terminée la transmission, avec ou sans succès.
    
- Déterminer s’il faut envoyer le message après avoir vérifié les ressources nécessaires. Dans ce cas, si la ressource est disponible, le fournisseur peut verrouiller la ressource, préparer le message et l’envoyer. Si la ressource est occupé (e), le fournisseur peut préparer le message et différer l’envoi à une date ultérieure.
    
La méthode recommandée pour la transmission des messages varie selon le fournisseur de transport et le nombre attendu de processus en concurrence pour les ressources système. 
  
Pendant un appel **SubmitMessage** , le fournisseur de transport contrôle le transfert des données des messages à partir de l’objet du message. Toutefois, le fournisseur de transport doit affecter une valeur de référence pour le message, à laquelle il retourne un pointeur dans _lpulMsgRef_, avant le transfert de données. Elle donc car à tout moment au cours du processus, le spouleur MAPI peut appeler la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) avec l’indicateur NOTIFY_CANCEL_MESSAGE définit pour signaler le fournisseur qu’il doit libérer tous les objets ouverts et arrêter le transfert de messages. 
  
Le fournisseur de transport ne doit pas envoyer toutes les propriétés nontransmittable du message. Lorsqu’il trouve ce type de propriété, il doit passer à traiter la propriété suivante. Le fournisseur doit faire le maximum ne pas pour afficher les informations relatives au destinataire MAPI_P1 dans le cadre du contenu message transmis ; le fournisseur doit utiliser ces informations destinataires uniquement pour l’adressage à des fins. Destinataires MAPI_P1 sont destinataires internes qui sont utilisées pour renvoyer des messages ; ils ne doivent pas être transmises. Au lieu de cela, utilisez les autres destinataires pour la transmission des informations relatives au destinataire. L’objectif de cette organisation est permet de renvoyer les destinataires pour afficher la même table destinataire exacte en tant que les destinataires d’origine.
  
Pendant un appel **SubmitMessage** , le spouleur MAPI traite des méthodes pour les objets qui sont ouverts lors du transfert du message, et il traite les pièces jointes. Ce traitement peut prendre beaucoup de temps. Fournisseurs de transport peuvent appeler la méthode [IMAPISupport::SpoolerYield](imapisupport-spooleryield.md) pour le spouleur MAPI fréquemment lors du traitement de ce temps processeur pour les autres tâches du système de publication. 
  
Tous les destinataires du message sont visibles dans le tableau destinataire du message que le spouleur MAPI transmis à l’origine. Le fournisseur de transport doit traiter seuls les destinataires qu’il peut traiter, en fonction de l’identificateur d’entrée, le type d’adresse ou les deux — et qui n’ont pas encore leur propriété **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) la valeur TRUE. Si **PR_RESPONSIBILITY** est déjà défini sur TRUE, un autre fournisseur de transport a traité ce destinataire. Lorsque le fournisseur est terminée suffisante traitement d’un destinataire pour déterminer si elle peut gérer les messages du destinataire, il doit définir la propriété **PR_RESPONSIBILITY** de ce destinataire sur TRUE dans le message transmis. En règle générale, le fournisseur pour ce faire après que la remise du message est terminée. 
  
En règle générale, le fournisseur de transport ne renvoie pas d’un appel **SubmitMessage** jusqu'à la fin du transfert de données de message. Si aucune erreur n’est renvoyée, l’appel suivant du spouleur MAPI pour le fournisseur est un appel à la méthode [IXPLogon::EndMessage](ixplogon-endmessage.md) . 
  
Si **SubmitMessage** renvoie une erreur, le spouleur MAPI libère le message en cours sans enregistrer les modifications. Si le fournisseur de transport requiert message change le point d’être enregistrées, il doit appeler la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message avant de retourner. 
  
En cas d’erreurs qui se produisent en raison de problèmes de transport, le spouleur MAPI conserve le message, mais il diffère le renvoi du message pour le fournisseur de transport en fonction de la valeur renvoyée dans _lpulReturnParm_. Le fournisseur de transport doit remplir cette valeur si sa valeur de retour de **SubmitMessage** est MAPI_E_WAIT ou MAPI_E_NETWORK_ERROR. Si une condition d’erreur grave se produit, le fournisseur de transport doit appeler la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) avec l’indicateur NOTIFY_CRITICAL_ERROR. 
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
  
[IMAPISupport::SpoolerYield](imapisupport-spooleryield.md)
  
[IXPLogon::EndMessage](ixplogon-endmessage.md)
  
[IXPLogon::TransportNotify](ixplogon-transportnotify.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

