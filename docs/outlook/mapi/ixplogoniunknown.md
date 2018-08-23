---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ecfbf33641c86d4f162c521466ca2bf0b79a61d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581404"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit l’accès de spouleur MAPI à un fournisseur de transport. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposés par :  <br/> |Objets d’ouverture de session de transport  <br/> |
|Implémentée par :  <br/> |Fournisseurs de transport  <br/> |
|Appelée par :  <br/> |Le spouleur MAPI  <br/> |
|Identificateur de l’interface :  <br/> |IID_IXPLogon  <br/> |
|Type de pointeur :  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Renvoie les types de destinataires qui gère le fournisseur de transport.  <br/> |
|**RegisterOptions** <br/> | *Non pris en charge ou documentés.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Indique l’occurrence d’un événement demandé une notification sur lequel le fournisseur de transport.  <br/> |
|[Inactif](ixplogon-idle.md) <br/> |Indique que le système est inactif, l’activation du fournisseur de transport effectuer des opérations de priorité basse.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Lance le processus de fermeture de session.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indique qu’un message pour le fournisseur de transport fournir le spouleur MAPI.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informe le fournisseur de transport que le spouleur MAPI terminé son traitement d’un message sortant.  <br/> |
|[Sondage](ixplogon-poll.md) <br/> |Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Lance le transfert d’un message entrant à partir du fournisseur de transport pour le spouleur MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur de transport.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Vérifie l’état externe du fournisseur de transport.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Demande que le fournisseur de transport remettre immédiatement tous les messages entrants ou sortants en attente.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

