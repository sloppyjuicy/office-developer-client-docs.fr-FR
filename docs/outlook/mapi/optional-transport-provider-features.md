---
title: Fonctionnalités facultatives du fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 0bec2c17-b41c-4e46-8961-a55bde1f7326
ms.openlocfilehash: 2eaf41dee90ea72fabecd139f435f3aba98c9950
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63371085"
---
# <a name="optional-transport-provider-features"></a>Fonctionnalités facultatives du fournisseur de transport

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fonctionnalités facultatives que les fournisseurs de transport peuvent implémenter sont les suivantes :
  
- Inscription des options de message et de destinataire spécifiques au fournisseur de transport.
    
- Maintenance d’un profil, si nécessaire, pour stocker les informations de configuration et les informations d’identification dans le système de messagerie.
    
- Effectuer toute vérification des informations d’identification requises par le système de messagerie.
    
- Prise en charge de la notification d’événement pour les applications clientes intéressées avec la méthode [IMAPISupport::Notify](imapisupport-notify.md) . 
    
- Affichage des feuilles de propriétés de configuration et des boîtes de dialogue de l’Assistant pour permettre aux utilisateurs de configurer les paramètres du fournisseur de transport.
    
- Fourniture de rapports de remise de messages aux applications clientes.
    

