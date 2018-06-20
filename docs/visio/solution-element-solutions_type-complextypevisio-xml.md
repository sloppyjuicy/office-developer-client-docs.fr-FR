---
title: Solution, élément (Solutions_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 46bf34be-761e-9d44-ab06-83d4c8932cab
description: Spécifie une instance d’une solution que XML stocké dans le dessin.
ms.openlocfilehash: 06cefcbf9b0191a9dded5548a457c4a0e50a33ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789786"
---
# <a name="solution-element-solutionstype-complextype-visio-xml"></a><span data-ttu-id="2f634-103">Solution, élément (Solutions_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2f634-103">Solution element (Solutions_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2f634-104">Spécifie une instance d’une solution que XML stocké dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="2f634-104">Specifies one instance of solution XML stored in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2f634-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2f634-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2f634-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2f634-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2f634-107">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="2f634-107">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2f634-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2f634-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2f634-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2f634-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2f634-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2f634-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2f634-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="2f634-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2f634-112">solutions.Xml</span><span class="sxs-lookup"><span data-stu-id="2f634-112">solutions.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2f634-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2f634-113">Definition</span></span>

```XML
< xs:element name="Solution"  type="Solution_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2f634-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2f634-114">Elements and attributes</span></span>

<span data-ttu-id="2f634-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2f634-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2f634-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2f634-116">Parent elements</span></span>

|<span data-ttu-id="2f634-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2f634-117">**Element**</span></span>|<span data-ttu-id="2f634-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="2f634-118">**Type**</span></span>|<span data-ttu-id="2f634-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f634-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f634-120">Solutions</span><span class="sxs-lookup"><span data-stu-id="2f634-120">Solutions</span></span>](solutions-elementvisio-xml.md) <br/> |[<span data-ttu-id="2f634-121">Solutions_Type</span><span class="sxs-lookup"><span data-stu-id="2f634-121">Solutions_Type</span></span>](solutions_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f634-122">Stocke les propriétés des solutions stockées dans le document.</span><span class="sxs-lookup"><span data-stu-id="2f634-122">Stores the properties of the solutions stored in the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2f634-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2f634-123">Child elements</span></span>

|<span data-ttu-id="2f634-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2f634-124">**Element**</span></span>|<span data-ttu-id="2f634-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="2f634-125">**Type**</span></span>|<span data-ttu-id="2f634-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f634-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2f634-127">Rel</span><span class="sxs-lookup"><span data-stu-id="2f634-127">Rel</span></span>](rel-element-solution_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2f634-128">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="2f634-128">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2f634-129">Spécifie la relation à un composant avec la solution que XML associé à cette solution.</span><span class="sxs-lookup"><span data-stu-id="2f634-129">Specifies the relationship to a part with the solution XML associated with this solution.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="2f634-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="2f634-130">Attributes</span></span>

|<span data-ttu-id="2f634-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2f634-131">**Attribute**</span></span>|<span data-ttu-id="2f634-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="2f634-132">**Type**</span></span>|<span data-ttu-id="2f634-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2f634-133">**Required**</span></span>|<span data-ttu-id="2f634-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="2f634-134">**Description**</span></span>|<span data-ttu-id="2f634-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2f634-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2f634-136">Nom</span><span class="sxs-lookup"><span data-stu-id="2f634-136">Name</span></span>  <br/> |<span data-ttu-id="2f634-137">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2f634-137">xsd:string</span></span>  <br/> |<span data-ttu-id="2f634-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2f634-138">required</span></span>  <br/> |<span data-ttu-id="2f634-139">Le nom de la solution.</span><span class="sxs-lookup"><span data-stu-id="2f634-139">The name of the solution.</span></span>  <br/> |<span data-ttu-id="2f634-140">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="2f634-140">Values of the xsd:string type.</span></span>  <br/> |
   

