---
title: Propriété canonique PidTagInternetReferences
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInternetReferences
api_type:
- HeaderDef
ms.assetid: 645fe61d-414a-455e-b034-db3cfd003b9d
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 431a212b6e024d695fe2de084080996d8b1054d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360409"
---
# <a name="pidtaginternetreferences-canonical-property"></a><span data-ttu-id="b0d91-103">Propriété canonique PidTagInternetReferences</span><span class="sxs-lookup"><span data-stu-id="b0d91-103">PidTagInternetReferences Canonical Property</span></span>

  
  
<span data-ttu-id="b0d91-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0d91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0d91-105">Contient la valeur du champ d'en-tête références d'un message MIME (Multipurpose Internet Mail Extensions).</span><span class="sxs-lookup"><span data-stu-id="b0d91-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's References header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b0d91-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b0d91-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b0d91-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span><span class="sxs-lookup"><span data-stu-id="b0d91-107">PR_INTERNET_REFERENCES, PR_INTERNET_REFERENCES_A, PR_INTERNET_REFERENCES_W</span></span>  <br/> |
|<span data-ttu-id="b0d91-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b0d91-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b0d91-109">0x1039</span><span class="sxs-lookup"><span data-stu-id="b0d91-109">0x1039</span></span>  <br/> |
|<span data-ttu-id="b0d91-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b0d91-110">Data type:</span></span>  <br/> |<span data-ttu-id="b0d91-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b0d91-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="b0d91-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b0d91-112">Area:</span></span>  <br/> |<span data-ttu-id="b0d91-113">MIME</span><span class="sxs-lookup"><span data-stu-id="b0d91-113">MIME</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0d91-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b0d91-114">Remarks</span></span>

<span data-ttu-id="b0d91-115">Pour générer un champ d'en-tête References, les clients doivent définir ces propriétés sur la valeur souhaitée.</span><span class="sxs-lookup"><span data-stu-id="b0d91-115">To generate a References header field, clients must set these properties to the desired value.</span></span> <span data-ttu-id="b0d91-116">Les enregistreurs MIME doivent copier la valeur de ces propriétés dans le champ d'en-tête References.</span><span class="sxs-lookup"><span data-stu-id="b0d91-116">MIME writers must copy the value of these properties to the References header field.</span></span>
  
<span data-ttu-id="b0d91-117">Pour définir la valeur de ces propriétés, les clients MIME doivent écrire la valeur souhaitée dans un champ d'en-tête References.</span><span class="sxs-lookup"><span data-stu-id="b0d91-117">To set the value of these properties, MIME clients must write the desired value to a References header field.</span></span> <span data-ttu-id="b0d91-118">Les lecteurs MIME doivent copier la valeur du champ d'en-tête références sur ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b0d91-118">MIME readers must copy the value of the References header field to these properties.</span></span> <span data-ttu-id="b0d91-119">Les lecteurs MIME peuvent tronquer la valeur de ces propriétés si elles dépassent la longueur de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="b0d91-119">MIME readers may truncate the value of these properties if it exceeds 64KB in length.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b0d91-120">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="b0d91-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b0d91-121">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="b0d91-121">Protocol specifications</span></span>

<span data-ttu-id="b0d91-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0d91-122">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0d91-123">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="b0d91-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b0d91-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b0d91-124">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b0d91-125">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="b0d91-125">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b0d91-126">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="b0d91-126">Header files</span></span>

<span data-ttu-id="b0d91-127">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="b0d91-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="b0d91-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b0d91-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="b0d91-129">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="b0d91-129">Mapitags.h</span></span>
  
> <span data-ttu-id="b0d91-130">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="b0d91-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b0d91-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0d91-131">See also</span></span>



[<span data-ttu-id="b0d91-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d91-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b0d91-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d91-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b0d91-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b0d91-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b0d91-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b0d91-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

