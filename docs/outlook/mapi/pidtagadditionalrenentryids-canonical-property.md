---
title: Propriété canonique PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 5b357a068249b12468be52f8782f646f394e4060
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567824"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a><span data-ttu-id="45775-103">Propriété canonique PidTagAdditionalRenEntryIds</span><span class="sxs-lookup"><span data-stu-id="45775-103">PidTagAdditionalRenEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="45775-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45775-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45775-105">Contient les identificateurs d’entrée de certains dossiers spéciaux.</span><span class="sxs-lookup"><span data-stu-id="45775-105">Contains the entry IDs of certain special folders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45775-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="45775-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="45775-107">PR_ADDITIONAL_REN_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="45775-107">PR_ADDITIONAL_REN_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="45775-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="45775-108">Identifier:</span></span>  <br/> |<span data-ttu-id="45775-109">0x36D8</span><span class="sxs-lookup"><span data-stu-id="45775-109">0x36D8</span></span>  <br/> |
|<span data-ttu-id="45775-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="45775-110">Data type:</span></span>  <br/> |<span data-ttu-id="45775-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="45775-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="45775-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="45775-112">Area:</span></span>  <br/> |<span data-ttu-id="45775-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="45775-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45775-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="45775-114">Remarks</span></span>

<span data-ttu-id="45775-115">Les cinq premières entrées de cette propriété à valeurs multiples s’appliquent aux dossiers spéciaux suivants, s’ils existent dans le magasin :</span><span class="sxs-lookup"><span data-stu-id="45775-115">The first five entries of this multi-valued property apply to following special folders, if they exist in the store:</span></span>
  
<span data-ttu-id="45775-116">0 - dossier conflits</span><span class="sxs-lookup"><span data-stu-id="45775-116">0 - conflicts folder</span></span>
  
<span data-ttu-id="45775-117">-1 dossier problèmes de synchronisation</span><span class="sxs-lookup"><span data-stu-id="45775-117">1 - sync issues folder</span></span>
  
<span data-ttu-id="45775-118">2 - dossier défaillances local</span><span class="sxs-lookup"><span data-stu-id="45775-118">2 - local failures folder</span></span>
  
<span data-ttu-id="45775-119">3 - dossier des échecs serveur</span><span class="sxs-lookup"><span data-stu-id="45775-119">3 - server failures folder</span></span>
  
<span data-ttu-id="45775-120">4 - dossier courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="45775-120">4 - junk email folder</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="45775-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="45775-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="45775-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="45775-122">Protocol specifications</span></span>

<span data-ttu-id="45775-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45775-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45775-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="45775-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="45775-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45775-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45775-126">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="45775-126">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="45775-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45775-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45775-128">Identifie et marque les messages électroniques qui sont conçues pour amener les destinataires à dévoiler des informations sensibles (comme les mots de passe et autres informations personnelles) à une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="45775-128">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
<span data-ttu-id="45775-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="45775-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="45775-130">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="45775-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="45775-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="45775-131">Header files</span></span>

<span data-ttu-id="45775-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="45775-132">Mapitags.h</span></span>
  
> <span data-ttu-id="45775-133">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="45775-133">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="45775-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="45775-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="45775-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="45775-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="45775-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45775-136">See also</span></span>



[<span data-ttu-id="45775-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="45775-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="45775-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="45775-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="45775-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="45775-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


[<span data-ttu-id="45775-140">À propos de l’API de magasin</span><span class="sxs-lookup"><span data-stu-id="45775-140">About the Store API</span></span>](http://msdn.microsoft.com/en-us/library/aa192884.aspx)

