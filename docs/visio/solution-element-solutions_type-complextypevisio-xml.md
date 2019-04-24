---
title: Solution, élément (Solutions_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Spécifie une instance du code XML de la solution stockée dans le dessin.
ms.openlocfilehash: bb3cd512ff6109467c9d6465ba72c764d83abf96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335265"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="52a41-103">Solution, élément (Solutions_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="52a41-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="52a41-104">Spécifie une instance du code XML de la solution stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="52a41-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="52a41-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="52a41-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="52a41-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="52a41-106">**Element type**</span></span> <br/> |[<span data-ttu-id="52a41-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="52a41-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="52a41-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="52a41-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="52a41-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="52a41-109">**Schema file**</span></span> <br/> |<span data-ttu-id="52a41-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="52a41-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="52a41-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="52a41-111">**Document parts**</span></span> <br/> |<span data-ttu-id="52a41-112">solutions. Xml</span><span class="sxs-lookup"><span data-stu-id="52a41-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="52a41-113">Définition</span><span class="sxs-lookup"><span data-stu-id="52a41-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="52a41-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="52a41-114">Elements and attributes</span></span>

<span data-ttu-id="52a41-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="52a41-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="52a41-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="52a41-116">Parent elements</span></span>

|<span data-ttu-id="52a41-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="52a41-117">**Element**</span></span>|<span data-ttu-id="52a41-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="52a41-118">**Type**</span></span>|<span data-ttu-id="52a41-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="52a41-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52a41-120">Solutions</span><span class="sxs-lookup"><span data-stu-id="52a41-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="52a41-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="52a41-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="52a41-122">Stocke les propriétés des solutions stockées dans le document.</span><span class="sxs-lookup"><span data-stu-id="52a41-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="52a41-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="52a41-123">Child elements</span></span>

|<span data-ttu-id="52a41-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="52a41-124">**Element**</span></span>|<span data-ttu-id="52a41-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="52a41-125">**Type**</span></span>|<span data-ttu-id="52a41-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="52a41-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="52a41-127">Ver</span><span class="sxs-lookup"><span data-stu-id="52a41-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="52a41-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="52a41-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="52a41-129">Spécifie la relation à un composant avec le code XML de la solution associé à cette solution.</span><span class="sxs-lookup"><span data-stu-id="52a41-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="52a41-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="52a41-130">Attributes</span></span>

|<span data-ttu-id="52a41-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="52a41-131">**Attribute**</span></span>|<span data-ttu-id="52a41-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="52a41-132">**Type**</span></span>|<span data-ttu-id="52a41-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="52a41-133">**Required**</span></span>|<span data-ttu-id="52a41-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="52a41-134">**Description**</span></span>|<span data-ttu-id="52a41-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="52a41-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="52a41-136">Nom</span><span class="sxs-lookup"><span data-stu-id="52a41-136">Name</span></span>  <br/> |<span data-ttu-id="52a41-137">xsd: String</span><span class="sxs-lookup"><span data-stu-id="52a41-137">xsd:string</span></span>  <br/> |<span data-ttu-id="52a41-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="52a41-138">required</span></span>  <br/> |<span data-ttu-id="52a41-139">Nom de la solution.</span><span class="sxs-lookup"><span data-stu-id="52a41-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="52a41-140">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="52a41-140">Values of the xsd:string type.</span></span>  <br/> |
   

