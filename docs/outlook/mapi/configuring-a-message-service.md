---
title: Configuration d’un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564107"
---
# <a name="configuring-a-message-service"></a>Configuration d’un service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
 **Pour configurer les fournisseurs de services dans un service de message**
  
- Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si toutes les données nécessaires à la configuration est disponible par programme, vous pouvez choisir d’afficher une interface utilisateur ou non. Cependant, si des informations pour un ou plusieurs fournisseurs n’est pas disponible, assurez-vous que vous définissez l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. La suppression d’une interface utilisateur lorsque les données de configuration requises sont indisponibles résultats dans un service de message non configuré.
    
 **Pour configurer un fournisseur de services unique dans un service de message**
  
1. Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder aux objets de l’état du fournisseur de services. 
    
2. Appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services. 
    
Pour plus d’informations sur l’utilisation des objets d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).
  

