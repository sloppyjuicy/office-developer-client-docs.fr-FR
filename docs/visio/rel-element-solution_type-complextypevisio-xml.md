---
title: Élément REL (Solution_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: Spécifie une relation vers un composant de la solution que XML associé à cette solution.
ms.openlocfilehash: 59d9db3f7e0897abf278a27229c07fd3942cee79
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789419"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a><span data-ttu-id="4691d-103">Élément REL (Solution_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4691d-103">Rel element (Solution_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="4691d-104">Spécifie une relation vers un composant de la solution que XML associé à cette solution.</span><span class="sxs-lookup"><span data-stu-id="4691d-104">Specifies a relationship to a part with the solution XML associated with this solution.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4691d-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="4691d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4691d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="4691d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="4691d-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="4691d-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="4691d-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4691d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="4691d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4691d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="4691d-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="4691d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="4691d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="4691d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="4691d-112">pages.XML, masters.xml, recordsets.xml, page # .xml, maître # .xml</span><span class="sxs-lookup"><span data-stu-id="4691d-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4691d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="4691d-113">Definition</span></span>

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4691d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4691d-114">Elements and attributes</span></span>

<span data-ttu-id="4691d-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4691d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="4691d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4691d-116">Parent elements</span></span>

|<span data-ttu-id="4691d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4691d-117">**Element**</span></span>|<span data-ttu-id="4691d-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="4691d-118">**Type**</span></span>|<span data-ttu-id="4691d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="4691d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4691d-120">Probl?me</span><span class="sxs-lookup"><span data-stu-id="4691d-120">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4691d-121">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="4691d-121">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="4691d-122">Spécifie une instance d’une solution que XML stocké dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="4691d-122">Specifies one instance of solution XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4691d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4691d-123">Child elements</span></span>

<span data-ttu-id="4691d-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4691d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4691d-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="4691d-125">Attributes</span></span>

|<span data-ttu-id="4691d-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4691d-126">**Attribute**</span></span>|<span data-ttu-id="4691d-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="4691d-127">**Type**</span></span>|<span data-ttu-id="4691d-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4691d-128">**Required**</span></span>|<span data-ttu-id="4691d-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="4691d-129">**Description**</span></span>|<span data-ttu-id="4691d-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4691d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4691d-131">r : id</span><span class="sxs-lookup"><span data-stu-id="4691d-131">r:id</span></span>  <br/> |<span data-ttu-id="4691d-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4691d-132">xsd:string</span></span>  <br/> <span data-ttu-id="4691d-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="4691d-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="4691d-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4691d-134">required</span></span>  <br/> |<span data-ttu-id="4691d-135">Spécifie une relation à un composant.</span><span class="sxs-lookup"><span data-stu-id="4691d-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="4691d-136">« Supprimer # »</span><span class="sxs-lookup"><span data-stu-id="4691d-136">"rId#"</span></span>  <br/> <span data-ttu-id="4691d-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="4691d-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4691d-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="4691d-138">Remarks</span></span>

<span data-ttu-id="4691d-139">La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="4691d-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="4691d-140">Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="4691d-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="4691d-141">Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** .</span><span class="sxs-lookup"><span data-stu-id="4691d-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="4691d-142">Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="4691d-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

