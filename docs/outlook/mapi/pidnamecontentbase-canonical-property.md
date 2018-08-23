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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 91eb93c9cf3afcecef698e27791c06831c13624d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589097"
---
# <a name="pidnamecontentbase-canonical-property"></a><span data-ttu-id="1c0dc-103">Propriété canonique PidNameContentBase</span><span class="sxs-lookup"><span data-stu-id="1c0dc-103">PidNameContentBase Canonical Property</span></span>

  
  
<span data-ttu-id="1c0dc-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c0dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c0dc-105">Contient une valeur de champ d’en-tête Content-Base [RFC3282].</span><span class="sxs-lookup"><span data-stu-id="1c0dc-105">Contains an [RFC3282] Content-Base header field value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1c0dc-106">Noms conviviaux :</span><span class="sxs-lookup"><span data-stu-id="1c0dc-106">Friendly names:</span></span>  <br/> |<span data-ttu-id="1c0dc-107">BodyContentBase</span><span class="sxs-lookup"><span data-stu-id="1c0dc-107">BodyContentBase</span></span>  <br/> |
|<span data-ttu-id="1c0dc-108">Jeu de propriétés :</span><span class="sxs-lookup"><span data-stu-id="1c0dc-108">Property set:</span></span>  <br/> |<span data-ttu-id="1c0dc-109">PS_INTERNET_HEADERS</span><span class="sxs-lookup"><span data-stu-id="1c0dc-109">PS_INTERNET_HEADERS</span></span>  <br/> |
|<span data-ttu-id="1c0dc-110">Nom de la propriété :</span><span class="sxs-lookup"><span data-stu-id="1c0dc-110">Property name:</span></span>  <br/> |<span data-ttu-id="1c0dc-111">Base de contenu</span><span class="sxs-lookup"><span data-stu-id="1c0dc-111">Content-Base</span></span>  <br/> |
|<span data-ttu-id="1c0dc-112">Type de données :</span><span class="sxs-lookup"><span data-stu-id="1c0dc-112">Data type:</span></span>  <br/> |<span data-ttu-id="1c0dc-113">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1c0dc-113">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1c0dc-114">Domaine :</span><span class="sxs-lookup"><span data-stu-id="1c0dc-114">Area:</span></span>  <br/> |<span data-ttu-id="1c0dc-115">E-mail</span><span class="sxs-lookup"><span data-stu-id="1c0dc-115">Email</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c0dc-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c0dc-116">Remarks</span></span>

<span data-ttu-id="1c0dc-117">Pour définir la valeur de cette propriété, les clients Message Extensions MIME (Multipurpose Internet) doivent écrire la valeur souhaitée pour un champ d’en-tête Content-Base sur une entité MIME qui mappe sur un corps de message.</span><span class="sxs-lookup"><span data-stu-id="1c0dc-117">To set the value of this property, Multipurpose Internet Message Extensions (MIME) clients must write the desired value to a Content-Base header field on a MIME entity that maps to a message body.</span></span> <span data-ttu-id="1c0dc-118">Lecteurs MIME doivent copier la valeur d’un champ d’en-tête Content-Base sur ce une entité MIME sur la valeur de cette propriété.</span><span class="sxs-lookup"><span data-stu-id="1c0dc-118">MIME readers must copy the value of a Content-Base header field on such a MIME entity to the value of this property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="1c0dc-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="1c0dc-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1c0dc-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="1c0dc-120">Protocol specifications</span></span>

<span data-ttu-id="1c0dc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0dc-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0dc-122">Fournit des définitions de jeu de propriétés et des références aux spécifications du protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="1c0dc-122">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1c0dc-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1c0dc-123">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1c0dc-124">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="1c0dc-124">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1c0dc-125">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="1c0dc-125">Header files</span></span>

<span data-ttu-id="1c0dc-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1c0dc-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="1c0dc-127">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="1c0dc-127">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1c0dc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1c0dc-128">See also</span></span>



[<span data-ttu-id="1c0dc-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0dc-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1c0dc-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0dc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1c0dc-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="1c0dc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1c0dc-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="1c0dc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

