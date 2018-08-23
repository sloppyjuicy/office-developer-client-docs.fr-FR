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
# <a name="configuring-a-message-service"></a><span data-ttu-id="34771-103">Configuration d’un service de messagerie</span><span class="sxs-lookup"><span data-stu-id="34771-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="34771-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34771-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="34771-105">**Pour configurer les fournisseurs de services dans un service de message**</span><span class="sxs-lookup"><span data-stu-id="34771-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="34771-106">Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="34771-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="34771-107">Si toutes les données nécessaires à la configuration est disponible par programme, vous pouvez choisir d’afficher une interface utilisateur ou non.</span><span class="sxs-lookup"><span data-stu-id="34771-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="34771-108">Cependant, si des informations pour un ou plusieurs fournisseurs n’est pas disponible, assurez-vous que vous définissez l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="34771-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="34771-109">La suppression d’une interface utilisateur lorsque les données de configuration requises sont indisponibles résultats dans un service de message non configuré.</span><span class="sxs-lookup"><span data-stu-id="34771-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="34771-110">**Pour configurer un fournisseur de services unique dans un service de message**</span><span class="sxs-lookup"><span data-stu-id="34771-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="34771-111">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder aux objets de l’état du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="34771-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="34771-112">Appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="34771-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="34771-113">Pour plus d’informations sur l’utilisation des objets d’état, voir la [Table d’état et les objets d’état](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="34771-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

