---
title: Implémentation de la méthode FlushQueues
description: Le spouleur MAPI utilise la méthode IXPLogon FlushQueues pour télécharger et charger tous les messages en attente vers et depuis un fournisseur de transport.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
ms.openlocfilehash: b2cfd75e80d60a7d433b7d8a3ad0b7a9bc353a4b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826924"
---
# <a name="implementing-the-flushqueues-method"></a>Implémentation de la méthode FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le spouleur MAPI utilise la méthode [IXPLogon::FlushQueues](ixplogon-flushqueues.md) pour télécharger et charger tous les messages en attente vers et depuis un fournisseur de transport. En règle générale, le spouleur MAPI vide les files d’attente de tous les fournisseurs de transport connectés à la session, en commençant par le premier fournisseur de transport défini dans la section ordre de transport du profil de l’utilisateur. Le vidage des files d’attente est presque toujours le résultat d’une requête directe de l’utilisateur. Par conséquent, l’envoi et la réception de messages pendant le vidage des files d’attente sont synchrones pour le spouleur MAPI. Étant donné que ces appels sont synchrones, le fournisseur de transport doit les traiter aussi rapidement que possible. 
  
Les fournisseurs de transport doivent gérer l’appel **FlushQueues** comme décrit dans la séquence suivante d’étapes pour activer le traitement approprié des messages et permettre aux ressources externes telles que les modems d’être utilisées par d’autres fournisseurs de transport dans le cadre de l’opération **FlushQueues** du spouleur MAPI. 
  
|**Étape**|**Composant**|**Mise en œuvre**|
|:-----|:-----|:-----|
|1. |Spouleur MAPI  <br/> |Appelle la méthode **FlushQueues** pour le premier fournisseur de transport répertorié dans l’ordre de transport du profil de l’utilisateur, en passant les indicateurs demandés dans le paramètre _ulFlags_ . **FlushQueues** est appelé une seule fois avec tous les indicateurs définis pour l’ensemble de l’opération de chargement et de téléchargement. |
|2. |Fournisseur de transport  <br/> |Doit effectuer plusieurs opérations avant de revenir de l’appel **FlushQueues** . Si les messages précédemment envoyés sont différés, la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) doit être appelée avec l’indicateur NOTIFY_SENT_DEFERRED défini. Notez qu’il est possible pour le spouleur MAPI d’annuler un message qui a été différé avant que le fournisseur de transport ait la possibilité de terminer le traitement du message. Si le fournisseur de transport utilise une ressource externe telle qu’un modem, la connexion à la ressource externe doit être établie. Le bit STATUS_OUTBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état du fournisseur de transport doit être défini à l’aide de la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Le fournisseur de transport doit ensuite retourner S_OK pour l’appel **FlushQueues** . |
|3. |Spouleur MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour le bit STATUS_OUTBOUND_FLUSH et appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) pour le premier message dans la file d’attente. |
|4. |Fournisseur de transport  <br/> |Gère le message et retourne à partir de l’appel **SubmitMessage** . |
|5. |Spouleur MAPI  <br/> |Si le fournisseur de transport retourne S_OK à partir de **SubmitMessage**, le spouleur MAPI appelle [IXPLogon::EndMessage](ixplogon-endmessage.md) pour le message comme il le fait avec l’envoi régulier de messages. Si le fournisseur de transport retourne une valeur autre que S_OK de **SubmitMessage**, le spouleur MAPI gère la valeur de manière appropriée avant d’appeler **EndMessage** ou avant d’appeler **SubmitMessage** à nouveau. |
|6. |Fournisseur de transport  <br/> |Renvoie **d’EndMessage** avec son état de traitement des messages dans le paramètre _lpulFlags_ . |
|7. |Spouleur et fournisseur de transport MAPI  <br/> |La boucle **SubmitMessage**- **EndMessage** se poursuit jusqu’à ce que tous les messages de la file d’attente aient été téléchargés. |
|8. |Spouleur MAPI  <br/> |Avertit le fournisseur de transport qu’il a terminé de télécharger les messages en appelant la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) du fournisseur de transport avec l’indicateur NOTIFY_END_OUTBOUND_FLUSH défini. |
|9. |Fournisseur de transport  <br/> |Libère toutes les ressources externes utilisées pour envoyer des messages sortants afin qu’elles puissent être utilisées par d’autres fournisseurs de transport pour vider leurs files d’attente. Le bit STATUS_INBOUND_FLUSH dans la propriété **PR_STATUS_CODE** de la ligne d’état du fournisseur de transport doit être défini à l’aide de **ModifyStatusRow**. |
|10. |Spouleur MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour le bit STATUS_INBOUND_FLUSH et appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) s’il est défini. |
|11. |Fournisseur de transport  <br/> |Traite le message et retourne à partir de **StartMessage**. Si le fournisseur de transport a d’autres messages à charger, il doit appeler **SpoolerNotify** avec l’indicateur NOTIFY_NEWMAIL défini. Si le fournisseur de transport n’a aucun message à charger, il doit appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message transmis par le spouleur MAPI dans **StartMessage** et retourné. |
|12. |Spouleur MAPI  <br/> |Continue à appeler **StartMessage** jusqu’à ce que **SaveChanges** soit appelé sur un message. Une fois le chargement du fournisseur de transport terminé, le spouleur MAPI appelle **TransportNotify** avec l’indicateur NOTIFY_END_INBOUND_FLUSH défini. |
|13. |Fournisseur de transport  <br/> |Efface le STATUS_INBOUND_FLUSH bit dans la propriété **PR_STATUS_CODE** de sa ligne d’état à l’aide de **ModifyStatusRow** et libère toutes les ressources externes afin qu’elles soient disponibles pour être utilisées par d’autres fournisseurs de transport. |
|14. |Spouleur MAPI  <br/> |Appelle **FlushQueues** pour le fournisseur de transport suivant répertorié dans l’ordre de transport du profil de l’utilisateur. |
   
Si une application cliente appelle [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) sur l’objet d’état d’un fournisseur de transport, le fournisseur de transport doit définir le bit approprié dans sa ligne d’état avec **ModifyStatusRow**. Le spouleur MAPI appelle ensuite la méthode **IXPLogon::FlushQueues** du fournisseur de transport à la convenance du spouleur MAPI. Lorsque la méthode **IXPLogon::FlushQueues** du fournisseur de transport est appelée à la suite de l’appel **IMAPIStatus::FlushQueues** d’une application cliente, l’opération se produit de façon asynchrone pour l’application cliente. Sinon **, IXPLogon::FlushQueues** fonctionne de façon synchrone avec le spouleur MAPI. 
  
Pour des raisons de performances, le spouleur MAPI appelle uniquement la méthode **FlushQueues** d’un fournisseur de transport si les indicateurs STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH sont définis dans la ligne d’état du fournisseur de transport. Par conséquent, un fournisseur de transport peut arrêter l’opération **FlushQueues** à tout moment en effaçant les indicateurs STATUS_OUTBOUND_FLUSH et STATUS_INBOUND_FLUSH dans sa ligne d’état. Si le spouleur MAPI s’arrête et doit mettre fin à l’opération **FlushQueues** , il appelle **TransportNotify** avec les indicateurs NOTIFY_END_INBOUND_FLUSH et NOTIFY_END_OUTBOUND_FLUSH définis. Le fournisseur de transport doit libérer toutes les ressources externes et retourner. 
  

