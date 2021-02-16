---
title: Élément RefreshConflict (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.
ms.openlocfilehash: f966ca4a9f23de7a96273615b2404041d1045652
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542834"
---
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="dcfd5-103">Élément RefreshConflict (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="dcfd5-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="dcfd5-104">Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dcfd5-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="dcfd5-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dcfd5-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-106">**Element type**</span></span> <br/> |[<span data-ttu-id="dcfd5-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="dcfd5-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="dcfd5-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="dcfd5-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-109">**Schema file**</span></span> <br/> |<span data-ttu-id="dcfd5-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="dcfd5-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="dcfd5-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-111">**Document parts**</span></span> <br/> |<span data-ttu-id="dcfd5-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="dcfd5-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="dcfd5-113">Définition</span><span class="sxs-lookup"><span data-stu-id="dcfd5-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="dcfd5-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="dcfd5-114">Elements and attributes</span></span>

<span data-ttu-id="dcfd5-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="dcfd5-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="dcfd5-116">Parent elements</span></span>

|<span data-ttu-id="dcfd5-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-117">**Element**</span></span>|<span data-ttu-id="dcfd5-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-118">**Type**</span></span>|<span data-ttu-id="dcfd5-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dcfd5-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="dcfd5-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="dcfd5-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="dcfd5-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="dcfd5-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="dcfd5-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="dcfd5-123">Child elements</span></span>

<span data-ttu-id="dcfd5-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dcfd5-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="dcfd5-125">Attributes</span></span>

|<span data-ttu-id="dcfd5-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-126">**Attribute**</span></span>|<span data-ttu-id="dcfd5-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-127">**Type**</span></span>|<span data-ttu-id="dcfd5-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-128">**Required**</span></span>|<span data-ttu-id="dcfd5-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-129">**Description**</span></span>|<span data-ttu-id="dcfd5-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="dcfd5-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="dcfd5-131">PageID</span><span class="sxs-lookup"><span data-stu-id="dcfd5-131">PageID</span></span>  <br/> |<span data-ttu-id="dcfd5-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcfd5-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcfd5-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcfd5-133">required</span></span>  <br/> |<span data-ttu-id="dcfd5-134">ID de page de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="dcfd5-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dcfd5-136">RowID</span><span class="sxs-lookup"><span data-stu-id="dcfd5-136">RowID</span></span>  <br/> |<span data-ttu-id="dcfd5-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcfd5-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcfd5-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcfd5-138">required</span></span>  <br/> |<span data-ttu-id="dcfd5-139">L’ID de ligne d’origine de la ligne est maintenant en conflit après l’actualisation des données.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="dcfd5-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="dcfd5-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="dcfd5-141">ShapeID</span></span>  <br/> |<span data-ttu-id="dcfd5-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="dcfd5-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="dcfd5-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="dcfd5-143">required</span></span>  <br/> |<span data-ttu-id="dcfd5-144">ID de forme de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="dcfd5-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="dcfd5-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

