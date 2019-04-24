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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282795"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Autorise l'accès au spouleur MAPI à un fournisseur de transport. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi. h  <br/> |
|Exposé par:  <br/> |Objets de connexion de transport  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |Spouleur MAPI  <br/> |
|Identificateur de l'interface:  <br/> |IID_IXPLogon  <br/> |
|Type de pointeur:  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Renvoie les types de destinataire gérés par le fournisseur de transport.  <br/> |
|**RegisterOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Signale l'occurrence d'un événement sur lequel le fournisseur de transport a demandé une notification.  <br/> |
|[Engrenage](ixplogon-idle.md) <br/> |Indique que le système est inactif, ce qui permet au fournisseur de transport d'effectuer des opérations de faible priorité.  <br/> |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Lance le processus de fermeture de session.  <br/> |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indique que le spouleur MAPI a un message pour le fournisseur de transport à livrer.  <br/> |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informe le fournisseur de transport que le spouleur MAPI a terminé son traitement sur un message sortant.  <br/> |
|[Temporisateur](ixplogon-poll.md) <br/> |Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants.  <br/> |
|[StartMessage](ixplogon-startmessage.md) <br/> |Lance le transfert d'un message entrant depuis le fournisseur de transport vers le spouleur MAPI.  <br/> |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Ouvre l'objet d'État du fournisseur de transport.  <br/> |
|[ValidateState](ixplogon-validatestate.md) <br/> |Vérifie l'état externe du fournisseur de transport.  <br/> |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Demande que le fournisseur de transport remet immédiatement tous les messages entrants ou sortants en attente.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

