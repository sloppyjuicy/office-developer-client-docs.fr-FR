---
title: Élément RowMap (complexType DataRecordSet_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f90dc76b-7f0b-dead-38c0-97062a7b76a6
description: Mappe une ligne de jeu d'enregistrements de données à une forme.
ms.openlocfilehash: 2dffa49d66e8e447b4e31d771179c74eecad21da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332514"
---
# <a name="rowmap-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="d0333-103">Élément RowMap (complexType DataRecordSet_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="d0333-103">RowMap element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="d0333-104">Mappe une ligne de jeu d'enregistrements de données à une forme.</span><span class="sxs-lookup"><span data-stu-id="d0333-104">Maps a data-recordset row to a shape.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0333-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="d0333-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0333-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="d0333-106">**Element type**</span></span> <br/> |[<span data-ttu-id="d0333-107">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="d0333-107">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="d0333-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d0333-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="d0333-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="d0333-109">**Schema file**</span></span> <br/> |<span data-ttu-id="d0333-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="d0333-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="d0333-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="d0333-111">**Document parts**</span></span> <br/> |<span data-ttu-id="d0333-112">recordsets. Xml</span><span class="sxs-lookup"><span data-stu-id="d0333-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d0333-113">Définition</span><span class="sxs-lookup"><span data-stu-id="d0333-113">Definition</span></span>

```XML
< xs:element name="RowMap" type="RowMap_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="d0333-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="d0333-114">Elements and attributes</span></span>

<span data-ttu-id="d0333-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="d0333-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="d0333-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="d0333-116">Parent elements</span></span>

****

|<span data-ttu-id="d0333-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="d0333-117">**Element**</span></span>|<span data-ttu-id="d0333-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="d0333-118">**Type**</span></span>|<span data-ttu-id="d0333-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0333-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="d0333-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="d0333-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="d0333-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="d0333-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="d0333-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="d0333-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="d0333-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d0333-123">Child elements</span></span>

<span data-ttu-id="d0333-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="d0333-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0333-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="d0333-125">Attributes</span></span>

|<span data-ttu-id="d0333-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d0333-126">**Attribute**</span></span>|<span data-ttu-id="d0333-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="d0333-127">**Type**</span></span>|<span data-ttu-id="d0333-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="d0333-128">**Required**</span></span>|<span data-ttu-id="d0333-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="d0333-129">**Description**</span></span>|<span data-ttu-id="d0333-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="d0333-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d0333-131">PageID</span><span class="sxs-lookup"><span data-stu-id="d0333-131">PageID</span></span>  <br/> |<span data-ttu-id="d0333-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0333-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0333-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0333-133">required</span></span>  <br/> |<span data-ttu-id="d0333-134">ID de page de la forme liée aux données dans la ligne de jeu d'enregistrements de données identifiée par **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="d0333-134">Page ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="d0333-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d0333-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0333-136">RowID</span><span class="sxs-lookup"><span data-stu-id="d0333-136">RowID</span></span>  <br/> |<span data-ttu-id="d0333-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0333-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0333-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0333-138">required</span></span>  <br/> |<span data-ttu-id="d0333-139">ID de ligne de la ligne, unique dans le jeu d'enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="d0333-139">Row ID of the row, unique within the data recordset.</span></span>  <br/> |<span data-ttu-id="d0333-140">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d0333-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="d0333-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="d0333-141">ShapeID</span></span>  <br/> |<span data-ttu-id="d0333-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="d0333-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="d0333-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="d0333-143">required</span></span>  <br/> |<span data-ttu-id="d0333-144">ID de la forme liée aux données de la ligne de jeu d'enregistrements de données identifiée par **ROWID**.</span><span class="sxs-lookup"><span data-stu-id="d0333-144">Shape ID of the shape linked to data in the data-recordset row identified by **RowID**.</span></span>  <br/> |<span data-ttu-id="d0333-145">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="d0333-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

