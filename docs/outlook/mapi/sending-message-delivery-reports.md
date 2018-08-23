---
title: Envoi de rapports de remise de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 717494f30fd4d43e94a7c6a37770e2eab8ebb59e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593598"
---
# <a name="sending-message-delivery-reports"></a>Envoi de rapports de remise de messages

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie sous-jacent prend en charge les rapports de remise et d’autres pas. Comment le fournisseur de transport détermine si les rapports de remise ou de non-remise du message peuvent être envoyés vers des applications clientes est un détail d’implémentation spécifique à un fournisseur de transport individuels. Si les rapports de remise peuvent être envoyés vers les applications clientes, fournisseurs de transport utilisent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour notifier MAPI de remise réussi ou échoué pour un ou plusieurs destinataires. MAPI puis génère des rapports de remise ou de non-remise correspondant à des destinataires. Fournisseurs de transport peuvent également traduire les rapports de remise et de non-remise entrants natifs au système de messagerie dans remise MAPI et les rapports de non-remise prenait **StatusRecips**.
  

