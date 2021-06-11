---
title: Élément Rel (Page_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Spécifie une relation à un élément avec le XML de page correspondant.
ms.openlocfilehash: 19224a7057786677cdb371df887e69e8457649c6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542778"
---
# <a name="rel-element-page_type-complextype-visio-xml"></a><span data-ttu-id="336f3-103">Élément Rel (Page_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="336f3-103">Rel element (Page_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="336f3-104">Spécifie une relation à un élément avec le XML de page correspondant.</span><span class="sxs-lookup"><span data-stu-id="336f3-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="336f3-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="336f3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="336f3-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="336f3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="336f3-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="336f3-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="336f3-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="336f3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="336f3-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="336f3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="336f3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="336f3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="336f3-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="336f3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="336f3-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="336f3-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="336f3-113">Définition</span><span class="sxs-lookup"><span data-stu-id="336f3-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="336f3-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="336f3-114">Elements and attributes</span></span>

<span data-ttu-id="336f3-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="336f3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="336f3-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="336f3-116">Parent elements</span></span>

|<span data-ttu-id="336f3-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="336f3-117">**Element**</span></span>|<span data-ttu-id="336f3-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="336f3-118">**Type**</span></span>|<span data-ttu-id="336f3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="336f3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="336f3-120">Page</span><span class="sxs-lookup"><span data-stu-id="336f3-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="336f3-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="336f3-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="336f3-122">Spécifie une instance de page XML stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="336f3-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="336f3-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="336f3-123">Child elements</span></span>

<span data-ttu-id="336f3-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="336f3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="336f3-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="336f3-125">Attributes</span></span>

|<span data-ttu-id="336f3-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="336f3-126">**Attribute**</span></span>|<span data-ttu-id="336f3-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="336f3-127">**Type**</span></span>|<span data-ttu-id="336f3-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="336f3-128">**Required**</span></span>|<span data-ttu-id="336f3-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="336f3-129">**Description**</span></span>|<span data-ttu-id="336f3-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="336f3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="336f3-131">r:id</span><span class="sxs-lookup"><span data-stu-id="336f3-131">r:id</span></span>  <br/> |<span data-ttu-id="336f3-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="336f3-132">xsd:string</span></span>  <br/> <span data-ttu-id="336f3-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="336f3-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="336f3-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="336f3-134">required</span></span>  <br/> |<span data-ttu-id="336f3-135">Spécifie une relation à un élément.</span><span class="sxs-lookup"><span data-stu-id="336f3-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="336f3-136">« rId# »</span><span class="sxs-lookup"><span data-stu-id="336f3-136">"rId#"</span></span>  <br/> <span data-ttu-id="336f3-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="336f3-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="336f3-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="336f3-138">Remarks</span></span>

<span data-ttu-id="336f3-139">La valeur de **l’attribut r:id** doit être **ST_RelationshipID** type.</span><span class="sxs-lookup"><span data-stu-id="336f3-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="336f3-140">Le ST_RelationshipID type est une chaîne qui doit être au format « rId# **»** où le caractère final doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="336f3-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="336f3-141">Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel.**</span><span class="sxs-lookup"><span data-stu-id="336f3-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="336f3-142">Pour plus d’informations sur le type ST_RelationshipID, voir la spécification [ISO/IEC 29500 Partie 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="336f3-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

