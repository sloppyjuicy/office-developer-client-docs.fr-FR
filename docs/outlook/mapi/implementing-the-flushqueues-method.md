---
title: Implémentation de la méthode FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: baafd8b6437f4febaee9420b274c20ba3242cae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784209"
---
# <a name="implementing-the-flushqueues-method"></a>Implémentation de la méthode FlushQueues

  
  
**S’applique à**: Outlook 
  
Le spouleur MAPI utilise la méthode [IXPLogon::FlushQueues](ixplogon-flushqueues.md) pour télécharger tous les messages en attente vers et à partir d’un fournisseur de transport. En règle générale, le spouleur MAPI système vider les files d’attente pour tous les fournisseurs de transport qui sont connectés à la session, commençant par le premier fournisseur de transport tels que définis dans la section ordre de transport de profil de l’utilisateur. Files d’attente de vidage est presque toujours le résultat d’une requête directe par l’utilisateur, afin des envoyer et recevoir des messages pendant la purge des files d’attente sont synchrone pour le spouleur MAPI. Étant donné que ces appels sont synchrones, le fournisseur de transport doit traiter aussi rapidement que possible. 
  
Fournisseurs de transport doivent gérer l’appel **FlushQueues** comme décrit dans la séquence d’étapes suivante pour activer le traitement de message approprié et activer des ressources externes telles que les modems à être utilisé par d’autres fournisseurs de transport dans le cadre de du spouleur MAPI Opération **FlushQueues** . 
  
|**Étape**|**Composant**|**Implémentation**|
|:-----|:-----|:-----|
|1.  <br/> |Spouleur MAPI  <br/> |Appelle la méthode **FlushQueues** pour le premier fournisseur de transport répertorié dans l’ordre de transport du profil de l’utilisateur, en passant les indicateurs demandés dans le paramètre _ulFlags_ . **FlushQueues** est appelée une seule fois avec tous les indicateurs définis pour l’intégralité du téléchargement et l’opération de téléchargement.  <br/> |
|2.  <br/> |Fournisseur de transport  <br/> |Doit effectuer un certain nombre de choses avant le retour de l’appel **FlushQueues** . Si précédemment envoyé différés des messages, la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) doit être appelée avec l’indicateur NOTIFY_SENT_DEFERRED. Notez qu’il est possible pour le spouleur MAPI annuler un message qui a été différé avant que le fournisseur de transport a un risque pour terminer le traitement du message.  <br/> Si le fournisseur de transport utilise une ressource externe comme un modem, la connexion à la ressource externe doit être établie.  <br/> Le bit dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état du fournisseur de transport STATUS_OUTBOUND_FLUSH doit être définie à l’aide de la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) .  <br/> Le fournisseur de transport doit renvoie S_OK pour l’appel de **FlushQueues** .  <br/> |
|3.  <br/> |Spouleur MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour le bit STATUS_OUTBOUND_FLUSH et appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) pour le premier message dans la file d’attente.  <br/> |
|4.  <br/> |Fournisseur de transport  <br/> |Gère le message et renvoie à partir de l’appel **SubmitMessage** .  <br/> |
|5.  <br/> |Spouleur MAPI  <br/> |Si le fournisseur de transport renvoie S_OK de **SubmitMessage**, le spouleur MAPI appelle [IXPLogon::EndMessage](ixplogon-endmessage.md) pour le message qu’avec l’envoi de message ordinaire.  <br/> Si le fournisseur de transport renvoie une valeur autre que S_OK de **SubmitMessage**, le spouleur MAPI gère la valeur appropriée avant d’appeler **EndMessage**ou avant d’appeler **SubmitMessage** à nouveau.  <br/> |
|6.  <br/> |Fournisseur de transport  <br/> |Renvoie à partir de **EndMessage** avec son statut dans le paramètre _lpulFlags_ de traitement du message.  <br/> |
|7.  <br/> |Fournisseur de transport et spouleur MAPI  <br/> |Le **SubmitMessage**- **EndMessage** boucle continue jusqu'à ce que tous les messages de la file d’attente ont été téléchargés.  <br/> |
|8.  <br/> |Spouleur MAPI  <br/> |Notifie le fournisseur de transport qu’il a terminé le téléchargement des messages en appelant la méthode de [IXPLogon::TransportNotify](ixplogon-transportnotify.md) du fournisseur de transport avec l’indicateur NOTIFY_END_OUTBOUND_FLUSH.  <br/> |
|9.  <br/> |Fournisseur de transport  <br/> |Libère toutes les ressources externes utilisées dans l’envoi de messages sortants afin qu’ils puissent être utilisées par d’autres fournisseurs de transport pour vider les files d’attente.  <br/> Le bit dans la propriété **PR_STATUS_CODE** de la ligne d’état du fournisseur de transport STATUS_INBOUND_FLUSH doit être définie à l’aide de **ModifyStatusRow**.  <br/> |
|10.  <br/> |Spouleur MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour le bit STATUS_INBOUND_FLUSH et appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) si elle est définie.  <br/> |
|11.  <br/> |Fournisseur de transport  <br/> |Traite le message et le renvoie à partir de **StartMessage**. Si le fournisseur de transport possède d’autres messages à télécharger, il doit appeler **SpoolerNotify** avec l’indicateur NOTIFY_NEWMAIL.  <br/> Si le fournisseur de transport n’a aucun message à télécharger, il doit appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message le spouleur MAPI passé dans **StartMessage** et retourner.  <br/> |
|12.  <br/> |Spouleur MAPI  <br/> |Continue à appeler **StartMessage** jusqu'à ce que **SaveChanges** est appelée sur un message. Une fois le fournisseur de transport téléchargement est terminé, le spouleur MAPI appelle **TransportNotify** avec l’indicateur NOTIFY_END_INBOUND_FLUSH.  <br/> |
|13.  <br/> |Fournisseur de transport  <br/> |Efface le STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** de sa ligne d’état à l’aide de **ModifyStatusRow** et utilisent toutes les ressources externes afin qu’elles soient disponibles pour les versions de bit par d’autres fournisseurs de transport.  <br/> |
|14.  <br/> |Spouleur MAPI  <br/> |Appelle **FlushQueues** pour le fournisseur de transport suivant répertorié dans l’ordre de transport de profil de l’utilisateur.  <br/> |
   
Si un client application appelle [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) sur l’objet d’état d’un fournisseur de transport, le fournisseur de transport doit définir le bit approprié dans sa ligne d’état avec **ModifyStatusRow**. Le spouleur MAPI appelle ensuite la méthode de **IXPLogon::FlushQueues** du fournisseur de transport à commodité du spouleur MAPI. Lorsque les méthode de **IXPLogon::FlushQueues** du fournisseur de transport est appelée à la suite d’appel de **IMAPIStatus::FlushQueues** d’une application client, l’opération est effectuée de manière asynchrone à l’application cliente. Dans le cas contraire **IXPLogon::FlushQueues** fonctionne de façon synchrone avec le spouleur MAPI. 
  
Pour des raisons de performances, le spouleur MAPI système appelez **FlushQueues** méthode d’un fournisseur transport uniquement si les indicateurs STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH sont définis dans la ligne d’état du fournisseur de transport. Par conséquent, un fournisseur de transport peut arrêter l’opération **FlushQueues** à tout moment en désactivant les indicateurs STATUS_OUTBOUND_FLUSH et STATUS_INBOUND_FLUSH dans sa ligne d’état. Si le spouleur MAPI s’arrête et doit mettre fin à l’opération **FlushQueues** , il appelle **TransportNotify** avec le NOTIFY_END_INBOUND_FLUSH et NOTIFY_END_OUTBOUND_FLUSH flags définie. Le fournisseur de transport doit libérer toutes les ressources externes et retourner. 
  

