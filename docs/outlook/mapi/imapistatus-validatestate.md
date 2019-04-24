---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: adcdf04653f8c9fed2ecc6520648abd3acd36134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331548"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Confirme les informations d'état externe disponibles pour la ressource MAPI ou le fournisseur de services. Cette méthode est prise en charge dans tous les objets d'État. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_ulUIParam_
  
> dans Handle de la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche.
    
_ulFlags_
  
> dans Masque de des indicateurs qui contrôle la validation. Les indicateurs suivants peuvent être définis:
    
ABORT_XP_HEADER_OPERATION
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue correspondante. L'objet Status comporte deux options: 
    
   - Continuez à travailler sur l'opération.
    
   - Arrêtez l'opération et retournez MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Une ou plusieurs propriétés de configuration de l'objet Status ont été modifiées. Les clients peuvent définir cet indicateur pour autoriser le spouleur MAPI à corriger de manière dynamique les échecs des fournisseurs de transport critiques. 
    
FORCE_XP_CONNECT 
  
> L'objet Status doit effectuer une connexion. Lorsque cet indicateur est utilisé avec l'indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la connexion s'effectue sans mise en cache.
    
FORCE_XP_DISCONNECT 
  
> L'objet Status doit effectuer une opération de déconnexion. Lorsque cet indicateur est utilisé avec l'indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la déconnexion s'effectue sans mise en cache.
    
PROCESS_XP_HEADER_CACHE 
  
> Les entrées de la table de cache d'en-tête doivent être traitées, tous les messages marqués avec l'indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l'indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés. Les messages qui ont à la fois MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE doivent être déplacés.
    
REFRESH_XP_HEADER_CACHE 
  
> Pour un fournisseur de transport distant, une nouvelle liste des en-têtes de message doit être téléchargée et tous les indicateurs qui signalent l'état du message doivent être effacés.
    
SUPPRESS_UI 
  
> Empêche l'objet d'état d'afficher une interface utilisateur dans le cadre de l'opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La validation a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours; il doit être autorisé à se terminer ou doit être arrêté avant l'exécution de cette opération.
    
MAPI_E_NO_SUPPORT 
  
> L'objet Status ne prend pas en charge la méthode de validation, comme indiqué par l'absence de l'indicateur STATUS_VALIDATE_STATE dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération de validation, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. Cette valeur est renvoyée uniquement par les fournisseurs de transport à distance. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus:: ValidateState** vérifie l'état d'une ressource associée à un objet Status. **ValidateState** est la seule méthode de l'interface [IMAPIStatus](imapistatusimapiprop.md) requise pour tous les objets d'État. Le comportement exact de cette méthode dépend de l'implémentation. Le tableau suivant décrit l'implémentation de chacun des différents types d'objets d'État. 
  
|**Objet Status**|ValidateState * * Implementation * *|
|:-----|:-----|
|Sous-système MAPI  <br/> |Valide l'état de toutes les ressources propres aux fournisseurs de services actifs et au sous-système proprement dit.  <br/> |
|Spouleur MAPI  <br/> |Effectue une ouverture de session de tous les fournisseurs de transport, qu'ils soient déjà connectés ou non.  <br/> |
|Carnet d'adresses MAPI  <br/> |Vérifie les entrées dans la section profil.  <br/> |
|Fournisseur de services  <br/> |L'implémentation dépend du type de fournisseur et des indicateurs définis dans le paramètre _ulFlags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les applications clientes disTantes appellent la méthode **ValidateState** pour démarrer le traitement à distance pour diverses actions. Cette méthode existe principalement pour définir des bits d'État pour communiquer avec le spouleur MAPI, au lieu de faire un travail. En règle générale, le fournisseur de transport définit des indicateurs dans sa ligne d'État qui indiquent au spouleur MAPI les actions à effectuer pour terminer la demande du client. 

Dans ce modèle d'interaction client-transport-Spooler, les actions demandées par le client sont asynchrones, dans cette **ValidateState** renvoie avant que les actions demandées ne soient terminées. Toutefois, les actions qui n'impliquent pas nécessairement le système de messagerie sous-jacent ou qui impliquent une interface spécifique au transport peuvent être synchrones. L'application cliente transmet un masque de masque des indicateurs suivants pour spécifier les actions que le fournisseur de transport distant doit effectuer. 
  
ABORT_XP_HEADER_OPERATION 
  
> Dans la mesure du possible, le fournisseur de transport distant doit annuler toutes les opérations impliquant le téléchargement des en-têtes. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d'état de l'objet d'ouverture de session:
    
   - Effacez les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE de la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) pour indiquer au spouleur MAPI d'arrêter le processus de vidage entrant pour ce fournisseur de transport.
    
   - Définissez le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** . 
    
   - Définissez la propriété **PR_REMOTE_VALIDATE_OK** ([PIDTAGREMOTEVALIDATEOK](pidtagremotevalidateok-canonical-property.md)) sur true.
    
   - Définissez la propriété **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) sur une chaîne qui indique l'état du fournisseur de transport à l'utilisateur.
    
   - Elles retournent S_OK. Toutefois, si l'opération en cours ne peut pas être annulée, **ValidateState** doit renvoyer MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un fournisseur de transport distant ne doit jamais établir une connexion à une ressource partagée (par exemple, un modem ou un port COM) en dehors du contexte de l'interaction MAPI de transport impliquée dans la méthode [IXPLogon:: FlushQueues](ixplogon-flushqueues.md) . Si **ValidateState** est appelé avec cet indicateur, votre fournisseur de transport doit effectuer les opérations suivantes: 
    
   - Définissez un indicateur d'état interne pour indiquer que la connexion à distance doit être établie lors de l'appel à la méthode **IXPLogon:: FlushQueues** . 
    
   - Définissez les valeurs correctes dans la table d'État pour que le spouleur MAPI lance le processus de vidage de la file d'attente.
    
   - Lorsque le vidage des files d'attente est terminé, libérez la ressource partagée.
    
   - Effacez le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** . 
    
   - Elles retournent S_OK.
    
FORCE_XP_DISCONNECT 
  
> Le fournisseur de transport distant doit libérer sa connexion aux ressources du système de messagerie. Une fois cette opération effectuée, il faut définir le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** et renvoyer S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit traiter les messages distants et télécharger les messages qui ont été différés. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d'état de l'objet d'ouverture de session:
    
   - Définissez la propriété **PR_STATUS_STRING** sur une chaîne qui indique l'état du fournisseur de transport à l'utilisateur. 
    
   - Définissez les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE dans la propriété **PR_STATUS_CODE** . 
    
   - Définissez la propriété **PR_REMOTE_VALIDATE_OK** dans la ligne d'État du fournisseur de transport sur false. 
    
   - Si une autre opération est en cours (par exemple, télécharger des en-têtes) lors de l'appel de **ValidateState** , **VALIDATESTATE** doit renvoyer MAPI_E_BUSY. 
    
   - Exécutez le code de traitement de l'indicateur REFRESH_XP_HEADER_CACHE afin de satisfaire aux exigences du client Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit récupérer les en-têtes de message à partir du système de messagerie. Pour ce faire, le fournisseur de transport doit procéder comme suit:
    
   - Définissez la propriété **PR_STATUS_STRING** sur une chaîne qui indique l'état du fournisseur de transport à l'utilisateur. 
    
   - Définissez les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE dans la propriété **PR_STATUS_CODE** . 
    
   - Effacez le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** . 
    
   - Définissez le bit STATUS_ONLINE dans la propriété **PR_STATUS_CODE** . 
    
   - Définissez la propriété **PR_REMOTE_VALIDATE_OK** dans la ligne d'État du fournisseur de transport sur false. 
    
SHOW_XP_SESSION_UI 
  
> Si votre fournisseur de transport possède des éléments d'interface utilisateur pour le traitement des en-têtes de message (par exemple, une boîte de dialogue confirmant le téléchargement des messages), cette boîte de dialogue doit s'afficher. Sinon, **ValidateState** peut renvoyer MAPI_E_NO_SUPPORT. 
    
Si des indicateurs autres que ceux-ci sont transmis, **ValidateState** doit renvoyer MAPI_E_UNKNOWN_FLAGS. 
  
L'appel du client au fournisseur de transport est souvent destiné à la méthode **IMAPIStatus:: ValidateState** . Pendant le traitement de **ValidateState**, le fournisseur de transport ne doit pas effectuer d'actions qui allouent de rares ressources système, telles qu'un modem ou un port com. Cela est dû au fait que le spouleur MAPI a parfois besoin de vider les files d'attente sur plusieurs fournisseurs de transport. Toutefois, le client peut appeler n'importe quelle méthode **ValidateState** du fournisseur de transport à tout moment. Si votre fournisseur de transport tente d'allouer une ressource rare pendant le traitement d' **ValidateState**, une erreur peut se produire en raison d'un conflit avec un autre fournisseur de transport que le spouleur MAPI a demandé de vider ses files d'attente. Si vous autorisez toutes les allocations de ressources rares sous la direction du spouleur MAPI, vous pouvez éviter de tels conflits. Votre fournisseur de transport doit prendre en charge la propriété **PR_REMOTE_VALIDATE_OK** afin que les applications clientes puissent détecter lorsque votre fournisseur de transport est occupé ou qu'il attend que le spouleur MAPI initie une action. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que cette méthode peut provoquer d'autres appels de longue durée, **ValidateState** peut retourner MAPI_E_BUSY pour vous informer que cette méthode attend l'achèvement d'une autre opération. Vous devez patienter jusqu'à ce que l'opération en attente soit terminée avant d'essayer une autre tâche. 
  
Vous avez le plus de contrôle sur vos appels vers les objets d'état des fournisseurs de transport. Vous pouvez transmettre un ou plusieurs indicateurs à **ValidateState** qui affectent les opérations du fournisseur de transport. Par exemple, l'indicateur ABORT_XP_HEADER_OPERATION indique que l'utilisateur a annulé la validation. Les fournisseurs de transport peuvent décider d'abandonner, retourner MAPI_E_USER_CANCELED ou continuer. 
  
Vous pouvez définir l'indicateur CONFIG_CHANGED sur un appel à l'objet Status d'un fournisseur de services ou du spouleur MAPI pour indiquer qu'une option de configuration a été modifiée. Vous pouvez utiliser CONFIG_CHANGED pour reconfigurer dynamiquement un fournisseur de transport. Lorsque vous définissez CONFIG_CHANGED sur un appel à l'objet d'état d'un fournisseur de services, le fournisseur répond avec un appel à [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) pour alerter le spouleur MAPI de la modification. Lorsque vous définissez CONFIG_CHANGED sur un appel à l'objet d'État du spouleur MAPI, le spouleur appelle [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pour chaque fournisseur de transport actif. **AddressTypes** informe le spouleur MAPI des types d'adresses prises en charge par un transport. Certains fournisseurs de services affichent également un indicateur de progression si la validation est censée prendre beaucoup de temps. L'affichage d'un indicateur de progression est utile, mais pas obligatoire. 
  
Lorsque l'indicateur SUPPRESS_UI est défini, aucune des boîtes de dialogue de configuration ou de progression ne peut être affichée. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriété canonique PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

