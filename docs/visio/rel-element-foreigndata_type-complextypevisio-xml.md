---
title: Élément Rel (ForeignData_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7ed604ef-e001-f379-92c3-391a18f22bb3
description: Spécifie une relation entre une forme et une partie de document qui contient les données d’image associées à la forme.
ms.openlocfilehash: 5836fd306670600f65eda1f3a998ef4c5479114b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542806"
---
# <a name="rel-element-foreigndata_type-complextype-visio-xml"></a><span data-ttu-id="38242-103">Élément Rel (ForeignData_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="38242-103">Rel element (ForeignData_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="38242-104">Spécifie une relation entre une forme et une partie de document qui contient les données d’image associées à la forme.</span><span class="sxs-lookup"><span data-stu-id="38242-104">Specifies a relationship between a shape and a document part that contains the image data associated with the shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38242-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="38242-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38242-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="38242-106">**Element type**</span></span> <br/> |[<span data-ttu-id="38242-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="38242-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="38242-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38242-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="38242-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="38242-109">**Schema file**</span></span> <br/> |<span data-ttu-id="38242-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="38242-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="38242-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="38242-111">**Document parts**</span></span> <br/> |<span data-ttu-id="38242-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="38242-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38242-113">Définition</span><span class="sxs-lookup"><span data-stu-id="38242-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="38242-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="38242-114">Elements and attributes</span></span>

<span data-ttu-id="38242-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="38242-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="38242-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="38242-116">Parent elements</span></span>

|<span data-ttu-id="38242-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="38242-117">**Element**</span></span>|<span data-ttu-id="38242-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="38242-118">**Type**</span></span>|<span data-ttu-id="38242-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="38242-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38242-120">ForeignData</span><span class="sxs-lookup"><span data-stu-id="38242-120">ForeignData</span></span>](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="38242-121">ForeignData_Type</span><span class="sxs-lookup"><span data-stu-id="38242-121">ForeignData_Type</span></span>](foreigndata_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="38242-122">Spécifie une instance de données d’image stockées dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="38242-122">Specifies one instance of image data stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38242-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="38242-123">Child elements</span></span>

<span data-ttu-id="38242-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="38242-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38242-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="38242-125">Attributes</span></span>

|<span data-ttu-id="38242-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="38242-126">**Attribute**</span></span>|<span data-ttu-id="38242-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="38242-127">**Type**</span></span>|<span data-ttu-id="38242-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="38242-128">**Required**</span></span>|<span data-ttu-id="38242-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="38242-129">**Description**</span></span>|<span data-ttu-id="38242-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="38242-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38242-131">r:id</span><span class="sxs-lookup"><span data-stu-id="38242-131">r:id</span></span>  <br/> |<span data-ttu-id="38242-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="38242-132">xsd:string</span></span>  <br/> <span data-ttu-id="38242-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="38242-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="38242-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="38242-134">required</span></span>  <br/> |<span data-ttu-id="38242-135">Spécifie une relation à un élément.</span><span class="sxs-lookup"><span data-stu-id="38242-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="38242-136">« rId# »</span><span class="sxs-lookup"><span data-stu-id="38242-136">"rId#"</span></span>  <br/> <span data-ttu-id="38242-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="38242-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38242-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="38242-138">Remarks</span></span>

<span data-ttu-id="38242-139">La valeur de **l’attribut r:id** doit être **ST_RelationshipID** type.</span><span class="sxs-lookup"><span data-stu-id="38242-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="38242-140">Le ST_RelationshipID type est une chaîne qui doit être au format « rId# **»** où le caractère final doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="38242-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="38242-141">Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel.**</span><span class="sxs-lookup"><span data-stu-id="38242-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="38242-142">Pour plus d’informations sur le type ST_RelationshipID, voir la spécification [ISO/IEC 29500 Partie 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="38242-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

