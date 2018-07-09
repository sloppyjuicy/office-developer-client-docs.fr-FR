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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e63d661ab8c7e410d6a0dd786819cc189813017e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785668"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a><span data-ttu-id="16049-103">Propriété canonique PidTagAdditionalRenEntryIds</span><span class="sxs-lookup"><span data-stu-id="16049-103">PidTagAdditionalRenEntryIds Canonical Property</span></span>

  
  
<span data-ttu-id="16049-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="16049-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="16049-105">Contient les identificateurs d’entrée de certains dossiers spéciaux.</span><span class="sxs-lookup"><span data-stu-id="16049-105">Contains the entry IDs of certain special folders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16049-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="16049-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="16049-107">PR_ADDITIONAL_REN_ENTRYIDS</span><span class="sxs-lookup"><span data-stu-id="16049-107">PR_ADDITIONAL_REN_ENTRYIDS</span></span>  <br/> |
|<span data-ttu-id="16049-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="16049-108">Identifier:</span></span>  <br/> |<span data-ttu-id="16049-109">0x36D8</span><span class="sxs-lookup"><span data-stu-id="16049-109">0x36D8</span></span>  <br/> |
|<span data-ttu-id="16049-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="16049-110">Data type:</span></span>  <br/> |<span data-ttu-id="16049-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="16049-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="16049-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="16049-112">Area:</span></span>  <br/> |<span data-ttu-id="16049-113">Application Outlook</span><span class="sxs-lookup"><span data-stu-id="16049-113">Outlook application</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="16049-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="16049-114">Remarks</span></span>

<span data-ttu-id="16049-115">Les cinq premières entrées de cette propriété à valeurs multiples s’appliquent aux dossiers spéciaux suivants, s’ils existent dans le magasin :</span><span class="sxs-lookup"><span data-stu-id="16049-115">The first five entries of this multi-valued property apply to following special folders, if they exist in the store:</span></span>
  
<span data-ttu-id="16049-116">0 - dossier conflits</span><span class="sxs-lookup"><span data-stu-id="16049-116">0 - conflicts folder</span></span>
  
<span data-ttu-id="16049-117">-1 dossier problèmes de synchronisation</span><span class="sxs-lookup"><span data-stu-id="16049-117">1 - sync issues folder</span></span>
  
<span data-ttu-id="16049-118">2 - dossier défaillances local</span><span class="sxs-lookup"><span data-stu-id="16049-118">2 - local failures folder</span></span>
  
<span data-ttu-id="16049-119">3 - dossier des échecs serveur</span><span class="sxs-lookup"><span data-stu-id="16049-119">3 - server failures folder</span></span>
  
<span data-ttu-id="16049-120">4 - dossier courrier indésirable</span><span class="sxs-lookup"><span data-stu-id="16049-120">4 - junk email folder</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="16049-121">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="16049-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="16049-122">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="16049-122">Protocol specifications</span></span>

<span data-ttu-id="16049-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16049-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16049-124">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="16049-124">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="16049-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16049-125">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16049-126">Spécifie les propriétés et opérations pour la création et la localisation des dossiers spéciaux dans une boîte aux lettres.</span><span class="sxs-lookup"><span data-stu-id="16049-126">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="16049-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16049-127">[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16049-128">Identifie et marque les messages électroniques qui sont conçues pour amener les destinataires à dévoiler des informations sensibles (comme les mots de passe et autres informations personnelles) à une source non fiable.</span><span class="sxs-lookup"><span data-stu-id="16049-128">Identifies and marks email messages that are designed to trick recipients into divulging sensitive information (such as passwords and other personal information) to a non-trustworthy source.</span></span>
    
<span data-ttu-id="16049-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="16049-129">[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="16049-130">Permet la gestion des listes autoriser/bloquer et la détermination des messages de courrier indésirable.</span><span class="sxs-lookup"><span data-stu-id="16049-130">Enables the handling of allow/block lists and the determination of junk email messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="16049-131">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="16049-131">Header files</span></span>

<span data-ttu-id="16049-132">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="16049-132">Mapitags.h</span></span>
  
> <span data-ttu-id="16049-133">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="16049-133">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="16049-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16049-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="16049-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="16049-135">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="16049-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="16049-136">See also</span></span>



[<span data-ttu-id="16049-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="16049-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="16049-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="16049-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="16049-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="16049-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)


[<span data-ttu-id="16049-140">À propos de l’API du magasin</span><span class="sxs-lookup"><span data-stu-id="16049-140">About the Store API</span></span>](http://msdn.microsoft.com/fr-fr/library/aa192884.aspx)

