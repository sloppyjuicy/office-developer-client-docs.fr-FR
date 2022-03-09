---
title: Configuration d’un service de message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
ms.openlocfilehash: 0ee2dd3f0920f5ee7e85b83341d35529b15c2143
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63382418"
---
# <a name="configuring-a-message-service"></a>Configuration d’un service de message

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour configurer tous les fournisseurs de services dans un service de messagerie**
  
- [Appelez IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si toutes les données nécessaires à la configuration sont disponibles par programme, vous pouvez choisir d’afficher ou non une interface utilisateur. Toutefois, si certaines informations d’un ou plusieurs fournisseurs ne sont pas disponibles, veillez à définir l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS fournisseur. La suppression d’une interface utilisateur lorsque les données de configuration requises ne sont pas disponibles entraîne un service de message non configuré.
    
 **Pour configurer un fournisseur de services unique dans un service de messagerie**
  
1. [Appelez IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à l’objet d’état du fournisseur de services. 
    
2. [Appelez IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services. 
    
Pour plus d’informations sur l’utilisation des objets d’état, voir [Tableau d’état et Objets d’état](status-table-and-status-objects.md).
  

