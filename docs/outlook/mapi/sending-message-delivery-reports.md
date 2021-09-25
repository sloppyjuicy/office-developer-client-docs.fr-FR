---
title: Envoi de rapports de remise de messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ef949db447aee54f0e007e1ddbbf104ea2451ef5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609438"
---
# <a name="sending-message-delivery-reports"></a>Envoi de rapports de remise de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie sous-jacents sont en charge des rapports de remise et d’autres non. La façon dont le fournisseur de transport détermine si des rapports de remise de messages ou de non remise peuvent être envoyés à des applications clientes est un détail d’implémentation propre à des fournisseurs de transport individuels. Si des rapports de remise peuvent être envoyés à des applications clientes, les fournisseurs de transport utilisent la méthode [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) pour informer MAPI de la réussite ou de l’échec de la remise pour un ou plusieurs destinataires. MAPI génère ensuite des rapports de remise ou de non remise correspondant à ces destinataires. Les fournisseurs de transport peuvent également traduire les rapports de remise et de remise entrants natifs du système de messagerie en rapports de remise et de non remise MAPI au moyen de **StatusRecips**.
  

