---
title: Reconfiguration d’un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408409"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="2793f-103">Reconfiguration d’un fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="2793f-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="2793f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2793f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2793f-105">Vous pouvez utiliser l’objet d’état d’un fournisseur de transport pour modifier certaines propriétés du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="2793f-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="2793f-106">La plage de propriétés qui peut être modifiée dépend des propriétés incluses dans la feuille des propriétés du fournisseur et de la façon dont ces propriétés sont définies.</span><span class="sxs-lookup"><span data-stu-id="2793f-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="2793f-107">**Pour reconfigurer un fournisseur de transport actif**</span><span class="sxs-lookup"><span data-stu-id="2793f-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="2793f-108">Appelez [IMAPISession::GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d’état.</span><span class="sxs-lookup"><span data-stu-id="2793f-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="2793f-109">Recherchez la ligne du fournisseur de transport à reconfigurer en créant une restriction de propriété qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du fournisseur cible.</span><span class="sxs-lookup"><span data-stu-id="2793f-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="2793f-110">Appelez [IMAPITable::FindRow](imapitable-findrow.md) pour récupérer la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="2793f-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="2793f-111">Vérifiez que les indicateurs STATUS_SETTINGS_DIALOG et STATUS_VALIDATE_STATE sont définies dans la propriété PR_RESOURCE_METHODS ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) du fournisseur de **transport** cible.</span><span class="sxs-lookup"><span data-stu-id="2793f-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="2793f-112">Si STATUS_SETTINGS_DIALOG n’est pas définie, le fournisseur de transport n’affiche pas de feuille des propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="2793f-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="2793f-113">Si STATUS_VALIDATE_STATE n’est pas définie, vous ne pouvez pas effectuer de reconfiguration dynamique.</span><span class="sxs-lookup"><span data-stu-id="2793f-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="2793f-114">Si STATUS_SETTINGS_DIALOG est définie, appelez [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille des propriétés du fournisseur de transport et permettre à l’utilisateur d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="2793f-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="2793f-115">Une fois que l’utilisateur a terminé la reconfiguration, appelez [IMAPIStatus::ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE est définie, en passant CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="2793f-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

