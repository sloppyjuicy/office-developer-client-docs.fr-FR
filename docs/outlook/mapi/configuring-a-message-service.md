---
title: Configuration d'un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434507"
---
# <a name="configuring-a-message-service"></a>Configuration d'un service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
 **Pour configurer tous les fournisseurs de services dans un service de messagerie**
  
- Appelez [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Si toutes les données nécessaires pour la configuration sont disponibles par programme, vous pouvez choisir d'afficher ou non une interface utilisateur. Toutefois, si certaines informations pour un ou plusieurs fournisseurs ne sont pas disponibles, veillez à définir l'indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS. Suppression d'une interface utilisateur lorsque les données de configuration requises ne sont pas disponibles, les résultats sont indisponibles dans un service de messagerie non configuré.
    
 **Pour configurer un fournisseur de services unique dans un service de messagerie**
  
1. Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à l'objet d'État du fournisseur de services. 
    
2. Appelez [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services. 
    
Pour plus d'informations sur l'utilisation des objets d'État, voir [table d'État et objets d'État](status-table-and-status-objects.md).
  

