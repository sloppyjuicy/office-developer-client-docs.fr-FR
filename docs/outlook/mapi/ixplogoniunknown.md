---
title: IXPLogon IUnknown
description: Décrit les propriétés et l’ordre de vtable des membres pour IXPLogon IUnknown, qui donne au spouleur MAPI l’accès à un fournisseur de transport.
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
ms.openlocfilehash: 9b737e5de8c6a25ea38cfc9013bb0be84629cd8b
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828114"
---
# <a name="ixplogon--iunknown"></a>IXPLogon : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Donne au spouleur MAPI l’accès à un fournisseur de transport. 
  
|Propriété|Valeur|
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Transporter des objets d’ouverture de session  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |Spouleur MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IXPLogon  <br/> |
|Type de pointeur :  <br/> |LXPLOGON  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member|Description|
|:-----|:-----|
|[AddressTypes](ixplogon-addresstypes.md) <br/> |Retourne les types de destinataires gérés par le fournisseur de transport. |
|**RegisterOptions** <br/> | *Non pris en charge ou documenté.*  <br/> |
|[TransportNotify](ixplogon-transportnotify.md) <br/> |Signale l’occurrence d’un événement sur lequel le fournisseur de transport a demandé une notification. |
|[Inactif](ixplogon-idle.md) <br/> |Indique que le système est inactif, ce qui permet au fournisseur de transport d’effectuer des opérations de faible priorité. |
|[TransportLogoff](ixplogon-transportlogoff.md) <br/> |Lance le processus de fermeture de session. |
|[SubmitMessage](ixplogon-submitmessage.md) <br/> |Indique que le spouleur MAPI a un message à remettre au fournisseur de transport. |
|[EndMessage](ixplogon-endmessage.md) <br/> |Informe le fournisseur de transport que le spouleur MAPI a terminé son traitement sur un message sortant. |
|[Sondage](ixplogon-poll.md) <br/> |Indique si le fournisseur de transport a reçu un ou plusieurs messages entrants. |
|[StartMessage](ixplogon-startmessage.md) <br/> |Lance le transfert d’un message entrant du fournisseur de transport vers le spouleur MAPI. |
|[OpenStatusEntry](ixplogon-openstatusentry.md) <br/> |Ouvre l’objet d’état du fournisseur de transport. |
|[ValidateState](ixplogon-validatestate.md) <br/> |Vérifie l’état externe du fournisseur de transport. |
|[FlushQueues](ixplogon-flushqueues.md) <br/> |Demande au fournisseur de transport de remettre immédiatement tous les messages entrants ou sortants en attente. |
   
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

