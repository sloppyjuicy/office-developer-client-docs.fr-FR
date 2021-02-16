---
title: Élément Solution (Solutions_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Spécifie une instance de solution XML stockée dans le dessin.
ms.openlocfilehash: 028decf0ac9b33ac33dd1e44ed3992ef7eb38aed
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540265"
---
# <a name="solution-element-solutions_type-complextype-visio-xml"></a><span data-ttu-id="95044-103">Élément Solution (Solutions_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="95044-103">Solution element (Solutions_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="95044-104">Spécifie une instance de solution XML stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="95044-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="95044-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="95044-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="95044-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="95044-106">**Element type**</span></span> <br/> |[<span data-ttu-id="95044-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="95044-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="95044-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="95044-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="95044-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="95044-109">**Schema file**</span></span> <br/> |<span data-ttu-id="95044-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="95044-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="95044-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="95044-111">**Document parts**</span></span> <br/> |<span data-ttu-id="95044-112">solutions.xml</span><span class="sxs-lookup"><span data-stu-id="95044-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="95044-113">Définition</span><span class="sxs-lookup"><span data-stu-id="95044-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="95044-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="95044-114">Elements and attributes</span></span>

<span data-ttu-id="95044-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="95044-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="95044-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="95044-116">Parent elements</span></span>

|<span data-ttu-id="95044-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="95044-117">**Element**</span></span>|<span data-ttu-id="95044-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="95044-118">**Type**</span></span>|<span data-ttu-id="95044-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="95044-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95044-120">Solutions</span><span class="sxs-lookup"><span data-stu-id="95044-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="95044-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="95044-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95044-122">Stocke les propriétés des solutions stockées dans le document.</span><span class="sxs-lookup"><span data-stu-id="95044-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="95044-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="95044-123">Child elements</span></span>

|<span data-ttu-id="95044-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="95044-124">**Element**</span></span>|<span data-ttu-id="95044-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="95044-125">**Type**</span></span>|<span data-ttu-id="95044-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="95044-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="95044-127">Rel</span><span class="sxs-lookup"><span data-stu-id="95044-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="95044-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="95044-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="95044-129">Spécifie la relation à un élément avec le XML de solution associé à cette solution.</span><span class="sxs-lookup"><span data-stu-id="95044-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="95044-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="95044-130">Attributes</span></span>

|<span data-ttu-id="95044-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="95044-131">**Attribute**</span></span>|<span data-ttu-id="95044-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="95044-132">**Type**</span></span>|<span data-ttu-id="95044-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="95044-133">**Required**</span></span>|<span data-ttu-id="95044-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="95044-134">**Description**</span></span>|<span data-ttu-id="95044-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="95044-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="95044-136">Nom</span><span class="sxs-lookup"><span data-stu-id="95044-136">Name</span></span>  <br/> |<span data-ttu-id="95044-137">xsd:string</span><span class="sxs-lookup"><span data-stu-id="95044-137">xsd:string</span></span>  <br/> |<span data-ttu-id="95044-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="95044-138">required</span></span>  <br/> |<span data-ttu-id="95044-139">Nom de la solution.</span><span class="sxs-lookup"><span data-stu-id="95044-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="95044-140">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="95044-140">Values of the xsd:string type.</span></span>  <br/> |
   

