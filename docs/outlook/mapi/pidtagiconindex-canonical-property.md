---
title: Propriété canonique PidTagIconIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIconIndex
api_type:
- HeaderDef
ms.assetid: 35bb0d6d-41d4-47d6-b161-be3721894201
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 35d9d0a50539f8aab2d26730dd4e4544c2535e60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346619"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="93cfc-103">Propriété canonique PidTagIconIndex</span><span class="sxs-lookup"><span data-stu-id="93cfc-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="93cfc-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93cfc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93cfc-105">Contient un nombre qui indique l’icône à utiliser lorsque vous affichez un groupe d’objets de messagerie.</span><span class="sxs-lookup"><span data-stu-id="93cfc-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="93cfc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="93cfc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="93cfc-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="93cfc-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="93cfc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="93cfc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="93cfc-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="93cfc-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="93cfc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="93cfc-110">Data type:</span></span>  <br/> |<span data-ttu-id="93cfc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="93cfc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="93cfc-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="93cfc-112">Area:</span></span>  <br/> |<span data-ttu-id="93cfc-113">Messagerie générale</span><span class="sxs-lookup"><span data-stu-id="93cfc-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="93cfc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="93cfc-114">Remarks</span></span>

<span data-ttu-id="93cfc-115">Si elle existe, cette propriété est un conseil au client.</span><span class="sxs-lookup"><span data-stu-id="93cfc-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="93cfc-116">Le client peut ignorer la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="93cfc-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="93cfc-117">**État de l’élément de messagerie**</span><span class="sxs-lookup"><span data-stu-id="93cfc-117">**Mail item state**</span></span>|<span data-ttu-id="93cfc-118">**Index d’icône**</span><span class="sxs-lookup"><span data-stu-id="93cfc-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="93cfc-119">Nouveau courrier</span><span class="sxs-lookup"><span data-stu-id="93cfc-119">New mail</span></span>  <br/> |<span data-ttu-id="93cfc-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="93cfc-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="93cfc-121">Publication</span><span class="sxs-lookup"><span data-stu-id="93cfc-121">Post</span></span>  <br/> |<span data-ttu-id="93cfc-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="93cfc-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="93cfc-123">Autre</span><span class="sxs-lookup"><span data-stu-id="93cfc-123">Other</span></span>  <br/> |<span data-ttu-id="93cfc-124">0x00000003</span><span class="sxs-lookup"><span data-stu-id="93cfc-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="93cfc-125">Lire le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="93cfc-125">Read mail</span></span>  <br/> |<span data-ttu-id="93cfc-126">0x00000100</span><span class="sxs-lookup"><span data-stu-id="93cfc-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="93cfc-127">Courrier non lu</span><span class="sxs-lookup"><span data-stu-id="93cfc-127">Unread mail</span></span>  <br/> |<span data-ttu-id="93cfc-128">0x00000101</span><span class="sxs-lookup"><span data-stu-id="93cfc-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="93cfc-129">Courrier envoyé</span><span class="sxs-lookup"><span data-stu-id="93cfc-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="93cfc-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="93cfc-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="93cfc-131">Courrier non envoyé</span><span class="sxs-lookup"><span data-stu-id="93cfc-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="93cfc-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="93cfc-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="93cfc-133">Accusé de réception</span><span class="sxs-lookup"><span data-stu-id="93cfc-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="93cfc-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="93cfc-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="93cfc-135">Courriers électroniques répondus</span><span class="sxs-lookup"><span data-stu-id="93cfc-135">Replied mail</span></span>  <br/> |<span data-ttu-id="93cfc-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="93cfc-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="93cfc-137">Courrier électronique transmis</span><span class="sxs-lookup"><span data-stu-id="93cfc-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="93cfc-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="93cfc-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="93cfc-139">Courrier distant</span><span class="sxs-lookup"><span data-stu-id="93cfc-139">Remote mail</span></span>  <br/> |<span data-ttu-id="93cfc-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="93cfc-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="93cfc-141">Remise du courrier</span><span class="sxs-lookup"><span data-stu-id="93cfc-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="93cfc-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="93cfc-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="93cfc-143">Lire le courrier électronique</span><span class="sxs-lookup"><span data-stu-id="93cfc-143">Read mail</span></span>  <br/> |<span data-ttu-id="93cfc-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="93cfc-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="93cfc-145">Courrier nondelivery</span><span class="sxs-lookup"><span data-stu-id="93cfc-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="93cfc-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="93cfc-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="93cfc-147">Courrier non lu</span><span class="sxs-lookup"><span data-stu-id="93cfc-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="93cfc-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="93cfc-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="93cfc-149">Recall_S courrier électronique</span><span class="sxs-lookup"><span data-stu-id="93cfc-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="93cfc-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="93cfc-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="93cfc-151">Recall_F courrier électronique</span><span class="sxs-lookup"><span data-stu-id="93cfc-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="93cfc-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="93cfc-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="93cfc-153">Suivi du courrier électronique</span><span class="sxs-lookup"><span data-stu-id="93cfc-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="93cfc-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="93cfc-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="93cfc-155">Courrier d’int office</span><span class="sxs-lookup"><span data-stu-id="93cfc-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="93cfc-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="93cfc-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="93cfc-157">Rappeler le courrier</span><span class="sxs-lookup"><span data-stu-id="93cfc-157">Recall mail</span></span>  <br/> |<span data-ttu-id="93cfc-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="93cfc-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="93cfc-159">Courrier suivi</span><span class="sxs-lookup"><span data-stu-id="93cfc-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="93cfc-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="93cfc-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="93cfc-161">Contact</span><span class="sxs-lookup"><span data-stu-id="93cfc-161">Contact</span></span>  <br/> |<span data-ttu-id="93cfc-162">0x00000200</span><span class="sxs-lookup"><span data-stu-id="93cfc-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="93cfc-163">Liste de distribution</span><span class="sxs-lookup"><span data-stu-id="93cfc-163">Distribution list</span></span>  <br/> |<span data-ttu-id="93cfc-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="93cfc-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="93cfc-165">Bleu de note rouge</span><span class="sxs-lookup"><span data-stu-id="93cfc-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="93cfc-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="93cfc-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="93cfc-167">Vert de note rouge</span><span class="sxs-lookup"><span data-stu-id="93cfc-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="93cfc-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="93cfc-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="93cfc-169">Note rose resserrante</span><span class="sxs-lookup"><span data-stu-id="93cfc-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="93cfc-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="93cfc-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="93cfc-171">Jaune de note rouge</span><span class="sxs-lookup"><span data-stu-id="93cfc-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="93cfc-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="93cfc-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="93cfc-173">Blanc de note rouge</span><span class="sxs-lookup"><span data-stu-id="93cfc-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="93cfc-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="93cfc-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="93cfc-175">Rendez-vous à instance unique</span><span class="sxs-lookup"><span data-stu-id="93cfc-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="93cfc-176">0x00000400</span><span class="sxs-lookup"><span data-stu-id="93cfc-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="93cfc-177">Rendez-vous périodique</span><span class="sxs-lookup"><span data-stu-id="93cfc-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="93cfc-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="93cfc-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="93cfc-179">Réunion d’instance unique</span><span class="sxs-lookup"><span data-stu-id="93cfc-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="93cfc-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="93cfc-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="93cfc-181">Réunion périodique</span><span class="sxs-lookup"><span data-stu-id="93cfc-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="93cfc-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="93cfc-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="93cfc-183">Demande de réunion</span><span class="sxs-lookup"><span data-stu-id="93cfc-183">Meeting request</span></span>  <br/> |<span data-ttu-id="93cfc-184">0x00000404</span><span class="sxs-lookup"><span data-stu-id="93cfc-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="93cfc-185">Accepter</span><span class="sxs-lookup"><span data-stu-id="93cfc-185">Accept</span></span>  <br/> |<span data-ttu-id="93cfc-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="93cfc-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="93cfc-187">Refuser</span><span class="sxs-lookup"><span data-stu-id="93cfc-187">Decline</span></span>  <br/> |<span data-ttu-id="93cfc-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="93cfc-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="93cfc-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="93cfc-189">Tentativly</span></span>  <br/> |<span data-ttu-id="93cfc-190">0x00000407</span><span class="sxs-lookup"><span data-stu-id="93cfc-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="93cfc-191">Annulation</span><span class="sxs-lookup"><span data-stu-id="93cfc-191">Cancellation</span></span>  <br/> |<span data-ttu-id="93cfc-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="93cfc-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="93cfc-193">Mise à jour d’informations</span><span class="sxs-lookup"><span data-stu-id="93cfc-193">Informational update</span></span>  <br/> |<span data-ttu-id="93cfc-194">0x00000409</span><span class="sxs-lookup"><span data-stu-id="93cfc-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="93cfc-195">Tâche/tâche</span><span class="sxs-lookup"><span data-stu-id="93cfc-195">Task/task</span></span>  <br/> |<span data-ttu-id="93cfc-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="93cfc-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="93cfc-197">Tâche périodique non résignée</span><span class="sxs-lookup"><span data-stu-id="93cfc-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="93cfc-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="93cfc-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="93cfc-199">Tâche de l’affectation</span><span class="sxs-lookup"><span data-stu-id="93cfc-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="93cfc-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="93cfc-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="93cfc-201">Tâche de l’assigneur</span><span class="sxs-lookup"><span data-stu-id="93cfc-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="93cfc-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="93cfc-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="93cfc-203">Demande de tâche</span><span class="sxs-lookup"><span data-stu-id="93cfc-203">Task request</span></span>  <br/> |<span data-ttu-id="93cfc-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="93cfc-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="93cfc-205">Acceptation des tâches</span><span class="sxs-lookup"><span data-stu-id="93cfc-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="93cfc-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="93cfc-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="93cfc-207">Rejet de tâche</span><span class="sxs-lookup"><span data-stu-id="93cfc-207">Task rejection</span></span>  <br/> |<span data-ttu-id="93cfc-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="93cfc-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="93cfc-209">Conversation de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="93cfc-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="93cfc-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="93cfc-211">Message électronique de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-211">Journal email message</span></span>  <br/> |<span data-ttu-id="93cfc-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="93cfc-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="93cfc-213">Journal de la demande de réunion</span><span class="sxs-lookup"><span data-stu-id="93cfc-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="93cfc-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="93cfc-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="93cfc-215">Réponse à une réunion de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="93cfc-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="93cfc-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="93cfc-217">Demande de tâche de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-217">Journal task request</span></span>  <br/> |<span data-ttu-id="93cfc-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="93cfc-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="93cfc-219">Réponse de la tâche de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-219">Journal task response</span></span>  <br/> |<span data-ttu-id="93cfc-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="93cfc-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="93cfc-221">Note de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-221">Journal note</span></span>  <br/> |<span data-ttu-id="93cfc-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="93cfc-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="93cfc-223">Télécopie de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-223">Journal fax</span></span>  <br/> |<span data-ttu-id="93cfc-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="93cfc-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="93cfc-225">Appel téléphonique de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="93cfc-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="93cfc-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="93cfc-227">Lettre de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-227">Journal letter</span></span>  <br/> |<span data-ttu-id="93cfc-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="93cfc-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="93cfc-229">Journal Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="93cfc-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="93cfc-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="93cfc-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="93cfc-231">Journal Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="93cfc-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="93cfc-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="93cfc-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="93cfc-233">Journal Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="93cfc-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="93cfc-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="93cfc-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="93cfc-235">Accès Microsoft Office journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="93cfc-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="93cfc-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="93cfc-237">Document de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-237">Journal document</span></span>  <br/> |<span data-ttu-id="93cfc-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="93cfc-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="93cfc-239">Réunion de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="93cfc-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="93cfc-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="93cfc-241">Annulation de réunion de journal</span><span class="sxs-lookup"><span data-stu-id="93cfc-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="93cfc-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="93cfc-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="93cfc-243">Journal de session distante</span><span class="sxs-lookup"><span data-stu-id="93cfc-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="93cfc-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="93cfc-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="93cfc-245">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="93cfc-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="93cfc-246">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="93cfc-246">Protocol specifications</span></span>

<span data-ttu-id="93cfc-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93cfc-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93cfc-248">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="93cfc-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="93cfc-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93cfc-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93cfc-250">Spécifie les propriétés et opérations autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="93cfc-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="93cfc-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93cfc-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93cfc-252">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="93cfc-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="93cfc-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="93cfc-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="93cfc-254">Spécifie les propriétés et opérations autorisées sur les contacts et les listes de distribution personnelles.</span><span class="sxs-lookup"><span data-stu-id="93cfc-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="93cfc-255">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="93cfc-255">Header files</span></span>

<span data-ttu-id="93cfc-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="93cfc-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="93cfc-257">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="93cfc-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="93cfc-258">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="93cfc-258">Mapitags.h</span></span>
  
> <span data-ttu-id="93cfc-259">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="93cfc-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93cfc-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="93cfc-260">See also</span></span>



[<span data-ttu-id="93cfc-261">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="93cfc-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="93cfc-262">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="93cfc-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="93cfc-263">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="93cfc-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="93cfc-264">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="93cfc-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

