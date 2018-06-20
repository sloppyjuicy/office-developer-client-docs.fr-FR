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
# <a name="configuring-a-message-service"></a><span data-ttu-id="d7d4d-103">Configuration d’un Service de Message</span><span class="sxs-lookup"><span data-stu-id="d7d4d-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="d7d4d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d7d4d-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="d7d4d-105">**Pour configurer les fournisseurs de services dans un service de message**</span><span class="sxs-lookup"><span data-stu-id="d7d4d-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="d7d4d-106">Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="d7d4d-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="d7d4d-107">Si toutes les données nécessaires à la configuration est disponible par programme, vous pouvez choisir d’afficher une interface utilisateur ou non.</span><span class="sxs-lookup"><span data-stu-id="d7d4d-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="d7d4d-108">Cependant, si des informations pour un ou plusieurs fournisseurs n’est pas disponible, assurez-vous que vous définissez l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="d7d4d-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="d7d4d-109">La suppression d’une interface utilisateur lorsque les données de configuration requises sont indisponibles résultats dans un service de message non configuré.</span><span class="sxs-lookup"><span data-stu-id="d7d4d-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="d7d4d-110">**Pour configurer un fournisseur de services unique dans un service de message**</span><span class="sxs-lookup"><span data-stu-id="d7d4d-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="d7d4d-111">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder aux objets de l’état du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="d7d4d-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="d7d4d-112">Appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="d7d4d-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="d7d4d-113">Pour plus d’informations sur l’utilisation des objets d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d7d4d-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

