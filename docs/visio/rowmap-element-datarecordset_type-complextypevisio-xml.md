---
title: Élément RowMap (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Mapie une ligne de data-recordset à une forme.
ms.openlocfilehash: 178ceb06d64bfc9ef50f75dd22f8bd94f09f5c33
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540769"
---
# <a name="rowmap-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="fae6a-103">Élément RowMap (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="fae6a-103">RowMap element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="fae6a-104">Mapie une ligne de data-recordset à une forme.</span><span class="sxs-lookup"><span data-stu-id="fae6a-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fae6a-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="fae6a-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fae6a-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fae6a-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fae6a-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="fae6a-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fae6a-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fae6a-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fae6a-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fae6a-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fae6a-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="fae6a-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fae6a-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="fae6a-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fae6a-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="fae6a-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fae6a-113">Définition</span><span class="sxs-lookup"><span data-stu-id="fae6a-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fae6a-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fae6a-114">Elements and attributes</span></span>

<span data-ttu-id="fae6a-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="fae6a-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fae6a-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fae6a-116">Parent elements</span></span>

****

|<span data-ttu-id="fae6a-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fae6a-117">**Element**</span></span>|<span data-ttu-id="fae6a-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="fae6a-118">**Type**</span></span>|<span data-ttu-id="fae6a-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fae6a-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fae6a-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="fae6a-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fae6a-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="fae6a-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fae6a-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="fae6a-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fae6a-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fae6a-123">Child elements</span></span>

<span data-ttu-id="fae6a-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fae6a-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fae6a-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="fae6a-125">Attributes</span></span>

|<span data-ttu-id="fae6a-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="fae6a-126">**Attribute**</span></span>|<span data-ttu-id="fae6a-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="fae6a-127">**Type**</span></span>|<span data-ttu-id="fae6a-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="fae6a-128">**Required**</span></span>|<span data-ttu-id="fae6a-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="fae6a-129">**Description**</span></span>|<span data-ttu-id="fae6a-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="fae6a-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="fae6a-131">PageID</span><span class="sxs-lookup"><span data-stu-id="fae6a-131">PageID</span></span>  <br/> |<span data-ttu-id="fae6a-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fae6a-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fae6a-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fae6a-133">required</span></span>  <br/> |<span data-ttu-id="fae6a-134">ID de page de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**.</span><span class="sxs-lookup"><span data-stu-id="fae6a-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="fae6a-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fae6a-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fae6a-136">RowID</span><span class="sxs-lookup"><span data-stu-id="fae6a-136">RowID</span></span>  <br/> |<span data-ttu-id="fae6a-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fae6a-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fae6a-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fae6a-138">required</span></span>  <br/> |<span data-ttu-id="fae6a-139">ID de ligne de la ligne, unique dans le recordset de données.</span><span class="sxs-lookup"><span data-stu-id="fae6a-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="fae6a-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fae6a-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="fae6a-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="fae6a-141">ShapeID</span></span>  <br/> |<span data-ttu-id="fae6a-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fae6a-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="fae6a-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="fae6a-143">required</span></span>  <br/> |<span data-ttu-id="fae6a-144">ID de forme de la forme liée aux données dans la ligne du data-recordset identifiée par **RowID**.</span><span class="sxs-lookup"><span data-stu-id="fae6a-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="fae6a-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="fae6a-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

