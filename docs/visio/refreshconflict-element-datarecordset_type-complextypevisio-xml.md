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
# <a name="refreshconflict-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="1beb0-103">Élément RefreshConflict (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="1beb0-103">RefreshConflict element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="1beb0-104">Indique une ligne du recordset de données liée à une forme en conflit après l’actualisation du recordset de données.</span><span class="sxs-lookup"><span data-stu-id="1beb0-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1beb0-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="1beb0-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1beb0-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="1beb0-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1beb0-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="1beb0-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="1beb0-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1beb0-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="1beb0-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1beb0-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1beb0-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="1beb0-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="1beb0-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="1beb0-111">**Document parts**</span></span> <br/> |<span data-ttu-id="1beb0-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="1beb0-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1beb0-113">Définition</span><span class="sxs-lookup"><span data-stu-id="1beb0-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1beb0-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1beb0-114">Elements and attributes</span></span>

<span data-ttu-id="1beb0-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="1beb0-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1beb0-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="1beb0-116">Parent elements</span></span>

|<span data-ttu-id="1beb0-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1beb0-117">**Element**</span></span>|<span data-ttu-id="1beb0-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="1beb0-118">**Type**</span></span>|<span data-ttu-id="1beb0-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="1beb0-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1beb0-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="1beb0-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="1beb0-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="1beb0-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="1beb0-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="1beb0-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1beb0-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1beb0-123">Child elements</span></span>

<span data-ttu-id="1beb0-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1beb0-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1beb0-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="1beb0-125">Attributes</span></span>

|<span data-ttu-id="1beb0-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1beb0-126">**Attribute**</span></span>|<span data-ttu-id="1beb0-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="1beb0-127">**Type**</span></span>|<span data-ttu-id="1beb0-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1beb0-128">**Required**</span></span>|<span data-ttu-id="1beb0-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="1beb0-129">**Description**</span></span>|<span data-ttu-id="1beb0-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1beb0-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1beb0-131">PageID</span><span class="sxs-lookup"><span data-stu-id="1beb0-131">PageID</span></span>  <br/> |<span data-ttu-id="1beb0-132">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1beb0-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1beb0-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1beb0-133">required</span></span>  <br/> |<span data-ttu-id="1beb0-134">ID de page de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="1beb0-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="1beb0-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1beb0-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1beb0-136">RowID</span><span class="sxs-lookup"><span data-stu-id="1beb0-136">RowID</span></span>  <br/> |<span data-ttu-id="1beb0-137">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1beb0-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1beb0-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1beb0-138">required</span></span>  <br/> |<span data-ttu-id="1beb0-139">L’ID de ligne d’origine de la ligne est maintenant en conflit après l’actualisation des données.</span><span class="sxs-lookup"><span data-stu-id="1beb0-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="1beb0-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1beb0-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1beb0-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1beb0-141">ShapeID</span></span>  <br/> |<span data-ttu-id="1beb0-142">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1beb0-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1beb0-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1beb0-143">required</span></span>  <br/> |<span data-ttu-id="1beb0-144">ID de forme de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="1beb0-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="1beb0-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1beb0-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

