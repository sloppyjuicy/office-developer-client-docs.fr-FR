---
title: Propriété canonique PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279628"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="bb798-103">Propriété canonique PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="bb798-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="bb798-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb798-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb798-105">Contient la valeur d'un champ d'en-tête d'aide sur la liste des messages MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="bb798-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="bb798-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="bb798-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="bb798-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="bb798-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="bb798-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="bb798-108">Identifier:</span></span>  <br/> |<span data-ttu-id="bb798-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="bb798-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="bb798-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="bb798-110">Data type:</span></span>  <br/> |<span data-ttu-id="bb798-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="bb798-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="bb798-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="bb798-112">Area:</span></span>  <br/> |<span data-ttu-id="bb798-113">Divers</span><span class="sxs-lookup"><span data-stu-id="bb798-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb798-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb798-114">Remarks</span></span>

<span data-ttu-id="bb798-115">Pour générer un champ d'en-tête d'aide sur la liste, les clients doivent définir la valeur de **PR_LIST_HELP** ou une propriété associée sur la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="bb798-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="bb798-116">Les enregistreurs MIME doivent copier cette valeur dans le champ d'en-tête de liste d'aide.</span><span class="sxs-lookup"><span data-stu-id="bb798-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="bb798-117">Pour définir la valeur de ces propriétés liées au serveur de liste, les clients MIME doivent écrire les champs d'en-tête comme indiqué dans le tableau suivant:</span><span class="sxs-lookup"><span data-stu-id="bb798-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="bb798-118">**Property**</span><span class="sxs-lookup"><span data-stu-id="bb798-118">**Property**</span></span>|<span data-ttu-id="bb798-119">**Nom de champ d'en-tête préféré**</span><span class="sxs-lookup"><span data-stu-id="bb798-119">**Preferred header field name**</span></span>|<span data-ttu-id="bb798-120">**Nom de champ d'en-tête secondaire**</span><span class="sxs-lookup"><span data-stu-id="bb798-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb798-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="bb798-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="bb798-122">Liste-aide</span><span class="sxs-lookup"><span data-stu-id="bb798-122">List-Help</span></span>  <br/> |<span data-ttu-id="bb798-123">X-List-aide</span><span class="sxs-lookup"><span data-stu-id="bb798-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="bb798-124">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="bb798-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="bb798-125">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="bb798-125">Protocol specifications</span></span>

<span data-ttu-id="bb798-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb798-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb798-127">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="bb798-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="bb798-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="bb798-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="bb798-129">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="bb798-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="bb798-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="bb798-130">Header files</span></span>

<span data-ttu-id="bb798-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="bb798-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="bb798-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="bb798-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="bb798-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="bb798-133">Mapitags.h</span></span>
  
> <span data-ttu-id="bb798-134">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="bb798-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="bb798-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb798-135">See also</span></span>



[<span data-ttu-id="bb798-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="bb798-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="bb798-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="bb798-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="bb798-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="bb798-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="bb798-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="bb798-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

