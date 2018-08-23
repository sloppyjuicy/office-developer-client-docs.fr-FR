---
title: Propriété canonique PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583357"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a><span data-ttu-id="5baa6-103">Propriété canonique PidTagDisplayTypeEx</span><span class="sxs-lookup"><span data-stu-id="5baa6-103">PidTagDisplayTypeEx Canonical Property</span></span>

  
  
<span data-ttu-id="5baa6-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5baa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5baa6-105">Contient le type d’une entrée, en ce qui concerne l’entrée affichage sur une ligne dans une table de la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="5baa6-105">Contains the type of an entry, with respect to how the entry should be displayed in a row in a table for the Global Address List.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5baa6-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5baa6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5baa6-107">PR_DISPLAY_TYPE_EX</span><span class="sxs-lookup"><span data-stu-id="5baa6-107">PR_DISPLAY_TYPE_EX</span></span>  <br/> |
|<span data-ttu-id="5baa6-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5baa6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5baa6-109">0x3905</span><span class="sxs-lookup"><span data-stu-id="5baa6-109">0x3905</span></span>  <br/> |
|<span data-ttu-id="5baa6-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5baa6-110">Data type:</span></span>  <br/> |<span data-ttu-id="5baa6-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="5baa6-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="5baa6-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5baa6-112">Area:</span></span>  <br/> |<span data-ttu-id="5baa6-113">Carnet d’adresses MAPI</span><span class="sxs-lookup"><span data-stu-id="5baa6-113">MAPI address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5baa6-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5baa6-114">Remarks</span></span>

<span data-ttu-id="5baa6-115">Cette propriété spécifie le type d’une entrée, en ce qui concerne comment il doit être affiché dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="5baa6-115">This property specifies the type of an entry, with respect to how it should be displayed in the Global Address List.</span></span> <span data-ttu-id="5baa6-116">Il fournit des informations supplémentaires qui ne peut pas être représentées dans **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5baa6-116">It provides additional information that cannot be represented in **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
  
> [!NOTE]
> <span data-ttu-id="5baa6-117">Les valeurs de cette propriété et **PR_DISPLAY_TYPE** commencent par « Du préfixeDT_ » et sont définies dans Mapitags.h.</span><span class="sxs-lookup"><span data-stu-id="5baa6-117">The values of both **PR_DISPLAY_TYPE** and this property begin with "DT_" and are defined in Mapitags.h.</span></span> <span data-ttu-id="5baa6-118">Toutes les valeurs non documentées sont réservés pour MAPI.</span><span class="sxs-lookup"><span data-stu-id="5baa6-118">All values not documented are reserved for MAPI.</span></span> <span data-ttu-id="5baa6-119">Applications clientes ne doivent pas définir de nouvelles valeurs et doivent être prêts à traiter avec une valeur non documentée.</span><span class="sxs-lookup"><span data-stu-id="5baa6-119">Client applications must not define any new values and must be prepared to deal with an undocumented value.</span></span> 
  
<span data-ttu-id="5baa6-120">Il existe certaines macros qui peuvent aider à déterminer les attributs d’un objet tel qu’il s’agisse local, à distance ou sécurisé.</span><span class="sxs-lookup"><span data-stu-id="5baa6-120">There are some macros that can help determine attributes of an object such as whether it is local, remote, or security-controlled.</span></span> <span data-ttu-id="5baa6-121">Ces macros sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="5baa6-121">These macros include:</span></span> 
  
|<span data-ttu-id="5baa6-122">**Macro**</span><span class="sxs-lookup"><span data-stu-id="5baa6-122">**Macro**</span></span>|<span data-ttu-id="5baa6-123">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5baa6-123">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5baa6-124">DTE_FLAG_REMOTE_VALID</span><span class="sxs-lookup"><span data-stu-id="5baa6-124">DTE_FLAG_REMOTE_VALID</span></span>  <br/> |<span data-ttu-id="5baa6-125">0 x 80000000)</span><span class="sxs-lookup"><span data-stu-id="5baa6-125">0x80000000)</span></span>  <br/> |
|<span data-ttu-id="5baa6-126">DTE_FLAG_ACL_CAPABLE</span><span class="sxs-lookup"><span data-stu-id="5baa6-126">DTE_FLAG_ACL_CAPABLE</span></span>  <br/> |<span data-ttu-id="5baa6-127">0 x 40000000</span><span class="sxs-lookup"><span data-stu-id="5baa6-127">0x40000000</span></span>  <br/> |
|<span data-ttu-id="5baa6-128">DTE_MASK_REMOTE</span><span class="sxs-lookup"><span data-stu-id="5baa6-128">DTE_MASK_REMOTE</span></span>  <br/> |<span data-ttu-id="5baa6-129">0x0000ff00</span><span class="sxs-lookup"><span data-stu-id="5baa6-129">0x0000ff00</span></span>  <br/> |
|<span data-ttu-id="5baa6-130">DTE_MASK_LOCAL</span><span class="sxs-lookup"><span data-stu-id="5baa6-130">DTE_MASK_LOCAL</span></span>  <br/> |<span data-ttu-id="5baa6-131">0x000000ff</span><span class="sxs-lookup"><span data-stu-id="5baa6-131">0x000000ff</span></span>  <br/> |
|<span data-ttu-id="5baa6-132">DTE_IS_REMOTE_VALID(v)</span><span class="sxs-lookup"><span data-stu-id="5baa6-132">DTE_IS_REMOTE_VALID(v)</span></span>  <br/> |<span data-ttu-id="5baa6-133">(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)</span><span class="sxs-lookup"><span data-stu-id="5baa6-133">(!!((v) &amp; DTE_FLAG_REMOTE_VALID)</span></span>  <br/> |
|<span data-ttu-id="5baa6-134">DTE_IS_ACL_CAPABLE(v)</span><span class="sxs-lookup"><span data-stu-id="5baa6-134">DTE_IS_ACL_CAPABLE(v)</span></span>  <br/> |<span data-ttu-id="5baa6-135">(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))</span><span class="sxs-lookup"><span data-stu-id="5baa6-135">(!!((v) &amp; DTE_FLAG_ACL_CAPABLE))</span></span>  <br/> |
|<span data-ttu-id="5baa6-136">DTE_REMOTE(v)</span><span class="sxs-lookup"><span data-stu-id="5baa6-136">DTE_REMOTE(v)</span></span>  <br/> |<span data-ttu-id="5baa6-137">(((v) &amp; DTE_MASK_REMOTE) \> \> 8)</span><span class="sxs-lookup"><span data-stu-id="5baa6-137">(((v) &amp; DTE_MASK_REMOTE) \>\> 8)</span></span>  <br/> |
|<span data-ttu-id="5baa6-138">DTE_LOCAL(v)</span><span class="sxs-lookup"><span data-stu-id="5baa6-138">DTE_LOCAL(v)</span></span>  <br/> |<span data-ttu-id="5baa6-139">((v) &amp; DTE_MASK_LOCAL)</span><span class="sxs-lookup"><span data-stu-id="5baa6-139">((v) &amp; DTE_MASK_LOCAL)</span></span>  <br/> |
|<span data-ttu-id="5baa6-140">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="5baa6-140">DT_ROOM</span></span>  <br/> |<span data-ttu-id="5baa6-141">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="5baa6-141">((ULONG) 0x00000007)</span></span>  <br/> |
|<span data-ttu-id="5baa6-142">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="5baa6-142">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="5baa6-143">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="5baa6-143">((ULONG) 0x00000008)</span></span>  <br/> |
|<span data-ttu-id="5baa6-144">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5baa6-144">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="5baa6-145">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="5baa6-145">((ULONG) 0x00000009)</span></span>  <br/> |
   
<span data-ttu-id="5baa6-146">Voici quelques conseils sur l’utilisation de ces macros.</span><span class="sxs-lookup"><span data-stu-id="5baa6-146">The following are a few notes about how to use these macros.</span></span> 
  
- <span data-ttu-id="5baa6-147">Pour vérifier si une entrée est une entrée dans une autre forêt distante, appliquer la macro DTE_IS_REMOTE_VALID à la valeur de cette propriété pour vérifier si l’indicateur DTE_FLAG_REMOTE_VALID est défini dans l’entrée.</span><span class="sxs-lookup"><span data-stu-id="5baa6-147">To check whether an entry is a remote entry in another forest, apply the DTE_IS_REMOTE_VALID macro to the value of this property to check whether the DTE_FLAG_REMOTE_VALID flag is set in the entry.</span></span> <span data-ttu-id="5baa6-148">S’il s’agit d’une entrée à distance, vous pouvez puis déterminer le type de l’entrée à distance à l’aide de la macro DTE_REMOTE.</span><span class="sxs-lookup"><span data-stu-id="5baa6-148">If it is a remote entry, you can then find out the type of the remote entry by using the DTE_REMOTE macro.</span></span> 
    
- <span data-ttu-id="5baa6-149">Dans les configurations de forêt unique et de plusieurs forêts, lorsque **PR_DISPLAY_TYPE** a la valeur de DT_DISTLIST et DTE_IS_REMOTE_VALID a la valeur false, l’application de la macro DTE_LOCAL à la valeur de cette propriété peut vous permettre de mieux identifier le type de l’objet en tant que DT_DISTLIST (une liste de distribution) ou DT_SEC_DISTLIST (une liste de distribution de sécurité).</span><span class="sxs-lookup"><span data-stu-id="5baa6-149">In both single-forest and cross-forest configurations, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST, and DTE_IS_REMOTE_VALID is false, applying the macro DTE_LOCAL to the value of this property can let you further identify the type of the object as either DT_DISTLIST (a distribution list) or DT_SEC_DISTLIST (a security distribution list).</span></span> 
    
- <span data-ttu-id="5baa6-150">Si vous appliquez la macro DTE_LOCAL à la valeur de **PR_DISPLAY_TYPE_EX** , et elle renvoie le type DT_REMOTE_MAILUSER, l’entrée est une entrée à distance.</span><span class="sxs-lookup"><span data-stu-id="5baa6-150">If you apply the macro DTE_LOCAL to the value of **PR_DISPLAY_TYPE_EX** and it returns the type DT_REMOTE_MAILUSER, then the entry is a remote entry.</span></span> 
    
- <span data-ttu-id="5baa6-151">Dans une seule forêt ou dans une configuration de plusieurs forêts où la réplication est contrôlée par une liste de contrôle d’accès (ACL), vous pouvez utiliser la macro DTE_IS_ACL_CAPABLE pour déterminer si une entrée est une entité de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5baa6-151">In a single forest or in a cross-forest configuration where replication is controlled by an Access Control List (ACL), you can use the DTE_IS_ACL_CAPABLE macro to determine whether an entry is a security principal.</span></span>
    
<span data-ttu-id="5baa6-152">Dans une configuration de plusieurs forêts, **PR_DISPLAY_TYPE** a la valeur DT_REMOTE_MAILUSER.</span><span class="sxs-lookup"><span data-stu-id="5baa6-152">In a cross-forest configuration, **PR_DISPLAY_TYPE** has the value of DT_REMOTE_MAILUSER.</span></span> <span data-ttu-id="5baa6-153">Application de la macro DTE_REMOTE à la valeur de cette propriété peut vous permettre d’obtenir le type de l’entrée à distance.</span><span class="sxs-lookup"><span data-stu-id="5baa6-153">Applying the macro DTE_REMOTE to the value of this property can let you obtain the type of the remote entry.</span></span> <span data-ttu-id="5baa6-154">Les types possibles d’entrée à distance sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5baa6-154">The possible types of remote entry are the following:</span></span> 
  
|<span data-ttu-id="5baa6-155">**Type d’entrée à distance**</span><span class="sxs-lookup"><span data-stu-id="5baa6-155">**Type of Remote Entry**</span></span>|<span data-ttu-id="5baa6-156">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5baa6-156">**Value**</span></span>|<span data-ttu-id="5baa6-157">**Description**</span><span class="sxs-lookup"><span data-stu-id="5baa6-157">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5baa6-158">DT_AGENT</span><span class="sxs-lookup"><span data-stu-id="5baa6-158">DT_AGENT</span></span>  <br/> |<span data-ttu-id="5baa6-159">((ULONG) 0 X 00000003)</span><span class="sxs-lookup"><span data-stu-id="5baa6-159">((ULONG) 0x00000003)</span></span>  <br/> |<span data-ttu-id="5baa6-160">Liste de distribution dynamique.</span><span class="sxs-lookup"><span data-stu-id="5baa6-160">Dynamic distribution list.</span></span>  <br/> |
|<span data-ttu-id="5baa6-161">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5baa6-161">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="5baa6-162">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="5baa6-162">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5baa6-163">Liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="5baa6-163">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="5baa6-164">DT_EQUIPMENT</span><span class="sxs-lookup"><span data-stu-id="5baa6-164">DT_EQUIPMENT</span></span>  <br/> |<span data-ttu-id="5baa6-165">((ULONG) 0 X 00000008)</span><span class="sxs-lookup"><span data-stu-id="5baa6-165">((ULONG) 0x00000008)</span></span>  <br/> |<span data-ttu-id="5baa6-166">Équipement, par exemple, une imprimante ou un projecteur.</span><span class="sxs-lookup"><span data-stu-id="5baa6-166">Equipment, for example, a printer or a projector.</span></span>  <br/> |
|<span data-ttu-id="5baa6-167">DT_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="5baa6-167">DT_MAILUSER</span></span>  <br/> |<span data-ttu-id="5baa6-168">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="5baa6-168">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="5baa6-169">Utilisateur disposant d’une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="5baa6-169">User with a mailbox.</span></span>  <br/> |
|<span data-ttu-id="5baa6-170">DT_REMOTE_MAILUSER</span><span class="sxs-lookup"><span data-stu-id="5baa6-170">DT_REMOTE_MAILUSER</span></span>  <br/> |<span data-ttu-id="5baa6-171">((ULONG) 0 X 00000000)</span><span class="sxs-lookup"><span data-stu-id="5baa6-171">((ULONG) 0x00000000)</span></span>  <br/> |<span data-ttu-id="5baa6-172">Une entrée de liste d’adresses dans la liste d’adresses globale.</span><span class="sxs-lookup"><span data-stu-id="5baa6-172">An address list entry in the Global Address List.</span></span>  <br/> |
|<span data-ttu-id="5baa6-173">DT_ROOM</span><span class="sxs-lookup"><span data-stu-id="5baa6-173">DT_ROOM</span></span>  <br/> |<span data-ttu-id="5baa6-174">((ULONG) 0 X 00000007)</span><span class="sxs-lookup"><span data-stu-id="5baa6-174">((ULONG) 0x00000007)</span></span>  <br/> |<span data-ttu-id="5baa6-175">Salle de conférence.</span><span class="sxs-lookup"><span data-stu-id="5baa6-175">Conference room.</span></span>  <br/> |
|<span data-ttu-id="5baa6-176">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5baa6-176">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="5baa6-177">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="5baa6-177">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="5baa6-178">Liste de distribution de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5baa6-178">Security distribution list.</span></span>  <br/> |
   
<span data-ttu-id="5baa6-179">Dans une seule forêt et dans plusieurs forêts configuration, lorsque **PR_DISPLAY_TYPE** a la valeur de DT_DISTLIST et DTE_IS_REMOTE_VALID a la valeur false, l’application de la macro DTE_LOCAL à la valeur de cette propriété peut vous permettre d’obtenir le type de la liste de distribution .</span><span class="sxs-lookup"><span data-stu-id="5baa6-179">In both a single forest and in a cross-forest configuration, when **PR_DISPLAY_TYPE** has the value of DT_DISTLIST and DTE_IS_REMOTE_VALID is false, applying the DTE_LOCAL macro to the value of this property can let you obtain the type of the distribution list.</span></span> <span data-ttu-id="5baa6-180">Les types de liste de distribution possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5baa6-180">The possible types of distribution list are the following:</span></span> 
  
|<span data-ttu-id="5baa6-181">**Type de liste de Distribution**</span><span class="sxs-lookup"><span data-stu-id="5baa6-181">**Type of Distribution List**</span></span>|<span data-ttu-id="5baa6-182">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5baa6-182">**Value**</span></span>|<span data-ttu-id="5baa6-183">**Description**</span><span class="sxs-lookup"><span data-stu-id="5baa6-183">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5baa6-184">DT_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5baa6-184">DT_DISTLIST</span></span>  <br/> |<span data-ttu-id="5baa6-185">((ULONG) 0 X 00000001)</span><span class="sxs-lookup"><span data-stu-id="5baa6-185">((ULONG) 0x00000001)</span></span>  <br/> |<span data-ttu-id="5baa6-186">Liste de distribution.</span><span class="sxs-lookup"><span data-stu-id="5baa6-186">Distribution list.</span></span>  <br/> |
|<span data-ttu-id="5baa6-187">DT_SEC_DISTLIST</span><span class="sxs-lookup"><span data-stu-id="5baa6-187">DT_SEC_DISTLIST</span></span>  <br/> |<span data-ttu-id="5baa6-188">((ULONG) 0 X 00000009)</span><span class="sxs-lookup"><span data-stu-id="5baa6-188">((ULONG) 0x00000009)</span></span>  <br/> |<span data-ttu-id="5baa6-189">Liste de distribution de sécurité.</span><span class="sxs-lookup"><span data-stu-id="5baa6-189">Security distribution list.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="5baa6-190">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="5baa6-190">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5baa6-191">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="5baa6-191">Protocol specifications</span></span>

<span data-ttu-id="5baa6-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5baa6-192">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5baa6-193">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="5baa6-193">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5baa6-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5baa6-194">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5baa6-195">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="5baa6-195">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5baa6-196">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="5baa6-196">Header files</span></span>

<span data-ttu-id="5baa6-197">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5baa6-197">Mapidefs.h</span></span>
  
> <span data-ttu-id="5baa6-198">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5baa6-198">Provides data type definitions.</span></span>
    
<span data-ttu-id="5baa6-199">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="5baa6-199">Mapitags.h</span></span>
  
> <span data-ttu-id="5baa6-200">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="5baa6-200">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5baa6-201">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5baa6-201">See also</span></span>



[<span data-ttu-id="5baa6-202">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5baa6-202">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5baa6-203">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5baa6-203">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5baa6-204">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5baa6-204">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5baa6-205">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5baa6-205">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

