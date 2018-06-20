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
ms.openlocfilehash: 3ff29ac7e7f9b7876bb678930390ca556351ecf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783987"
---
# <a name="imapistatusvalidatestate"></a>IMAPIStatus::ValidateState

**S’applique à**: Outlook 
  
Vérifie les informations d’état externe disponibles pour la ressource MAPI ou le fournisseur de services. Cette méthode est prise en charge dans tous les objets d’état. 
  
```cpp
HRESULT ValidateState(
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

_ulUIParam_
  
> [in] Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows qui affiche cette méthode.
    
_ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la validation. Les indicateurs suivants peuvent être définis :
    
ABORT_XP_HEADER_OPERATION
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans la boîte de dialogue correspondante. L’objet état comprend deux options : 
    
   - Continuer à travailler sur l’opération.
    
   - Arrêter l’opération et revenir MAPI_E_USER_CANCELED.
    
CONFIG_CHANGED 
  
> Un ou plusieurs des propriétés de configuration de l’objet état modifié. Les clients peuvent définir cet indicateur pour autoriser le spouleur MAPI dynamiquement corriger les échecs de fournisseur de transport critique. 
    
FORCE_XP_CONNECT 
  
> L’objet état doit effectuer une connexion. Lorsque cet indicateur est utilisé avec l’indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la connexion se produit sans mise en cache.
    
FORCE_XP_DISCONNECT 
  
> L’objet état doit effectuer une opération de déconnexion. Lorsque cet indicateur est utilisé avec l’indicateur REFRESH_XP_HEADER_CACHE ou PROCESS_XP_HEADER_CACHE, la déconnexion se produit sans mise en cache.
    
PROCESS_XP_HEADER_CACHE 
  
> Entrées de la table de cache d’en-tête doivent être traitées, tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DOWNLOAD doivent être téléchargés et tous les messages marqués avec l’indicateur MSGSTATUS_REMOTE_DELETE doivent être supprimés. Messages MSGSTATUS_REMOTE_DOWNLOAD et MSGSTATUS_REMOTE_DELETE la valeur doivent être déplacés.
    
REFRESH_XP_HEADER_CACHE 
  
> Pour un fournisseur de transport à distance, une nouvelle liste d’en-têtes de message doit être téléchargée et tous les indicateurs qui marquant le statut du message doivent être effacés.
    
SUPPRESS_UI 
  
> L’objet état empêche l’affichage d’une interface utilisateur dans le cadre de l’opération.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> La validation a réussi.
    
MAPI_E_BUSY 
  
> Une autre opération est en cours ; Il doit être autorisé pour effectuer, ou il doit être arrêté, avant cette opération est lancée.
    
MAPI_E_NO_SUPPORT 
  
> L’objet état ne gère pas la méthode de validation, comme indiqué par l’absence de l’indicateur STATUS_VALIDATE_STATE dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)).
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de validation de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. Cette valeur est renvoyée uniquement par les fournisseurs de transport à distance. 
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIStatus::ValidateState** vérifie l’état d’une ressource qui est associée à un objet d’état. **ValidateState** est la seule méthode dans l’interface [IMAPIStatus](imapistatusimapiprop.md) qui est requis pour tous les objets d’état. Le comportement exact de cette méthode dépend de l’implémentation. Le tableau suivant décrit l’implémentation de chacune des différents types d’objets d’état. 
  
|**Objet d’état**|ValidateState ** implémentation **|
|:-----|:-----|
|Sous-système MAPI  <br/> |Vérifie l’état de toutes les ressources qui possèdent les fournisseurs de services active et le sous-système de lui-même.  <br/> |
|Spouleur MAPI  <br/> |Effectue une ouverture de session de tous les fournisseurs de transport, quel que soit le si elles sont déjà connectés.  <br/> |
|Carnet d’adresses MAPI  <br/> |Vérifie les entrées dans la section de profil.  <br/> |
|Fournisseur de services  <br/> |Implémentation dépend du type de fournisseur et les indicateurs définis dans le paramètre _ulFlags_ .  <br/> |
   
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Applications clientes à distance appellent la méthode de **ValidateState** de démarrage à distance pour différentes actions de traitement. Cette méthode existe principalement pour définir des bits d’état pour communiquer avec le spouleur MAPI, au lieu de faire tout travail. En règle générale, le fournisseur de transport définit les indicateurs dans sa ligne d’état qui indiquent au spouleur MAPI qu’actions doivent être lancées pour terminer la demande du client. 

Dans ce modèle d’interaction de transport-client-spouleur, les actions demandées par le client sont asynchrones, **ValidateState** renvoie avant les actions demandées sont terminées. Toutefois, les actions qui n’impliquent pas nécessairement le système de messagerie sous-jacent ou qui mettent en œuvre une interface de transport spécifique, peuvent être synchrones. L’application cliente transmet un masque de bits des indicateurs suivants pour spécifier les actions que le fournisseur de transport distant doit exécuter. 
  
ABORT_XP_HEADER_OPERATION 
  
> Dans la mesure du possible, le fournisseur de transport distant doit annuler toutes les opérations qui impliquent le téléchargement des en-têtes. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’ouverture de session :
    
   - Effacer les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE dans la propriété **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) pour indiquer le spouleur MAPI pour arrêter le processus de vidage entrant pour ce fournisseur de transport.
    
   - Définir le bit dans la propriété **PR_STATUS_CODE** de STATUS_OFFLINE. 
    
   - La propriété **PR_REMOTE_VALIDATE_OK** ([PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)) la valeur TRUE.
    
   - Définissez la propriété **PR_STATUS_STRING** ([PidTagStatusString](pidtagstatusstring-canonical-property.md)) sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur.
    
   - Elles retournent S_OK. Toutefois, si l’opération en cours ne peut pas être annulée, **ValidateState** doit renvoyer MAPI_E_BUSY. 
    
FORCE_XP_CONNECT 
  
> Un fournisseur de transport à distance ne doit jamais établir une connexion à une ressource partagée (par exemple, un modem ou le port COM) en dehors du contexte de l’interaction de transport-spouleur MAPI impliquée dans la méthode [IXPLogon::FlushQueues](ixplogon-flushqueues.md) . Si **ValidateState** est appelé avec cet indicateur, votre fournisseur de transport doit procédez comme suit : 
    
   - Définir un indicateur d’état interne pour indiquer que la connexion à distance doit être établie lorsque la méthode **IXPLogon::FlushQueues** est appelée. 
    
   - Définir les valeurs appropriées dans la table d’état pour le spouleur MAPI lancer la file d’attente de vidage du processus.
    
   - Lors de la purge des files d’attente est terminée, version de la ressource partagée.
    
   - Désactivez le STATUS_OFFLINE bit dans la propriété **PR_STATUS_CODE** . 
    
   - Elles retournent S_OK.
    
FORCE_XP_DISCONNECT 
  
> Le fournisseur de transport distant doit libérer sa connexion avec les ressources du système de messagerie. Après cela, il doit définir le bit STATUS_OFFLINE dans la propriété **PR_STATUS_CODE** et qu’elles retournent S_OK. 
    
PROCESS_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit traiter les messages à distance et téléchargez tous les messages qui ont été différés. Pour ce faire, le fournisseur de transport doit définir les valeurs de propriété suivantes dans la ligne d’état de l’objet d’ouverture de session :
    
   - Définissez la propriété **PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur. 
    
   - Définir les bits STATUS_OUTBOUND_ENABLED et STATUS_OUTBOUND_ACTIVE dans la propriété **PR_STATUS_CODE** . 
    
   - Définir la propriété **PR_REMOTE_VALIDATE_OK** dans la ligne d’état du fournisseur de transport sur FALSE. 
    
   - Si une autre opération est en cours (telles que le téléchargement des en-têtes) lorsque **ValidateState** est appelé, **ValidateState** doit retourner MAPI_E_BUSY. 
    
   - Exécuter le code pour le traitement de l’indicateur REFRESH_XP_HEADER_CACHE, ainsi que pour satisfaire aux exigences du client Microsoft Exchange.
    
REFRESH_XP_HEADER_CACHE 
  
> Le fournisseur de transport distant doit récupérer les en-têtes des nouveaux messages du système de messagerie. Pour ce faire, le fournisseur de transport procédez comme suit :
    
   - Définissez la propriété **PR_STATUS_STRING** sur une chaîne qui indique l’état du fournisseur de transport à l’utilisateur. 
    
   - Définir les bits STATUS_INBOUND_ENABLED et STATUS_INBOUND_ACTIVE dans la propriété **PR_STATUS_CODE** . 
    
   - Désactivez le STATUS_OFFLINE bit dans la propriété **PR_STATUS_CODE** . 
    
   - Définir le bit dans la propriété **PR_STATUS_CODE** de STATUS_ONLINE. 
    
   - Définir la propriété **PR_REMOTE_VALIDATE_OK** dans la ligne d’état du fournisseur de transport sur FALSE. 
    
SHOW_XP_SESSION_UI 
  
> Si votre fournisseur de transport comprend les éléments de l’interface utilisateur pour traiter les en-têtes des messages (par exemple une boîte de dialogue qui confirme le téléchargement des messages), cette boîte de dialogue doit être affichée. Dans le cas contraire, **ValidateState** peut renvoyer MAPI_E_NO_SUPPORT. 
    
Si tous les indicateurs de ces passés, **ValidateState** doit renvoyer MAPI_E_UNKNOWN_FLAGS. 
  
L’appel du client pour le fournisseur de transport sera souvent à la méthode **IMAPIStatus::ValidateState** . Lors du traitement de **ValidateState**, le fournisseur de transport ne doit pas effectuer toutes les actions qui affectent des ressources système limitées, tel qu’un modem ou d’un port COM. Il s’agit, car le spouleur MAPI vous devrez parfois vider les files d’attente sur plusieurs fournisseurs de transport. Toutefois, le client peut appeler la méthode **ValidateState** de tout fournisseur transport à tout moment. Si votre fournisseur de transport tente d’allouer une ressource rare lors du traitement de **ValidateState**, une erreur risque en raison de conflits avec un autre fournisseur de transport que le spouleur MAPI a demandé à purger ses files d’attente. Si vous autorisez toutes les affectations de ressources limitées se produise sous la direction du spouleur MAPI, vous pouvez éviter ces conflits. Votre fournisseur de transport doit prendre en charge la propriété **PR_REMOTE_VALIDATE_OK** pour les applications clientes détecte lorsque votre fournisseur de transport est occupé (e) ou en attente pour le spouleur MAPI déclencher une action. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Étant donné que cette méthode peut entraîner des autres appels potentiellement longues, **ValidateState** peut renvoyer MAPI_E_BUSY pour vous informer que cette méthode attend la fin d’une autre opération. Vous devez attendre jusqu'à ce que l’opération en attente est terminée avant d’essayer une autre tâche. 
  
Vous avez meilleur contrôle sur vos appels aux objets état du fournisseur de transport. Vous pouvez passer un ou plusieurs indicateurs à **ValidateState** qui affectent les opérations du fournisseur de transport. Par exemple, l’indicateur ABORT_XP_HEADER_OPERATION indique que l’utilisateur a annulé la validation. Fournisseurs de transport peuvent décider d’abandon renvoi MAPI_E_USER_CANCELED, ou peuvent continuer. 
  
Vous pouvez définir l’indicateur CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de service ou le spouleur MAPI pour indiquer qu’une option de configuration a été modifiée. Vous pouvez utiliser CONFIG_CHANGED pour reconfigurer dynamiquement un fournisseur de transport. Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état d’un fournisseur de service, le fournisseur répond à un appel à [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) pour le spouleur MAPI de la modification d’alerte. Lorsque vous définissez CONFIG_CHANGED sur un appel à l’objet d’état du spouleur MAPI, le spouleur appelle [IXPLogon::AddressTypes](ixplogon-addresstypes.md) pour chaque fournisseur de transport actif. **AddressTypes** informe le spouleur MAPI prises en charge d’un transport types d’adresse. Certains fournisseurs de services affichent également un indicateur de progression si la validation doit prendre beaucoup de temps. Affichage d’un indicateur de progression est utile, mais pas obligatoire. 
  
Lorsque l’indicateur SUPPRESS_UI est défini, aucune des feuilles de propriétés de configuration ou des boîtes de dialogue de progression peuvent être affichées. 
  
## <a name="see-also"></a>Voir aussi

- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)
- [IXPLogon::FlushQueues](ixplogon-flushqueues.md)
- [Propriété canonique PidTagRemoteValidateOk](pidtagremotevalidateok-canonical-property.md)
- [Propriété canonique PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
- [Propriété canonique PidTagStatusCode](pidtagstatuscode-canonical-property.md)
- [Propriété canonique PidTagStatusString](pidtagstatusstring-canonical-property.md)
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

