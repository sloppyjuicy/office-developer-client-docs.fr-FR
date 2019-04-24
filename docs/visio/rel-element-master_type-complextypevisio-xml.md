---
title: Rel, élément (Master_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Spécifie une relation avec le code XML principal correspondant à une partie.
ms.openlocfilehash: 82552eeab746d9675f6175b62c34cef4a9c3c418
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320005"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="ad1b8-103">Rel, élément (Master_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="ad1b8-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ad1b8-104">Spécifie une relation avec le code XML principal correspondant à une partie.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ad1b8-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="ad1b8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ad1b8-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ad1b8-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="ad1b8-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ad1b8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ad1b8-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ad1b8-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="ad1b8-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ad1b8-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-111">**Document parts**</span></span> <br/> |<span data-ttu-id="ad1b8-112">pages. xml, Masters. xml, recordsets. xml, page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="ad1b8-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ad1b8-113">Définition</span><span class="sxs-lookup"><span data-stu-id="ad1b8-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ad1b8-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ad1b8-114">Elements and attributes</span></span>

<span data-ttu-id="ad1b8-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ad1b8-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ad1b8-116">Parent elements</span></span>

|<span data-ttu-id="ad1b8-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-117">**Element**</span></span>|<span data-ttu-id="ad1b8-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-118">**Type**</span></span>|<span data-ttu-id="ad1b8-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ad1b8-120">Master</span><span class="sxs-lookup"><span data-stu-id="ad1b8-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ad1b8-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="ad1b8-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ad1b8-122">Spécifie une instance du code XML principal stocké dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="ad1b8-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ad1b8-123">Child elements</span></span>

<span data-ttu-id="ad1b8-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ad1b8-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="ad1b8-125">Attributes</span></span>

|<span data-ttu-id="ad1b8-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-126">**Attribute**</span></span>|<span data-ttu-id="ad1b8-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-127">**Type**</span></span>|<span data-ttu-id="ad1b8-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-128">**Required**</span></span>|<span data-ttu-id="ad1b8-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-129">**Description**</span></span>|<span data-ttu-id="ad1b8-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ad1b8-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ad1b8-131">r:ID</span><span class="sxs-lookup"><span data-stu-id="ad1b8-131">r:id</span></span>  <br/> |<span data-ttu-id="ad1b8-132">xsd: String</span><span class="sxs-lookup"><span data-stu-id="ad1b8-132">xsd:string</span></span>  <br/> <span data-ttu-id="ad1b8-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="ad1b8-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ad1b8-134">required</span></span>  <br/> |<span data-ttu-id="ad1b8-135">Spécifie une relation avec un composant.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="ad1b8-136">«rId #»</span><span class="sxs-lookup"><span data-stu-id="ad1b8-136">"rId#"</span></span>  <br/> <span data-ttu-id="ad1b8-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad1b8-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="ad1b8-138">Remarks</span></span>

<span data-ttu-id="ad1b8-139">La valeur de l'attribut **r:ID** doit être un type **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="ad1b8-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="ad1b8-140">Le type **ST_RelationshipID** est une chaîne qui doit être au format «rId #», où le dernier caractère doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="ad1b8-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="ad1b8-141">Le nombre doit être unique parmi tous les éléments frères de l'élément **rel** .</span><span class="sxs-lookup"><span data-stu-id="ad1b8-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="ad1b8-142">Pour plus d'informations sur le type ST_RelationshipID, reportez-vous à la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="ad1b8-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

