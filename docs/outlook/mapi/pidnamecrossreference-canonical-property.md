---
title: Propriété canonique PidNameCrossReference
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameCrossReference
api_type:
- COM
ms.assetid: d16e1adf-c911-427e-9c98-678a303e6791
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 8f8706ec3db36cddbe7be7420ba27683c190cd43
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331443"
---
# <a name="pidnamecrossreference-canonical-property"></a><span data-ttu-id="0bb68-103">Propriété canonique PidNameCrossReference</span><span class="sxs-lookup"><span data-stu-id="0bb68-103">PidNameCrossReference Canonical Property</span></span>

  
  
<span data-ttu-id="0bb68-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bb68-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bb68-105">Contient une valeur de champ d'en-tête RFC3282] XREF.</span><span class="sxs-lookup"><span data-stu-id="0bb68-105">Contains an [RFC3282] Xref header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0bb68-106">Noms conviviaux:</span><span class="sxs-lookup"><span data-stu-id="0bb68-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="0bb68-107">Aucun</span><span class="sxs-lookup"><span data-stu-id="0bb68-107">None</span></span>  <br/> |
|<span data-ttu-id="0bb68-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="0bb68-108">Property set:</span></span>  <br/> |<span data-ttu-id="0bb68-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="0bb68-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="0bb68-110">Nom de la propriété:</span><span class="sxs-lookup"><span data-stu-id="0bb68-110">Property name:</span></span>  <br/> |<span data-ttu-id="0bb68-111">Crois</span><span class="sxs-lookup"><span data-stu-id="0bb68-111">Xref</span></span>  <br/> |
|<span data-ttu-id="0bb68-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0bb68-112">Data type:</span></span>  <br/> |<span data-ttu-id="0bb68-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0bb68-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0bb68-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0bb68-114">Area:</span></span>  <br/> |<span data-ttu-id="0bb68-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="0bb68-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0bb68-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="0bb68-116">Remarks</span></span>

<span data-ttu-id="0bb68-117">Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message extensions) doivent écrire la valeur souhaitée dans un champ d'en-tête XRef.</span><span class="sxs-lookup"><span data-stu-id="0bb68-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to an XRef header field.</span></span> <span data-ttu-id="0bb68-118">Les lecteurs MIME doivent copier la valeur d'un champ d'en-tête XRef à la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="0bb68-118">MIME readers must copy the value of an XRef header field to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0bb68-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="0bb68-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0bb68-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="0bb68-120">Protocol specifications</span></span>

<span data-ttu-id="0bb68-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bb68-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bb68-122">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="0bb68-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0bb68-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0bb68-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0bb68-124">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="0bb68-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0bb68-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="0bb68-125">Header files</span></span>

<span data-ttu-id="0bb68-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0bb68-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="0bb68-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0bb68-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0bb68-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bb68-128">See also</span></span>



[<span data-ttu-id="0bb68-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0bb68-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0bb68-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0bb68-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0bb68-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0bb68-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0bb68-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0bb68-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

