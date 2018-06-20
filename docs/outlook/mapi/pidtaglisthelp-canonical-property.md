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
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786203"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="c5b4d-103">Propriété canonique PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="c5b4d-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="c5b4d-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c5b4d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c5b4d-105">Contient la valeur du champ d’en-tête d’un message Multipurpose Internet Mail Extensions (MIME) aide à la liste.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c5b4d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c5b4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c5b4d-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="c5b4d-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="c5b4d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c5b4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c5b4d-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="c5b4d-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="c5b4d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c5b4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="c5b4d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c5b4d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c5b4d-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c5b4d-112">Area:</span></span>  <br/> |<span data-ttu-id="c5b4d-113">Divers</span><span class="sxs-lookup"><span data-stu-id="c5b4d-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5b4d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5b4d-114">Remarks</span></span>

<span data-ttu-id="c5b4d-115">Pour générer un champ d’en-tête de l’aide de la liste, les clients doivent définir la valeur de **PR_LIST_HELP** ou une propriété associée à la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="c5b4d-116">Rédacteurs MIME doivent copiez cette valeur dans le champ d’en-tête de l’aide de la liste.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="c5b4d-117">Pour définir la valeur de ces propriétés liées au serveur de la liste, les clients MIME doivent écrire les champs d’en-tête tel que spécifié dans le tableau suivant :</span><span class="sxs-lookup"><span data-stu-id="c5b4d-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="c5b4d-118">**Propriété**</span><span class="sxs-lookup"><span data-stu-id="c5b4d-118">**Property**</span></span>|<span data-ttu-id="c5b4d-119">**Nom de champ d’en-tête par défaut**</span><span class="sxs-lookup"><span data-stu-id="c5b4d-119">**Preferred header field name**</span></span>|<span data-ttu-id="c5b4d-120">**Nom de champ d’en-tête de substitution**</span><span class="sxs-lookup"><span data-stu-id="c5b4d-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c5b4d-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="c5b4d-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="c5b4d-122">Aide à la liste</span><span class="sxs-lookup"><span data-stu-id="c5b4d-122">List-Help</span></span>  <br/> |<span data-ttu-id="c5b4d-123">X-liste-Help</span><span class="sxs-lookup"><span data-stu-id="c5b4d-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="c5b4d-124">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c5b4d-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c5b4d-125">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c5b4d-125">Protocol specifications</span></span>

<span data-ttu-id="c5b4d-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5b4d-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5b4d-127">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c5b4d-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c5b4d-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c5b4d-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c5b4d-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c5b4d-130">Header files</span></span>

<span data-ttu-id="c5b4d-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c5b4d-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="c5b4d-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="c5b4d-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c5b4d-133">Mapitags.h</span></span>
  
> <span data-ttu-id="c5b4d-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c5b4d-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c5b4d-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b4d-135">See also</span></span>



[<span data-ttu-id="c5b4d-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b4d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c5b4d-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b4d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c5b4d-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c5b4d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c5b4d-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c5b4d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

