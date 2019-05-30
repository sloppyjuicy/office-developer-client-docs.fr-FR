---
title: Élément REL (Page_Type complexType) (XML Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Spécifie une relation avec le code XML de la page correspondante.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542778"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="ac27d-103">Élément REL (Page_Type complexType) (XML Visio)</span><span class="sxs-lookup"><span data-stu-id="ac27d-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="ac27d-104">Spécifie une relation avec le code XML de la page correspondante.</span><span class="sxs-lookup"><span data-stu-id="ac27d-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ac27d-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ac27d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ac27d-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ac27d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ac27d-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ac27d-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ac27d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ac27d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ac27d-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ac27d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ac27d-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ac27d-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ac27d-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ac27d-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ac27d-112">pages. xml, Masters. xml, recordsets. xml, page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="ac27d-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ac27d-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ac27d-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ac27d-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ac27d-114">Elements and attributes</span></span>

<span data-ttu-id="ac27d-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ac27d-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ac27d-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ac27d-116">Parent elements</span></span>

|<span data-ttu-id="ac27d-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ac27d-117">**Element**</span></span>|<span data-ttu-id="ac27d-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ac27d-118">**Type**</span></span>|<span data-ttu-id="ac27d-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac27d-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ac27d-120">Page</span><span class="sxs-lookup"><span data-stu-id="ac27d-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ac27d-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="ac27d-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ac27d-122">Spécifie une instance de code XML de page stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="ac27d-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ac27d-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ac27d-123">Child elements</span></span>

<span data-ttu-id="ac27d-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ac27d-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ac27d-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="ac27d-125">Attributes</span></span>

|<span data-ttu-id="ac27d-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ac27d-126">**Attribute**</span></span>|<span data-ttu-id="ac27d-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="ac27d-127">**Type**</span></span>|<span data-ttu-id="ac27d-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ac27d-128">**Required**</span></span>|<span data-ttu-id="ac27d-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac27d-129">**Description**</span></span>|<span data-ttu-id="ac27d-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ac27d-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ac27d-131">r:id</span><span class="sxs-lookup"><span data-stu-id="ac27d-131">r:id</span></span>  <br/> |<span data-ttu-id="ac27d-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ac27d-132">xsd:string</span></span>  <br/> <span data-ttu-id="ac27d-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="ac27d-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="ac27d-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac27d-134">required</span></span>  <br/> |<span data-ttu-id="ac27d-135">Spécifie une relation avec un composant.</span><span class="sxs-lookup"><span data-stu-id="ac27d-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="ac27d-136">«rId #»</span><span class="sxs-lookup"><span data-stu-id="ac27d-136">"rId#"</span></span>  <br/> <span data-ttu-id="ac27d-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="ac27d-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac27d-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="ac27d-138">Remarks</span></span>

<span data-ttu-id="ac27d-139">La valeur de l’attribut **r:ID** doit être un type **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="ac27d-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="ac27d-140">Le type **ST_RelationshipID** est une chaîne qui doit être au format «rId #», où le dernier caractère doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="ac27d-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="ac27d-141">Le nombre doit être unique parmi tous les éléments frères de l’élément **rel** .</span><span class="sxs-lookup"><span data-stu-id="ac27d-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="ac27d-142">Pour plus d’informations sur le type ST_RelationshipID, reportez-vous à la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="ac27d-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

