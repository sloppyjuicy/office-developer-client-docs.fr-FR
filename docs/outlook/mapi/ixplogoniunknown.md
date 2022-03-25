---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5b83df9c5ab1a7b08e34e9e09f19408b4f6fbfa3
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781312"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne aupooler MAPI l’accès à un fournisseur de transport. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets d’logo de transport  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |Lepooler MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IXPLogon  <br/> |
|Type de pointeur :  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member|Description|
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Renvoie les types de destinataires gérés par le fournisseur de transport. |
|**RegisterOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Signale l’occurrence d’un événement sur lequel le fournisseur de transport a demandé une notification. |
|[Inactif](ixplogon-idle.md) <br/> |Indique que le système est inactif, ce qui permet au fournisseur de transport d’effectuer des opérations de faible priorité. |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Lance le processus de ffage de logo. |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indique que lepooler MAPI a un message à remettre au fournisseur de transport. |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informe le fournisseur de transport que lepooler MAPI a terminé son traitement sur un message sortant. |
|[Sondage](ixplogon-poll.md) <br/> |Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants. |
|[StartMessage](ixplogon-startmessage.md) <br/> |Lance le transfert d’un message entrant du fournisseur de transport vers lepooler MAPI. |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur de transport. |
|[ValidateState](ixplogon-validatestate.md) <br/> |Vérifie l’état externe du fournisseur de transport. |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Demande au fournisseur de transport de remettre immédiatement tous les messages entrants ou sortants en attente. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

