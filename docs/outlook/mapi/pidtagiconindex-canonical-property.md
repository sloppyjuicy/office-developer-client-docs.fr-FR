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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398107"
---
# <a name="pidtagiconindex-canonical-property"></a><span data-ttu-id="dad46-103">Propriété canonique PidTagIconIndex</span><span class="sxs-lookup"><span data-stu-id="dad46-103">PidTagIconIndex Canonical Property</span></span>

  
  
<span data-ttu-id="dad46-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dad46-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dad46-105">Contient un nombre qui indique l’icône à utiliser lorsque vous affichez un groupe d’objets de messagerie.</span><span class="sxs-lookup"><span data-stu-id="dad46-105">Contains a number that indicates which icon to use when you display a group of email objects.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dad46-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="dad46-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dad46-107">PR_ICON_INDEX</span><span class="sxs-lookup"><span data-stu-id="dad46-107">PR_ICON_INDEX</span></span>  <br/> |
|<span data-ttu-id="dad46-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="dad46-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dad46-109">0x1080</span><span class="sxs-lookup"><span data-stu-id="dad46-109">0x1080</span></span>  <br/> |
|<span data-ttu-id="dad46-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="dad46-110">Data type:</span></span>  <br/> |<span data-ttu-id="dad46-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="dad46-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="dad46-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="dad46-112">Area:</span></span>  <br/> |<span data-ttu-id="dad46-113">Général de messagerie</span><span class="sxs-lookup"><span data-stu-id="dad46-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dad46-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dad46-114">Remarks</span></span>

<span data-ttu-id="dad46-115">Cette propriété, si elle existe, est un indicateur au client.</span><span class="sxs-lookup"><span data-stu-id="dad46-115">This property, if it exists, is a hint to the client.</span></span> <span data-ttu-id="dad46-116">Le client peut ignorer la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dad46-116">The client may ignore the value of this property.</span></span> 
  
|<span data-ttu-id="dad46-117">**Élément d’état de la messagerie**</span><span class="sxs-lookup"><span data-stu-id="dad46-117">**Mail item state**</span></span>|<span data-ttu-id="dad46-118">**Index de l’icône**</span><span class="sxs-lookup"><span data-stu-id="dad46-118">**Icon Index**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dad46-119">Nouveau courrier</span><span class="sxs-lookup"><span data-stu-id="dad46-119">New mail</span></span>  <br/> |<span data-ttu-id="dad46-120">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="dad46-120">0xFFFFFFFF</span></span>  <br/> |
|<span data-ttu-id="dad46-121">Publication</span><span class="sxs-lookup"><span data-stu-id="dad46-121">Post</span></span>  <br/> |<span data-ttu-id="dad46-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="dad46-122">0x00000001</span></span>  <br/> |
|<span data-ttu-id="dad46-123">Other</span><span class="sxs-lookup"><span data-stu-id="dad46-123">Other</span></span>  <br/> |<span data-ttu-id="dad46-124">0 x 00000003</span><span class="sxs-lookup"><span data-stu-id="dad46-124">0x00000003</span></span>  <br/> |
|<span data-ttu-id="dad46-125">Lire le courrier</span><span class="sxs-lookup"><span data-stu-id="dad46-125">Read mail</span></span>  <br/> |<span data-ttu-id="dad46-126">0 x 00000100</span><span class="sxs-lookup"><span data-stu-id="dad46-126">0x00000100</span></span>  <br/> |
|<span data-ttu-id="dad46-127">Courrier non lu</span><span class="sxs-lookup"><span data-stu-id="dad46-127">Unread mail</span></span>  <br/> |<span data-ttu-id="dad46-128">0 x 00000101</span><span class="sxs-lookup"><span data-stu-id="dad46-128">0x00000101</span></span>  <br/> |
|<span data-ttu-id="dad46-129">Courrier envoyé</span><span class="sxs-lookup"><span data-stu-id="dad46-129">Submitted mail</span></span>  <br/> |<span data-ttu-id="dad46-130">0x00000102</span><span class="sxs-lookup"><span data-stu-id="dad46-130">0x00000102</span></span>  <br/> |
|<span data-ttu-id="dad46-131">Messages non envoyés</span><span class="sxs-lookup"><span data-stu-id="dad46-131">Unsent mail</span></span>  <br/> |<span data-ttu-id="dad46-132">0x00000103</span><span class="sxs-lookup"><span data-stu-id="dad46-132">0x00000103</span></span>  <br/> |
|<span data-ttu-id="dad46-133">Messages d’accusé de réception</span><span class="sxs-lookup"><span data-stu-id="dad46-133">Receipt mail</span></span>  <br/> |<span data-ttu-id="dad46-134">0x00000104</span><span class="sxs-lookup"><span data-stu-id="dad46-134">0x00000104</span></span>  <br/> |
|<span data-ttu-id="dad46-135">Messagerie de réponse</span><span class="sxs-lookup"><span data-stu-id="dad46-135">Replied mail</span></span>  <br/> |<span data-ttu-id="dad46-136">0x00000105</span><span class="sxs-lookup"><span data-stu-id="dad46-136">0x00000105</span></span>  <br/> |
|<span data-ttu-id="dad46-137">Courrier transféré</span><span class="sxs-lookup"><span data-stu-id="dad46-137">Forwarded mail</span></span>  <br/> |<span data-ttu-id="dad46-138">0x00000106</span><span class="sxs-lookup"><span data-stu-id="dad46-138">0x00000106</span></span>  <br/> |
|<span data-ttu-id="dad46-139">Courrier à distance</span><span class="sxs-lookup"><span data-stu-id="dad46-139">Remote mail</span></span>  <br/> |<span data-ttu-id="dad46-140">0x00000107</span><span class="sxs-lookup"><span data-stu-id="dad46-140">0x00000107</span></span>  <br/> |
|<span data-ttu-id="dad46-141">Messagerie de remise</span><span class="sxs-lookup"><span data-stu-id="dad46-141">Delivery mail</span></span>  <br/> |<span data-ttu-id="dad46-142">0x00000108</span><span class="sxs-lookup"><span data-stu-id="dad46-142">0x00000108</span></span>  <br/> |
|<span data-ttu-id="dad46-143">Lire le courrier</span><span class="sxs-lookup"><span data-stu-id="dad46-143">Read mail</span></span>  <br/> |<span data-ttu-id="dad46-144">0x00000109</span><span class="sxs-lookup"><span data-stu-id="dad46-144">0x00000109</span></span>  <br/> |
|<span data-ttu-id="dad46-145">Messagerie de non-remise</span><span class="sxs-lookup"><span data-stu-id="dad46-145">Nondelivery mail</span></span>  <br/> |<span data-ttu-id="dad46-146">0x0000010A</span><span class="sxs-lookup"><span data-stu-id="dad46-146">0x0000010A</span></span>  <br/> |
|<span data-ttu-id="dad46-147">Messagerie nonread</span><span class="sxs-lookup"><span data-stu-id="dad46-147">Nonread mail</span></span>  <br/> |<span data-ttu-id="dad46-148">0x0000010B</span><span class="sxs-lookup"><span data-stu-id="dad46-148">0x0000010B</span></span>  <br/> |
|<span data-ttu-id="dad46-149">Messagerie Recall_S</span><span class="sxs-lookup"><span data-stu-id="dad46-149">Recall_S mail</span></span>  <br/> |<span data-ttu-id="dad46-150">0x0000010C</span><span class="sxs-lookup"><span data-stu-id="dad46-150">0x0000010C</span></span>  <br/> |
|<span data-ttu-id="dad46-151">Messagerie Recall_F</span><span class="sxs-lookup"><span data-stu-id="dad46-151">Recall_F mail</span></span>  <br/> |<span data-ttu-id="dad46-152">0x0000010D</span><span class="sxs-lookup"><span data-stu-id="dad46-152">0x0000010D</span></span>  <br/> |
|<span data-ttu-id="dad46-153">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="dad46-153">Tracking mail</span></span>  <br/> |<span data-ttu-id="dad46-154">0x0000010E</span><span class="sxs-lookup"><span data-stu-id="dad46-154">0x0000010E</span></span>  <br/> |
|<span data-ttu-id="dad46-155">En dehors de la messagerie office</span><span class="sxs-lookup"><span data-stu-id="dad46-155">Out of office mail</span></span>  <br/> |<span data-ttu-id="dad46-156">0x0000011B</span><span class="sxs-lookup"><span data-stu-id="dad46-156">0x0000011B</span></span>  <br/> |
|<span data-ttu-id="dad46-157">Rappeler la messagerie</span><span class="sxs-lookup"><span data-stu-id="dad46-157">Recall mail</span></span>  <br/> |<span data-ttu-id="dad46-158">0x0000011C</span><span class="sxs-lookup"><span data-stu-id="dad46-158">0x0000011C</span></span>  <br/> |
|<span data-ttu-id="dad46-159">Suivi des messages</span><span class="sxs-lookup"><span data-stu-id="dad46-159">Tracked mail</span></span>  <br/> |<span data-ttu-id="dad46-160">0x00000130</span><span class="sxs-lookup"><span data-stu-id="dad46-160">0x00000130</span></span>  <br/> |
|<span data-ttu-id="dad46-161">Contact</span><span class="sxs-lookup"><span data-stu-id="dad46-161">Contact</span></span>  <br/> |<span data-ttu-id="dad46-162">0 x 00000200</span><span class="sxs-lookup"><span data-stu-id="dad46-162">0x00000200</span></span>  <br/> |
|<span data-ttu-id="dad46-163">Liste de distribution</span><span class="sxs-lookup"><span data-stu-id="dad46-163">Distribution list</span></span>  <br/> |<span data-ttu-id="dad46-164">0x00000202</span><span class="sxs-lookup"><span data-stu-id="dad46-164">0x00000202</span></span>  <br/> |
|<span data-ttu-id="dad46-165">Bleu pense-bête</span><span class="sxs-lookup"><span data-stu-id="dad46-165">Sticky note blue</span></span>  <br/> |<span data-ttu-id="dad46-166">0x00000300</span><span class="sxs-lookup"><span data-stu-id="dad46-166">0x00000300</span></span>  <br/> |
|<span data-ttu-id="dad46-167">Vert pense-bête</span><span class="sxs-lookup"><span data-stu-id="dad46-167">Sticky note green</span></span>  <br/> |<span data-ttu-id="dad46-168">0x00000301</span><span class="sxs-lookup"><span data-stu-id="dad46-168">0x00000301</span></span>  <br/> |
|<span data-ttu-id="dad46-169">Rose pense-bête</span><span class="sxs-lookup"><span data-stu-id="dad46-169">Sticky note pink</span></span>  <br/> |<span data-ttu-id="dad46-170">0x00000302</span><span class="sxs-lookup"><span data-stu-id="dad46-170">0x00000302</span></span>  <br/> |
|<span data-ttu-id="dad46-171">Jaune pense-bête</span><span class="sxs-lookup"><span data-stu-id="dad46-171">Sticky note yellow</span></span>  <br/> |<span data-ttu-id="dad46-172">0x00000303</span><span class="sxs-lookup"><span data-stu-id="dad46-172">0x00000303</span></span>  <br/> |
|<span data-ttu-id="dad46-173">Livre pense-bête</span><span class="sxs-lookup"><span data-stu-id="dad46-173">Sticky note white</span></span>  <br/> |<span data-ttu-id="dad46-174">0x00000304</span><span class="sxs-lookup"><span data-stu-id="dad46-174">0x00000304</span></span>  <br/> |
|<span data-ttu-id="dad46-175">Rendez-vous unique</span><span class="sxs-lookup"><span data-stu-id="dad46-175">Single instance appointment</span></span>  <br/> |<span data-ttu-id="dad46-176">0 x 00000400</span><span class="sxs-lookup"><span data-stu-id="dad46-176">0x00000400</span></span>  <br/> |
|<span data-ttu-id="dad46-177">Rendez-vous périodique</span><span class="sxs-lookup"><span data-stu-id="dad46-177">Recurring appointment</span></span>  <br/> |<span data-ttu-id="dad46-178">0x00000401</span><span class="sxs-lookup"><span data-stu-id="dad46-178">0x00000401</span></span>  <br/> |
|<span data-ttu-id="dad46-179">Réunion unique</span><span class="sxs-lookup"><span data-stu-id="dad46-179">Single instance meeting</span></span>  <br/> |<span data-ttu-id="dad46-180">0x00000402</span><span class="sxs-lookup"><span data-stu-id="dad46-180">0x00000402</span></span>  <br/> |
|<span data-ttu-id="dad46-181">Réunion périodique</span><span class="sxs-lookup"><span data-stu-id="dad46-181">Recurring meeting</span></span>  <br/> |<span data-ttu-id="dad46-182">0x00000403</span><span class="sxs-lookup"><span data-stu-id="dad46-182">0x00000403</span></span>  <br/> |
|<span data-ttu-id="dad46-183">Demande de réunion</span><span class="sxs-lookup"><span data-stu-id="dad46-183">Meeting request</span></span>  <br/> |<span data-ttu-id="dad46-184">0 x 00000404</span><span class="sxs-lookup"><span data-stu-id="dad46-184">0x00000404</span></span>  <br/> |
|<span data-ttu-id="dad46-185">Accepter</span><span class="sxs-lookup"><span data-stu-id="dad46-185">Accept</span></span>  <br/> |<span data-ttu-id="dad46-186">0x00000405</span><span class="sxs-lookup"><span data-stu-id="dad46-186">0x00000405</span></span>  <br/> |
|<span data-ttu-id="dad46-187">Refuser</span><span class="sxs-lookup"><span data-stu-id="dad46-187">Decline</span></span>  <br/> |<span data-ttu-id="dad46-188">0x00000406</span><span class="sxs-lookup"><span data-stu-id="dad46-188">0x00000406</span></span>  <br/> |
|<span data-ttu-id="dad46-189">Tentativly</span><span class="sxs-lookup"><span data-stu-id="dad46-189">Tentativly</span></span>  <br/> |<span data-ttu-id="dad46-190">0 x 00000407</span><span class="sxs-lookup"><span data-stu-id="dad46-190">0x00000407</span></span>  <br/> |
|<span data-ttu-id="dad46-191">Annulation</span><span class="sxs-lookup"><span data-stu-id="dad46-191">Cancellation</span></span>  <br/> |<span data-ttu-id="dad46-192">0x00000408</span><span class="sxs-lookup"><span data-stu-id="dad46-192">0x00000408</span></span>  <br/> |
|<span data-ttu-id="dad46-193">Mise à jour d’information</span><span class="sxs-lookup"><span data-stu-id="dad46-193">Informational update</span></span>  <br/> |<span data-ttu-id="dad46-194">0 x 00000409</span><span class="sxs-lookup"><span data-stu-id="dad46-194">0x00000409</span></span>  <br/> |
|<span data-ttu-id="dad46-195">/ Tâche</span><span class="sxs-lookup"><span data-stu-id="dad46-195">Task/task</span></span>  <br/> |<span data-ttu-id="dad46-196">0x00000500</span><span class="sxs-lookup"><span data-stu-id="dad46-196">0x00000500</span></span>  <br/> |
|<span data-ttu-id="dad46-197">Tâche périodique non attribué</span><span class="sxs-lookup"><span data-stu-id="dad46-197">Unassigned recurring task</span></span>  <br/> |<span data-ttu-id="dad46-198">0x00000501</span><span class="sxs-lookup"><span data-stu-id="dad46-198">0x00000501</span></span>  <br/> |
|<span data-ttu-id="dad46-199">Tâche de la personne affectée</span><span class="sxs-lookup"><span data-stu-id="dad46-199">Assignee's task</span></span>  <br/> |<span data-ttu-id="dad46-200">0x00000502</span><span class="sxs-lookup"><span data-stu-id="dad46-200">0x00000502</span></span>  <br/> |
|<span data-ttu-id="dad46-201">Tâche d’assigne</span><span class="sxs-lookup"><span data-stu-id="dad46-201">Assigner's task</span></span>  <br/> |<span data-ttu-id="dad46-202">0x00000503</span><span class="sxs-lookup"><span data-stu-id="dad46-202">0x00000503</span></span>  <br/> |
|<span data-ttu-id="dad46-203">Demande de tâche</span><span class="sxs-lookup"><span data-stu-id="dad46-203">Task request</span></span>  <br/> |<span data-ttu-id="dad46-204">0x00000504</span><span class="sxs-lookup"><span data-stu-id="dad46-204">0x00000504</span></span>  <br/> |
|<span data-ttu-id="dad46-205">Acceptation de tâche</span><span class="sxs-lookup"><span data-stu-id="dad46-205">Task acceptance</span></span>  <br/> |<span data-ttu-id="dad46-206">0x00000505</span><span class="sxs-lookup"><span data-stu-id="dad46-206">0x00000505</span></span>  <br/> |
|<span data-ttu-id="dad46-207">Refus de tâche</span><span class="sxs-lookup"><span data-stu-id="dad46-207">Task rejection</span></span>  <br/> |<span data-ttu-id="dad46-208">0x00000506</span><span class="sxs-lookup"><span data-stu-id="dad46-208">0x00000506</span></span>  <br/> |
|<span data-ttu-id="dad46-209">Conversation de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-209">Journal conversation</span></span>  <br/> |<span data-ttu-id="dad46-210">0x00000601</span><span class="sxs-lookup"><span data-stu-id="dad46-210">0x00000601</span></span>  <br/> |
|<span data-ttu-id="dad46-211">Message électronique de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-211">Journal email message</span></span>  <br/> |<span data-ttu-id="dad46-212">0x00000602</span><span class="sxs-lookup"><span data-stu-id="dad46-212">0x00000602</span></span>  <br/> |
|<span data-ttu-id="dad46-213">Demande de réunion de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-213">Journal meeting request</span></span>  <br/> |<span data-ttu-id="dad46-214">0x00000603</span><span class="sxs-lookup"><span data-stu-id="dad46-214">0x00000603</span></span>  <br/> |
|<span data-ttu-id="dad46-215">Réponse à une réunion journal</span><span class="sxs-lookup"><span data-stu-id="dad46-215">Journal meeting response</span></span>  <br/> |<span data-ttu-id="dad46-216">0x00000604</span><span class="sxs-lookup"><span data-stu-id="dad46-216">0x00000604</span></span>  <br/> |
|<span data-ttu-id="dad46-217">Demande de tâche de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-217">Journal task request</span></span>  <br/> |<span data-ttu-id="dad46-218">0x00000606</span><span class="sxs-lookup"><span data-stu-id="dad46-218">0x00000606</span></span>  <br/> |
|<span data-ttu-id="dad46-219">Réponse de la tâche feuille</span><span class="sxs-lookup"><span data-stu-id="dad46-219">Journal task response</span></span>  <br/> |<span data-ttu-id="dad46-220">0x00000607</span><span class="sxs-lookup"><span data-stu-id="dad46-220">0x00000607</span></span>  <br/> |
|<span data-ttu-id="dad46-221">Note du journal</span><span class="sxs-lookup"><span data-stu-id="dad46-221">Journal note</span></span>  <br/> |<span data-ttu-id="dad46-222">0x00000608</span><span class="sxs-lookup"><span data-stu-id="dad46-222">0x00000608</span></span>  <br/> |
|<span data-ttu-id="dad46-223">Télécopie de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-223">Journal fax</span></span>  <br/> |<span data-ttu-id="dad46-224">0x00000609</span><span class="sxs-lookup"><span data-stu-id="dad46-224">0x00000609</span></span>  <br/> |
|<span data-ttu-id="dad46-225">Appel téléphonique de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-225">Journal phone call</span></span>  <br/> |<span data-ttu-id="dad46-226">0x0000060A</span><span class="sxs-lookup"><span data-stu-id="dad46-226">0x0000060A</span></span>  <br/> |
|<span data-ttu-id="dad46-227">Lettre de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-227">Journal letter</span></span>  <br/> |<span data-ttu-id="dad46-228">0x0000060C</span><span class="sxs-lookup"><span data-stu-id="dad46-228">0x0000060C</span></span>  <br/> |
|<span data-ttu-id="dad46-229">Feuille Microsoft Office Word</span><span class="sxs-lookup"><span data-stu-id="dad46-229">Journal Microsoft Office Word</span></span>  <br/> |<span data-ttu-id="dad46-230">0x0000060D</span><span class="sxs-lookup"><span data-stu-id="dad46-230">0x0000060D</span></span>  <br/> |
|<span data-ttu-id="dad46-231">Feuille Microsoft Office Excel</span><span class="sxs-lookup"><span data-stu-id="dad46-231">Journal Microsoft Office Excel</span></span>  <br/> |<span data-ttu-id="dad46-232">0x0000060E</span><span class="sxs-lookup"><span data-stu-id="dad46-232">0x0000060E</span></span>  <br/> |
|<span data-ttu-id="dad46-233">Feuille Microsoft Office PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dad46-233">Journal Microsoft Office PowerPoint</span></span>  <br/> |<span data-ttu-id="dad46-234">0x0000060F</span><span class="sxs-lookup"><span data-stu-id="dad46-234">0x0000060F</span></span>  <br/> |
|<span data-ttu-id="dad46-235">Feuille Microsoft Office Access</span><span class="sxs-lookup"><span data-stu-id="dad46-235">Journal Microsoft Office Access</span></span>  <br/> |<span data-ttu-id="dad46-236">0x00000610</span><span class="sxs-lookup"><span data-stu-id="dad46-236">0x00000610</span></span>  <br/> |
|<span data-ttu-id="dad46-237">Document de feuille</span><span class="sxs-lookup"><span data-stu-id="dad46-237">Journal document</span></span>  <br/> |<span data-ttu-id="dad46-238">0x00000612</span><span class="sxs-lookup"><span data-stu-id="dad46-238">0x00000612</span></span>  <br/> |
|<span data-ttu-id="dad46-239">Réunion de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-239">Journal meeting</span></span>  <br/> |<span data-ttu-id="dad46-240">0x00000613</span><span class="sxs-lookup"><span data-stu-id="dad46-240">0x00000613</span></span>  <br/> |
|<span data-ttu-id="dad46-241">Annulation de réunion de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-241">Journal meeting cancellation</span></span>  <br/> |<span data-ttu-id="dad46-242">0x00000614</span><span class="sxs-lookup"><span data-stu-id="dad46-242">0x00000614</span></span>  <br/> |
|<span data-ttu-id="dad46-243">Session à distance de journal</span><span class="sxs-lookup"><span data-stu-id="dad46-243">Journal remote session</span></span>  <br/> |<span data-ttu-id="dad46-244">0x00000615</span><span class="sxs-lookup"><span data-stu-id="dad46-244">0x00000615</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="dad46-245">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="dad46-245">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dad46-246">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="dad46-246">Protocol specifications</span></span>

<span data-ttu-id="dad46-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dad46-247">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dad46-248">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="dad46-248">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dad46-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dad46-249">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dad46-250">Spécifie les propriétés et les opérations qui sont autorisées sur les objets de message électronique.</span><span class="sxs-lookup"><span data-stu-id="dad46-250">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
<span data-ttu-id="dad46-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dad46-251">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dad46-252">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="dad46-252">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="dad46-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dad46-253">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dad46-254">Spécifie les propriétés et les opérations qui sont autorisées sur les contacts et les listes de distribution personnelle.</span><span class="sxs-lookup"><span data-stu-id="dad46-254">Specifies the properties and operations that are permissible on contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dad46-255">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="dad46-255">Header files</span></span>

<span data-ttu-id="dad46-256">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dad46-256">Mapidefs.h</span></span>
  
> <span data-ttu-id="dad46-257">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="dad46-257">Provides data type definitions.</span></span>
    
<span data-ttu-id="dad46-258">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="dad46-258">Mapitags.h</span></span>
  
> <span data-ttu-id="dad46-259">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="dad46-259">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dad46-260">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dad46-260">See also</span></span>



[<span data-ttu-id="dad46-261">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="dad46-261">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="dad46-262">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="dad46-262">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dad46-263">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="dad46-263">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dad46-264">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="dad46-264">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

