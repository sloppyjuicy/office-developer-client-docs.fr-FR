---
title: Reconfiguration d'un fournisseur de transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d466bde-b70d-44b6-ba03-6ad8353ec759
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: b35ca2bb52439cf2ba1750c6fad2883730c4c3f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328412"
---
# <a name="reconfiguring-a-transport-provider"></a><span data-ttu-id="4ef8b-103">Reconfiguration d'un fournisseur de transport</span><span class="sxs-lookup"><span data-stu-id="4ef8b-103">Reconfiguring a Transport Provider</span></span>

  
  
<span data-ttu-id="4ef8b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4ef8b-105">Vous pouvez utiliser l'objet d'état d'un fournisseur de transport pour modifier certaines des propriétés du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-105">You can use a transport provider's status object to change some of the properties of the provider.</span></span> <span data-ttu-id="4ef8b-106">La plage de propriétés qui peut être modifiée dépend des propriétés incluses dans la feuille des propriétés du fournisseur et de la façon dont ces propriétés sont définies.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-106">The range of properties that can be changed depends on the properties that are included with the provider's property sheet and how those properties are defined.</span></span> 
  
 <span data-ttu-id="4ef8b-107">**Pour reconfigurer un fournisseur de transport actif**</span><span class="sxs-lookup"><span data-stu-id="4ef8b-107">**To reconfigure an active transport provider**</span></span>
  
1. <span data-ttu-id="4ef8b-108">Appelez [IMAPISession:: GetStatusTable](imapisession-getstatustable.md) pour accéder à la table d'État.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-108">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="4ef8b-109">Localisez la ligne du fournisseur de transport qui doit être reconfigurée en créant une restriction de propriété qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) avec le nom du fournisseur cible.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-109">Locate the row for the transport provider to be reconfigured by creating a property restriction that matches **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) with the name of the target provider.</span></span> 
    
3. <span data-ttu-id="4ef8b-110">Appelez [IMAPITable:: FindRow](imapitable-findrow.md) pour récupérer la ligne appropriée.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-110">Call [IMAPITable::FindRow](imapitable-findrow.md) to retrieve the appropriate row.</span></span> 
    
4. <span data-ttu-id="4ef8b-111">Vérifiez que les indicateurs STATUS_SETTINGS_DIALOG et STATUS_VALIDATE_STATE sont définis dans la propriété **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) du fournisseur de transport cible.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-111">Check that the STATUS_SETTINGS_DIALOG and STATUS_VALIDATE_STATE flags are set in the target transport provider's **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property.</span></span> <span data-ttu-id="4ef8b-112">Si STATUS_SETTINGS_DIALOG n'est pas défini, le fournisseur de transport n'affiche pas de feuille de propriétés de configuration.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-112">If STATUS_SETTINGS_DIALOG is not set, the transport provider does not display a configuration property sheet.</span></span> <span data-ttu-id="4ef8b-113">Si STATUS_VALIDATE_STATE n'est pas défini, vous ne pouvez pas effectuer une reconfiguration dynamique.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-113">If STATUS_VALIDATE_STATE is not set, you cannot perform dynamic reconfiguration.</span></span>
    
5. <span data-ttu-id="4ef8b-114">Si STATUS_SETTINGS_DIALOG est défini, appelez [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) pour afficher la feuille de propriétés du fournisseur de transport et permettre à l'utilisateur d'effectuer des modifications.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-114">If STATUS_SETTINGS_DIALOG is set, call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the transport provider's property sheet and allow the user to make changes.</span></span> 
    
6. <span data-ttu-id="4ef8b-115">Une fois que l'utilisateur a terminé la reconfiguration, appelez [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) si STATUS_VALIDATE_STATE est défini, en passant CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="4ef8b-115">After the user has finished with the reconfiguration, call [IMAPIStatus::ValidateState](imapistatus-validatestate.md) if STATUS_VALIDATE_STATE is set, passing CONFIG_CHANGED.</span></span> 
    

