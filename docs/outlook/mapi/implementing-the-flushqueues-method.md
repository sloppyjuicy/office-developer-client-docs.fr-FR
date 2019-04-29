---
title: Implémentation de la méthode FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411777"
---
# <a name="implementing-the-flushqueues-method"></a>Implémentation de la méthode FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le spouleur MAPI utilise la méthode [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) pour télécharger et télécharger les messages en attente vers et à partir d'un fournisseur de transport. En règle générale, le spouleur MAPI vide les files d'attente de tous les fournisseurs de transport qui sont connectés à la session, en commençant par le premier fournisseur de transport défini dans la section ordre de transport du profil de l'utilisateur. Le vidage des files d'attente est presque toujours le résultat d'une demande directe de l'utilisateur, de sorte que l'envoi et la réception de messages pendant le vidage des files d'attente sont synchrones pour le spouleur MAPI. Étant donné que ces appels sont synchrones, le fournisseur de transport doit les traiter aussi rapidement que possible. 
  
Les fournisseurs de transport doivent gérer l'appel **FlushQueues** comme décrit dans la séquence d'étapes suivante pour activer le traitement des messages correct et permettre à d'autres fournisseurs de transport d'utiliser des ressources externes telles que des modems dans le cadre du SPOULEur MAPI. Opération **FlushQueues** . 
  
|**Étape**|**Composant**|**Mise en œuvre**|
|:-----|:-----|:-----|
|1.  <br/> |Spouleur MAPI  <br/> |Appelle la méthode **FlushQueues** pour le premier fournisseur de transport figurant dans l'ordre de transport du profil de l'utilisateur, en transmettant les indicateurs demandés dans le paramètre _ulFlags_ . **FlushQueues** est appelé une seule fois avec tous les indicateurs définis pour l'intégralité de l'opération de téléchargement et de téléchargement.  <br/> |
|2.  <br/> |Fournisseur de transport  <br/> |Doit effectuer un certain nombre d'opérations avant le renvoi de l'appel **FlushQueues** . Si les messages soumis précédemment sont différés, la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) doit être appelée avec l'indicateur NOTIFY_SENT_DEFERRED défini. Notez que le spouleur MAPI peut annuler un message qui a été différé avant que le fournisseur de transport ait pu terminer le traitement du message.  <br/> Si le fournisseur de transport utilise une ressource externe telle qu'un modem, la connexion à la ressource externe doit être établie.  <br/> Le bit STATUS_OUTBOUND_FLUSH de la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d'État du fournisseur de transport doit être défini à l'aide de la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> Le fournisseur de transport doit ensuite renvoyer S_OK pour l'appel **FlushQueues** .  <br/> |
|3.  <br/> |Spouleur MAPI  <br/> |Vérifie la ligne d'État du fournisseur de transport pour le bit STATUS_OUTBOUND_FLUSH et appelle [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) pour le premier message de la file d'attente.  <br/> |
|4.  <br/> |Fournisseur de transport  <br/> |Gère le message et renvoie à partir de l'appel **SubmitMessage** .  <br/> |
|5.  <br/> |Spouleur MAPI  <br/> |Si le fournisseur de transport renvoie S_OK depuis **SubmitMessage**, le spouleur MAPI appelle [IXPLogon:: EndMessage](ixplogon-endmessage.md) pour le message comme il le fait avec l'envoi de messages classiques.  <br/> Si le fournisseur de transport renvoie une valeur autre que S_OK à partir de **SubmitMessage**, le spouleur MAPI gère la valeur de manière appropriée avant d'appeler **EndMessage**ou avant d'appeler de nouveau **SubmitMessage** .  <br/> |
|6.  <br/> |Fournisseur de transport  <br/> |Renvoie de **EndMessage** avec son état de traitement de message dans le paramètre _lpulFlags_ .  <br/> |
|7.  <br/> |Spouleur MAPI et fournisseur de transport  <br/> |La boucle **SubmitMessage**- **EndMessage** continue jusqu'à ce que tous les messages de la file d'attente aient été téléchargés.  <br/> |
|8.  <br/> |Spouleur MAPI  <br/> |Avertit le fournisseur de transport qu'il a terminé de télécharger les messages en appelant la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) du fournisseur de transport avec l'indicateur NOTIFY_END_OUTBOUND_FLUSH défini.  <br/> |
|9.  <br/> |Fournisseur de transport  <br/> |Libère toutes les ressources externes utilisées lors de l'envoi de messages sortants afin qu'ils puissent être utilisés par d'autres fournisseurs de transport pour vider leurs files d'attente.  <br/> Le bit STATUS_INBOUND_FLUSH de la propriété **PR_STATUS_CODE** de la ligne d'État du fournisseur de transport doit être défini à l'aide de **ModifyStatusRow**.  <br/> |
|10.  <br/> |Spouleur MAPI  <br/> |Vérifie la ligne d'État du fournisseur de transport pour le bit STATUS_INBOUND_FLUSH et appelle [IXPLogon:: StartMessage](ixplogon-startmessage.md) s'il est défini.  <br/> |
|11.  <br/> |Fournisseur de transport  <br/> |Traite le message et renvoie à partir de **StartMessage**. Si le fournisseur de transport a d'autres messages à charger, il doit appeler **SpoolerNotify** avec l'indicateur NOTIFY_NEWMAIL défini.  <br/> Si le fournisseur de transport n'a aucun message à charger, il doit appeler [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) sur le message le spouleur MAPI transmis dans **StartMessage** et Return.  <br/> |
|an.  <br/> |Spouleur MAPI  <br/> |Continue d'appeler **StartMessage** jusqu'à ce que **SaveChanges** soit appelé sur un message. Une fois le téléchargement du fournisseur de transport terminé, le spouleur MAPI appelle **TransportNotify** avec l'indicateur NOTIFY_END_INBOUND_FLUSH défini.  <br/> |
|kg.  <br/> |Fournisseur de transport  <br/> |Efface le bit STATUS_INBOUND_FLUSH de la propriété **PR_STATUS_CODE** de sa ligne d'État à l'aide de **ModifyStatusRow** et libère toutes les ressources externes de sorte qu'elles soient utilisables par d'autres fournisseurs de transport.  <br/> |
|13.  <br/> |Spouleur MAPI  <br/> |Appelle **FlushQueues** pour le fournisseur de transport suivant indiqué dans l'ordre de transport du profil de l'utilisateur.  <br/> |
   
Si une application cliente appelle [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) sur l'objet d'état d'un fournisseur de transport, le fournisseur de transport doit définir le bit approprié dans sa ligne d'État avec **ModifyStatusRow**. Le spouleur MAPI appelle ensuite la méthode **IXPLogon:: FlushQueues** du fournisseur de transport au niveau de la commodité du spouleur MAPI. Lorsque la méthode **IXPLogon:: FlushQueues** du fournisseur de transport est appelée à la suite de l'appel de **IMAPIStatus:: FlushQueues** de l'application cliente, l'opération a lieu de manière asynchrone à l'application cliente. Sinon, **IXPLogon:: FlushQueues** fonctionne de façon synchrone avec le spouleur MAPI. 
  
Pour des raisons de performances, le spouleur MAPI appelle uniquement la méthode **FlushQueues** d'un fournisseur de transport si les indicateurs STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH sont définis dans la ligne d'État du fournisseur de transport. Par conséquent, un fournisseur de transport peut arrêter l'opération **FlushQueues** à tout moment en effaçant les indicateurs STATUS_OUTBOUND_FLUSH et STATUS_INBOUND_FLUSH dans sa ligne d'État. Si le spouleur MAPI est arrêté et doit mettre fin à l'opération **FlushQueues** , il appelle **TransportNotify** avec les indicateurs NOTIFY_END_INBOUND_FLUSH et NOTIFY_END_OUTBOUND_FLUSH définis. Le fournisseur de transport doit libérer toutes les ressources externes et renvoyer. 
  

