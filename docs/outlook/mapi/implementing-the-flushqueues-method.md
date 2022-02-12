---
title: Mise en œuvre de la méthode FlushQueues
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f9884a134523221c01a225e136c73c066037bcf9
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62773368"
---
# <a name="implementing-the-flushqueues-method"></a>Mise en œuvre de la méthode FlushQueues

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lepooler MAPI utilise la méthode [IXPLogon::FlushQueues](ixplogon-flushqueues.md) pour télécharger et télécharger les messages en attente vers et à partir d’un fournisseur de transport. En règle générale, lepooler MAPI vide les files d’attente de tous les fournisseurs de transport qui sont connectés à la session, en commençant par le premier fournisseur de transport tel qu’il est définie dans la section ordre de transport du profil de l’utilisateur. Le  purgement des files d’attente est presque toujours le résultat d’une demande directe de l’utilisateur, de sorte que l’envoi et la réception de messages pendant le  purgement des files d’attente sont synchrones avec lepooler MAPI. Étant donné que ces appels sont synchrones, le fournisseur de transport doit les traiter aussi rapidement que possible. 
  
Les fournisseurs de transport doivent gérer l’appel **FlushQueues** comme décrit dans la séquence d’étapes suivante pour activer le traitement correct des messages et permettre à des ressources externes telles que des modems d’être utilisées par d’autres fournisseurs de transport dans le cadre de l’opération **FlushQueues** dupooler MAPI. 
  
|**Étape**|**Composant**|**Mise en œuvre**|
|:-----|:-----|:-----|
|1. |Pooler MAPI  <br/> |Appelle la **méthode FlushQueues** pour le premier fournisseur de transport répertorié dans l’ordre de transport du profil de l’utilisateur, en passant les indicateurs demandés dans le paramètre _ulFlags_ . **FlushQueues est appelé une** seule fois avec tous les indicateurs définies pour l’ensemble de l’opération de chargement et de téléchargement. |
|2. |Fournisseur de transport  <br/> |Doit faire un certain nombre d’éléments avant de revenir à partir de **l’appel FlushQueues** . Si les messages envoyés précédemment sont différés, la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) doit être appelée avec l NOTIFY_SENT_DEFERRED état. Notez qu’il est possible pour lepooler MAPI d’annuler un message différé avant que le fournisseur de transport ait la possibilité de terminer le traitement du message. Si le fournisseur de transport utilise une ressource externe telle qu’un modem, la connexion à la ressource externe doit être établie. Le bit STATUS_OUTBOUND_FLUSH dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de la ligne d’état du fournisseur de transport doit être définie à l’aide de la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . Le fournisseur de transport doit ensuite renvoyer S_OK pour **l’appel FlushQueues** . |
|3. |Pooler MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour le bit STATUS_OUTBOUND_FLUSH et appelle [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) pour le premier message de la file d’attente. |
|4. |Fournisseur de transport  <br/> |Gère le message et renvoie le message à partir de **l’appel SubmitMessage** . |
|5. |Pooler MAPI  <br/> |Si le fournisseur de transport renvoie S_OK à partir de **SubmitMessage**, lepooler MAPI appelle [IXPLogon::EndMessage](ixplogon-endmessage.md) pour le message comme il le fait avec l’envoi de message normal. Si le fournisseur de transport renvoie une valeur autre que S_OK à partir de **SubmitMessage**, lepooler MAPI gère la valeur de manière appropriée avant d’appeler **EndMessage** ou d’appeler **à nouveau SubmitMessage** . |
|6. |Fournisseur de transport  <br/> |Renvoie à **partir de EndMessage avec** son état de traitement des messages dans _le paramètre lpulFlags_ . |
|7. |Fournisseur de transport et depooler MAPI  <br/> |La **boucle SubmitMessageEndMessage**-  continue jusqu’à ce que tous les messages de la file d’attente soient téléchargés. |
|8. |Pooler MAPI  <br/> |Avertit le fournisseur de transport qu’il a terminé le téléchargement des messages en appelant la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) du fournisseur de transport avec l’indicateur NOTIFY_END_OUTBOUND_FLUSH définie. |
|9. |Fournisseur de transport  <br/> |Libère toutes les ressources externes utilisées pour envoyer des messages sortants afin qu’elles soient utilisées par d’autres fournisseurs de transport pour vider leurs files d’attente. Le bit STATUS_INBOUND_FLUSH la propriété **PR_STATUS_CODE** de la ligne d’état du fournisseur de transport doit être définie à l’aide **de ModifyStatusRow**. |
|10. |Pooler MAPI  <br/> |Vérifie la ligne d’état du fournisseur de transport pour STATUS_INBOUND_FLUSH bit et appelle [IXPLogon::StartMessage](ixplogon-startmessage.md) si elle est définie. |
|11. |Fournisseur de transport  <br/> |Traite le message et renvoie à partir **de StartMessage**. Si le fournisseur de transport a d’autres messages à télécharger, il doit appeler **SpoolerNotify** avec l’indicateur NOTIFY_NEWMAIL de transport. Si le fournisseur de transport n’a aucun message à télécharger, il doit appeler [IMAPIProp::SaveChanges](imapiprop-savechanges.md) sur le message que lepooler MAPI a transmis dans **StartMessage** et retourner. |
|12. |Pooler MAPI  <br/> |Continue **d’appeler StartMessage** **jusqu’à ce que SaveChanges** soit appelé sur un message. Une fois que le fournisseur de transport a terminé le chargement, lepooler MAPI appelle **TransportNotify** avec l’indicateur NOTIFY_END_INBOUND_FLUSH de transport. |
|13. |Fournisseur de transport  <br/> |Cette propriété STATUS_INBOUND_FLUSH la propriété **PR_STATUS_CODE** de sa ligne d’état à l’aide de **ModifyStatusRow** et libère toutes les ressources externes afin qu’elles soient disponibles pour une utilisation par d’autres fournisseurs de transport. |
|14. |Pooler MAPI  <br/> |Appelle **FlushQueues pour** le fournisseur de transport suivant répertorié dans l’ordre de transport du profil de l’utilisateur. |
   
Si une application cliente appelle [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) sur l’objet d’état d’un fournisseur de transport, le fournisseur de transport doit définir le bit approprié dans sa ligne d’état avec **ModifyStatusRow**. Lepooler MAPI appelle ensuite la méthode **IXPLogon::FlushQueues** du fournisseur de transport au convenance dupooler MAPI. Lorsque la méthode **IXPLogon::FlushQueues** du fournisseur de transport est appelée à la suite de l’appel **IMAPIStatus::FlushQueues** d’une application cliente, l’opération se produit de manière asynchrone sur l’application cliente. Sinon **, IXPLogon::FlushQueues** fonctionne de manière synchrone avec lepooler MAPI. 
  
Pour des raisons de performances, lepooler MAPI appelle uniquement la méthode **FlushQueues** d’un fournisseur de transport si les indicateurs STATUS_INBOUND_FLUSH et STATUS_OUTBOUND_FLUSH sont définies dans la ligne d’état du fournisseur de transport. Par conséquent, un fournisseur de transport peut arrêter l’opération **FlushQueues** à tout moment en effaçant les indicateurs STATUS_OUTBOUND_FLUSH et STATUS_INBOUND_FLUSH dans sa ligne d’état. Si lepooler MAPI s’arrête et doit mettre fin à l’opération **FlushQueues** , il appelle **TransportNotify** avec les indicateurs NOTIFY_END_INBOUND_FLUSH et NOTIFY_END_OUTBOUND_FLUSH définies. Le fournisseur de transport doit libérer toutes les ressources externes et retourner. 
  

