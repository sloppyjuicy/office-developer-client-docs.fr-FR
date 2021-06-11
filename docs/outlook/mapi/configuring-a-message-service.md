---
title: Configuration d’un service de message
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
# <a name="configuring-a-message-service"></a><span data-ttu-id="96506-103">Configuration d’un service de message</span><span class="sxs-lookup"><span data-stu-id="96506-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="96506-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="96506-105">**Pour configurer tous les fournisseurs de services dans un service de messagerie**</span><span class="sxs-lookup"><span data-stu-id="96506-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="96506-106">Appelez [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="96506-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="96506-107">Si toutes les données nécessaires à la configuration sont disponibles par programme, vous pouvez choisir d’afficher ou non une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="96506-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="96506-108">Toutefois, si certaines informations d’un ou plusieurs fournisseurs ne sont pas disponibles, veillez à définir l’indicateur SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS’indicateur.</span><span class="sxs-lookup"><span data-stu-id="96506-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="96506-109">La suppression d’une interface utilisateur lorsque les données de configuration requises ne sont pas disponibles entraîne un service de message non configuré.</span><span class="sxs-lookup"><span data-stu-id="96506-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="96506-110">**Pour configurer un fournisseur de services unique dans un service de messagerie**</span><span class="sxs-lookup"><span data-stu-id="96506-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="96506-111">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à l’objet d’état du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="96506-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="96506-112">Appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="96506-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="96506-113">Pour plus d’informations sur l’utilisation des objets d’état, voir [Tableau d’état et Objets d’état.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="96506-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

