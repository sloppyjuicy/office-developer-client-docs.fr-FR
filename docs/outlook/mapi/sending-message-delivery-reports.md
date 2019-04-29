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
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433079"
---
# <a name="sending-message-delivery-reports"></a>Envoi de rapports de remise de messages

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Certains systèmes de messagerie sous-jacents prennent en charge les rapports de remise et d'autres non. La manière dont le fournisseur de transport détermine si les rapports de remise de messages ou de non-remise peuvent être envoyés aux applications clientes est un détail d'implémentation spécifique aux fournisseurs de transport individuels. Si des rapports de remise peuvent être envoyés aux applications clientes, les fournisseurs de transport utilisent la méthode [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) pour informer MAPI de la réussite ou de l'échec de la remise d'un ou de plusieurs destinataires. MAPI génère ensuite des rapports de remise ou de livraison correspondant à ces destinataires. Les fournisseurs de transport peuvent également convertir les rapports de remise et de non remise entrants natifs du système de messagerie en rapports de remise et de non remise MAPI au moyen de **StatusRecips**.
  

