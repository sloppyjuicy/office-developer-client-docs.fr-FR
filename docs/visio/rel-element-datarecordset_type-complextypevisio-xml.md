---
title: Élément Rel (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9148c73f-970d-61f8-b5da-e3bc748a6541
description: Spécifie une relation à un élément avec le recordset associé et les informations de liaison de données.
ms.openlocfilehash: fa93a3cbc32b6929b159b958ef2a96eafacf204f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542862"
---
# <a name="rel-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="92640-103">Élément Rel (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="92640-103">Rel element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="92640-104">Spécifie une relation à un élément avec le recordset associé et les informations de liaison de données.</span><span class="sxs-lookup"><span data-stu-id="92640-104">Specifies a relationship to a part with the associated recordset and data binding information.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92640-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="92640-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92640-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="92640-106">**Element type**</span></span> <br/> |[<span data-ttu-id="92640-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="92640-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="92640-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="92640-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="92640-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="92640-109">**Schema file**</span></span> <br/> |<span data-ttu-id="92640-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="92640-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="92640-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="92640-111">**Document parts**</span></span> <br/> |<span data-ttu-id="92640-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="92640-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92640-113">Définition</span><span class="sxs-lookup"><span data-stu-id="92640-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92640-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="92640-114">Elements and attributes</span></span>

<span data-ttu-id="92640-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="92640-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="92640-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="92640-116">Parent elements</span></span>

|<span data-ttu-id="92640-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="92640-117">**Element**</span></span>|<span data-ttu-id="92640-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="92640-118">**Type**</span></span>|<span data-ttu-id="92640-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="92640-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="92640-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="92640-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="92640-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="92640-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="92640-122">Spécifie une instance d’un recordset et des informations de liaison de données stockées dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="92640-122">Specifies one instance of a recordset and data binding information stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="92640-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="92640-123">Child elements</span></span>

<span data-ttu-id="92640-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="92640-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92640-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="92640-125">Attributes</span></span>

|<span data-ttu-id="92640-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92640-126">**Attribute**</span></span>|<span data-ttu-id="92640-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="92640-127">**Type**</span></span>|<span data-ttu-id="92640-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="92640-128">**Required**</span></span>|<span data-ttu-id="92640-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="92640-129">**Description**</span></span>|<span data-ttu-id="92640-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="92640-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92640-131">r:id</span><span class="sxs-lookup"><span data-stu-id="92640-131">r:id</span></span>  <br/> |<span data-ttu-id="92640-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="92640-132">xsd:string</span></span>  <br/> <span data-ttu-id="92640-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="92640-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="92640-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="92640-134">required</span></span>  <br/> |<span data-ttu-id="92640-135">Spécifie une relation à un élément.</span><span class="sxs-lookup"><span data-stu-id="92640-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="92640-136">« rId# »</span><span class="sxs-lookup"><span data-stu-id="92640-136">"rId#"</span></span>  <br/> <span data-ttu-id="92640-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="92640-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="92640-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="92640-138">Remarks</span></span>

<span data-ttu-id="92640-139">La valeur de **l’attribut r:id** doit être **ST_RelationshipID** type.</span><span class="sxs-lookup"><span data-stu-id="92640-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="92640-140">Le ST_RelationshipID type est une chaîne qui doit être au format « rId# **»** où le caractère final doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="92640-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="92640-141">Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel.**</span><span class="sxs-lookup"><span data-stu-id="92640-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="92640-142">Pour plus d’informations sur ST_RelationshipID type d’ST_RelationshipID, voir la spécification [ISO/IEC 29500 Part 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="92640-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

