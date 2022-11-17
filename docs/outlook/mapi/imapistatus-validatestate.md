---
title: IMAPIStatusValidateState
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIStatus.ValidateState
api_type:
- COM
ms.assetid: 036b9b15-86e1-4a37-8e4b-e37b2963d8fb
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 58a30090c772150f3376ddd8b636de26f548b9e8
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62463162"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Confirme les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services. Cette méthode est prise en charge dans tous les objets d’état. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode.
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la validation. Les indicateurs suivants peuvent être définies :
    
ABORT_XP_HEADER_OPERATION
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** la boîte de dialogue correspondante. L’objet d’état dispose de deux options : 
    
   - Continuez à travailler sur l’opération.
    
   - Arrêtez l’opération et renvoyez MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Une ou plusieurs propriétés de configuration de l’objet d’état ont été modifiées. Les clients peuvent définir cet indicateur pour permettre aupooler MAPI de corriger dynamiquement les défaillances critiques du fournisseur de transport. 
    
FORCE_XP_CONNECT 
  
> L’objet d’état doit effectuer une connexion. Lorsque cet indicateur est utilisé avec l’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la connexion se produit sans mise en cache.
    
FORCE_XP_DISCONNECT 
  
> L’objet d’état doit effectuer une opération de déconnexion. Lorsque cet indicateur est utilisé avec l’REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la déconnexion se produit sans mise en cache.
    
PROCESS_XP_HEADER_CACHE 
  
> Les entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés. Les messages qui ont des MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE doivent être déplacés.
    
REFRESH_XP_HEADER_CACHE 
  
> Pour un fournisseur de transport distant, une nouvelle liste d’en-têtes de message doit être téléchargée et tous les indicateurs qui marquent l’état du message doivent être effacés.
    
SUPPRESS_UI 
  
> Empêche l’objet d’état d’afficher une interface utilisateur dans le cadre de l’opération.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> La validation a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé à se terminer ou arrêté avant le début de cette opération.
    
MAPI_E_NO_SUPPORT 
  
> L’objet status ne prend pas en charge la méthode de validation, comme indiqué par l’absence de l’indicateur STATUS_VALIDATE_STATE dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de validation, généralement en cliquant sur le **bouton Annuler dans** une boîte de dialogue. Cette valeur est renvoyée uniquement par les fournisseurs de transport distants. 
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIStatus::ValidateState** vérifie l’état d’une ressource associée à un objet d’état. **ValidateState** est la seule méthode de l’interface [IMAPIStatus](imapistatusimapiprop.md) requise pour tous les objets d’état. Le comportement exact de cette méthode dépend de l’implémentation. Le tableau suivant décrit l’implémentation de chacun des différents types d’objets d’état. 
  
|**Objet Status**|Implémentation ValidateState****|
|:-----|:-----|
|Sous-système MAPI  <br/> |Valide l’état de toutes les ressources que les fournisseurs de services actifs et le sous-système lui-même possèdent.  <br/> |
|Pooler MAPI  <br/> |Effectue une session de tous les fournisseurs de transport, qu’ils soient déjà connectés ou non.  <br/> |
|Carnet d’adresses MAPI  <br/> |Vérifie les entrées dans sa section de profil.  <br/> |
|Fournisseur de services  <br/> |L’implémentation dépend du type de fournisseur et des indicateurs définies dans _le paramètre ulFlags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les applications clientes distantes **appellent la méthode ValidateState** pour démarrer le traitement à distance pour diverses actions. Cette méthode permet principalement de définir des bits d’état pour communiquer avec lepooler MAPI, au lieu de faire n’importe quel travail. En règle générale, le fournisseur de transport définit des indicateurs dans sa ligne d’état qui indiquent aupooler MAPI quelles actions doivent être lancées pour terminer la demande du client. 

Dans ce modèle d’interaction client-transport-spooler, les actions demandées par le client sont asynchrones, dans ce cas **ValidateState** renvoie avant que les actions demandées soient terminées. Toutefois, les actions qui n’impliquent pas nécessairement le système de messagerie sous-jacent ou qui impliquent une interface spécifique au transport peuvent être synchrones. L’application cliente passe un masque de bits des indicateurs suivants pour spécifier les actions que le fournisseur de transport distant doit prendre. 
  
ABORT_XP_HEADER_OPERATION 
  
> Si possible, le fournisseur de transport distant doit annuler toutes les opérations qui impliquent le téléchargement d’en-têtes. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’logo :
    
   - Clear the STATUS_INBOUND_ENABLED and STATUS_INBOUND_ACTIVE bits in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property to tell the MAPI spooler to stop the incoming flush process for this transport provider.
    
   - Définissez le STATUS_OFFLINE bit dans la **PR_STATUS_CODE** propriété. 
    
   - Définissez **la PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) sur TRUE.
    
   - Définissez **PR_STATUS_STRING** propriété ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur.
    
   - Elles retournent S_OK. Toutefois, si l’opération en cours ne peut pas être annulée, **ValidateState** doit MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un fournisseur de transport distant ne doit jamais établir de connexion à une ressource partagée (par exemple, un modem ou un port COM) en dehors du contexte de l’interaction de transport depooler MAPI impliquée dans la méthode [IXPLogon::FlushQueues](ixplogon-flushqueues.md) . Si **ValidateState** est appelé avec cet indicateur, votre fournisseur de transport doit : 
    
   - Définissez un indicateur d’état interne pour indiquer que la connexion distante doit être établie lorsque la méthode **IXPLogon::FlushQueues** est appelée. 
    
   - Définissez les valeurs correctes dans la table d’état pour que lepooler MAPI lance le processus de  purge de la file d’attente.
    
   - Lorsque le  purgement des files d’attente est terminé, relâchez la ressource partagée.
    
   - Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property. 
    
   - Elles retournent S_OK.
    
FORCE_XP_DISCONNECT 
  
> Le fournisseur de transport distant doit libérer sa connexion aux ressources système de messagerie. Après cela, il doit définir le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** et renvoyer S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit traiter les messages distants et télécharger tous les messages différés. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’logo :
    
   - Définissez **la PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur. 
    
   - Définissez les STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE bits dans la **PR_STATUS_CODE** de la propriété. 
    
   - Définissez **la PR_REMOTE_VALIDATE_OK** de transport dans la ligne d’état du fournisseur de transport sur FALSE. 
    
   - Si une autre opération est en cours (par exemple, le téléchargement des en-têtes) lorsque **ValidateState** est appelé, **ValidateState** doit MAPI_E_BUSY. 
    
   - Exécutez le code pour traiter l’indicateur REFRESH_XP_HEADER_CACHE, afin de satisfaire les exigences du client Microsoft Exchange client.
    
REFRESH_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit récupérer les nouveaux en-têtes de message à partir du système de messagerie. Pour ce faire, le fournisseur de transport doit :
    
   - Définissez **la PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur. 
    
   - Définissez les STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE bits dans la **PR_STATUS_CODE** propriété. 
    
   - Clear the STATUS_OFFLINE bit in the **PR_STATUS_CODE** property. 
    
   - Définissez le STATUS_ONLINE bit dans la **PR_STATUS_CODE** propriété. 
    
   - Définissez **la PR_REMOTE_VALIDATE_OK** de transport dans la ligne d’état du fournisseur de transport sur FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Si votre fournisseur de transport dispose d’éléments d’interface utilisateur pour le traitement des en-têtes de message (par exemple, une boîte de dialogue confirmant le téléchargement des messages), cette boîte de dialogue doit s’afficher. Dans le cas **contraire, ValidateState** peut renvoyer MAPI_E_NO_SUPPORT. 
    
Si des indicateurs autres que ceux-ci sont passés, **ValidateState** doit MAPI_E_UNKNOWN_FLAGS. 
  
L’appel du client au fournisseur de transport est souvent à la méthode **IMAPIStatus::ValidateState** . Pendant le traitement de **ValidateState**, le fournisseur de transport ne doit effectuer aucune action qui alloue des ressources système allouées, telles qu’un modem ou un port COM. Cela est dû au fait que lepooler MAPI devra parfois vider les files d’attente sur plusieurs fournisseurs de transport. Toutefois, le client peut appeler la méthode **ValidateState** de n’importe quel fournisseur de transport à tout moment. Si votre fournisseur de transport tente d’allouer une ressource importante pendant le traitement de **ValidateState**, une erreur peut se produite en raison d’un conflit avec un autre fournisseur de transport que lepooler MAPI a demandé de vider ses files d’attente. Si vous autorisez toutes les allocations de ressources sous la direction dupooler MAPI, vous pouvez éviter de tels conflits. Votre fournisseur de transport doit prendre en **charge la propriété PR_REMOTE_VALIDATE_OK** afin que les applications clientes détectent quand votre fournisseur de transport est occupé ou en attente que lepooler MAPI lance une action. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Étant donné que cette méthode peut entraîner d’autres appels potentiellement longs, **ValidateState** peut renvoyer MAPI_E_BUSY pour vous informer que cette méthode attend la fin d’une autre opération. Vous devez attendre la fin de l’opération en attente avant d’essayer une autre tâche. 
  
Vous contrôlez le mieux vos appels aux objets d’état du fournisseur de transport. Vous pouvez transmettre un ou plusieurs indicateurs **à ValidateState** qui affectent les opérations du fournisseur de transport. Par exemple, l’ABORT_XP_HEADER_OPERATION indique que l’utilisateur a annulé la validation. Les fournisseurs de transport peuvent décider d’abandonner, de MAPI_E_USER_CANCELED ou de continuer. 
  
Vous pouvez définir l’indicateur CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de services ou aupooler MAPI pour indiquer qu’une option de configuration a été modifiée. Vous pouvez utiliser CONFIG_CHANGED pour reconfigurer dynamiquement un fournisseur de transport. Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de services, le fournisseur répond par un appel à [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) pour alerter lepooler MAPI de la modification. Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état dupooler MAPI, lepooler appelle [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour chaque fournisseur de transport actif. **AddressTypes informe** lepooler MAPI des types d’adresses pris en charge par un transport. Certains fournisseurs de services affichent également un indicateur de progression si la validation est prévue pour prendre beaucoup de temps. L’affichage d’un indicateur de progression est utile, mais pas obligatoire. 
  
Lorsque l’SUPPRESS_UI est définie, aucune des feuilles de propriétés de configuration ou des boîtes de dialogue de progression ne peut être affichée. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriété canonique PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

