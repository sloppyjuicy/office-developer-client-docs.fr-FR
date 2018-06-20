---
title: Élément RefreshConflict (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne dans le jeu d’enregistrements de données liée à une forme qui est en conflit après l’actualisation du jeu d’enregistrements.
ms.openlocfilehash: 0bcfb38c1a9ef84fc8581476fcce13b0de32c308
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789416"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="e03a3-103">Élément RefreshConflict (DataRecordSet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="e03a3-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e03a3-104">Indique une ligne dans le jeu d’enregistrements de données liée à une forme qui est en conflit après l’actualisation du jeu d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="e03a3-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e03a3-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="e03a3-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e03a3-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e03a3-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e03a3-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="e03a3-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e03a3-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="e03a3-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e03a3-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e03a3-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e03a3-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="e03a3-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e03a3-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e03a3-111">**Document parts**</span></span> <br/> |<span data-ttu-id="e03a3-112">recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="e03a3-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e03a3-113">Définition</span><span class="sxs-lookup"><span data-stu-id="e03a3-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e03a3-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e03a3-114">Elements and attributes</span></span>

<span data-ttu-id="e03a3-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="e03a3-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e03a3-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e03a3-116">Parent elements</span></span>

|<span data-ttu-id="e03a3-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e03a3-117">**Element**</span></span>|<span data-ttu-id="e03a3-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="e03a3-118">**Type**</span></span>|<span data-ttu-id="e03a3-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="e03a3-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e03a3-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="e03a3-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e03a3-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="e03a3-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e03a3-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="e03a3-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e03a3-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e03a3-123">Child elements</span></span>

<span data-ttu-id="e03a3-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e03a3-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e03a3-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="e03a3-125">Attributes</span></span>

|<span data-ttu-id="e03a3-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e03a3-126">**Attribute**</span></span>|<span data-ttu-id="e03a3-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="e03a3-127">**Type**</span></span>|<span data-ttu-id="e03a3-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e03a3-128">**Required**</span></span>|<span data-ttu-id="e03a3-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="e03a3-129">**Description**</span></span>|<span data-ttu-id="e03a3-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e03a3-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e03a3-131">PageID</span><span class="sxs-lookup"><span data-stu-id="e03a3-131">PageID</span></span>  <br/> |<span data-ttu-id="e03a3-132">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e03a3-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e03a3-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e03a3-133">required</span></span>  <br/> |<span data-ttu-id="e03a3-134">ID de page de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="e03a3-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="e03a3-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e03a3-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e03a3-136">RowID</span><span class="sxs-lookup"><span data-stu-id="e03a3-136">RowID</span></span>  <br/> |<span data-ttu-id="e03a3-137">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e03a3-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e03a3-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e03a3-138">required</span></span>  <br/> |<span data-ttu-id="e03a3-139">L’ID de ligne d’origine de la ligne en conflit après l’actualisation de données.</span><span class="sxs-lookup"><span data-stu-id="e03a3-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="e03a3-140">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e03a3-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="e03a3-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="e03a3-141">ShapeID</span></span>  <br/> |<span data-ttu-id="e03a3-142">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="e03a3-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="e03a3-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e03a3-143">required</span></span>  <br/> |<span data-ttu-id="e03a3-144">ID de la forme de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="e03a3-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="e03a3-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="e03a3-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

