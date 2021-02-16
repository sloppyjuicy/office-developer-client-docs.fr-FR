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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 501b54cfb7846a91aec7172cbe1d846c24704923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331499"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="fda0d-103">Propriété canonique PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="fda0d-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="fda0d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fda0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fda0d-105">Contient une valeur de champ d’en-tête Content-Base [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="fda0d-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fda0d-106">Noms convivial :</span><span class="sxs-lookup"><span data-stu-id="fda0d-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="fda0d-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="fda0d-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="fda0d-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="fda0d-108">Property set:</span></span>  <br/> |<span data-ttu-id="fda0d-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="fda0d-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="fda0d-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="fda0d-110">Property name:</span></span>  <br/> |<span data-ttu-id="fda0d-111">Content-Base</span><span class="sxs-lookup"><span data-stu-id="fda0d-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="fda0d-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fda0d-112">Data type:</span></span>  <br/> |<span data-ttu-id="fda0d-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fda0d-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fda0d-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fda0d-114">Area:</span></span>  <br/> |<span data-ttu-id="fda0d-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="fda0d-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fda0d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="fda0d-116">Remarks</span></span>

<span data-ttu-id="fda0d-117">Pour définir la valeur de cette propriété, les clients MIME (Multipurpose Internet Message Extensions) doivent écrire la valeur souhaitée dans un champ d’en-tête Content-Base sur une entité MIME migré à un corps de message.</span><span class="sxs-lookup"><span data-stu-id="fda0d-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="fda0d-118">Les lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Base sur une entité MIME de ce type vers la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="fda0d-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fda0d-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fda0d-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fda0d-120">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="fda0d-120">Protocol specifications</span></span>

<span data-ttu-id="fda0d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fda0d-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fda0d-122">Fournit des définitions de jeu de propriétés et des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="fda0d-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fda0d-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fda0d-123">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fda0d-124">Convertit des conventions de messagerie standard Internet en objets de message.</span><span class="sxs-lookup"><span data-stu-id="fda0d-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fda0d-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fda0d-125">Header files</span></span>

<span data-ttu-id="fda0d-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fda0d-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="fda0d-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fda0d-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fda0d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fda0d-128">See also</span></span>



[<span data-ttu-id="fda0d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fda0d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fda0d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fda0d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fda0d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fda0d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fda0d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fda0d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

