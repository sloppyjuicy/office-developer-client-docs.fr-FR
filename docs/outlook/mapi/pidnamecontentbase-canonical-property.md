---
title: Propriété canonique PidNameContentBase
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentBase
api_type:
- COM
ms.assetid: ab197ace-6e7d-4ec5-9f6d-4a63a1eda11c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331499"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="872ea-103">Propriété canonique PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="872ea-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="872ea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="872ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="872ea-105">Contient une valeur de champ d'en-tête [RFC3282] Content-base.</span><span class="sxs-lookup"><span data-stu-id="872ea-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="872ea-106">Noms conviviaux:</span><span class="sxs-lookup"><span data-stu-id="872ea-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="872ea-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="872ea-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="872ea-108">Jeu de propriétés:</span><span class="sxs-lookup"><span data-stu-id="872ea-108">Property set:</span></span>  <br/> |<span data-ttu-id="872ea-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="872ea-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="872ea-110">Nom de la propriété:</span><span class="sxs-lookup"><span data-stu-id="872ea-110">Property name:</span></span>  <br/> |<span data-ttu-id="872ea-111">Content-base</span><span class="sxs-lookup"><span data-stu-id="872ea-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="872ea-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="872ea-112">Data type:</span></span>  <br/> |<span data-ttu-id="872ea-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="872ea-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="872ea-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="872ea-114">Area:</span></span>  <br/> |<span data-ttu-id="872ea-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="872ea-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="872ea-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="872ea-116">Remarks</span></span>

<span data-ttu-id="872ea-117">Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message extensions) doivent écrire la valeur souhaitée dans un champ d'en-tête Content-base sur une entité MIME qui mappe à un corps de message.</span><span class="sxs-lookup"><span data-stu-id="872ea-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="872ea-118">Les lecteurs MIME doivent copier la valeur d'un champ d'en-tête Content-base sur une entité MIME de ce type vers la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="872ea-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="872ea-119">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="872ea-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="872ea-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="872ea-120">Protocol specifications</span></span>

<span data-ttu-id="872ea-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="872ea-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="872ea-122">Fournit des définitions de jeu de propriétés et des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="872ea-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="872ea-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="872ea-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="872ea-124">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="872ea-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="872ea-125">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="872ea-125">Header files</span></span>

<span data-ttu-id="872ea-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="872ea-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="872ea-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="872ea-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="872ea-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="872ea-128">See also</span></span>



[<span data-ttu-id="872ea-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="872ea-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="872ea-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="872ea-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="872ea-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="872ea-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="872ea-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="872ea-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

