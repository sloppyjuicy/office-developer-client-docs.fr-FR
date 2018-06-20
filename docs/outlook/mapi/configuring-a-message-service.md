---
title: Configuration d’un Service de Message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: fd87d169cd5131c6e1c8ca45a35dded96a295c57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783041"
---
# <a name="configuring-a-message-service"></a>Configuration d’un Service de Message

  
  
**S’applique à**: Outlook 
  
 **Pour configurer les fournisseurs de services dans un service de message**
  
- Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si toutes les données nécessaires à la configuration est disponible par programme, vous pouvez choisir d’afficher une interface utilisateur ou non. Cependant, si des informations pour un ou plusieurs fournisseurs n’est pas disponible, assurez-vous que vous définissez l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. La suppression d’une interface utilisateur lorsque les données de configuration requises sont indisponibles résultats dans un service de message non configuré.
    
 **Pour configurer un fournisseur de services unique dans un service de message**
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder aux objets de l’état du fournisseur de services. 
    
2. Appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services. 
    
Pour plus d’informations sur l’utilisation des objets d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).
  

