---
title: Élément RefreshConflict (complexType DataRecordSet_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 373983f7-fc0c-95f6-7665-7ed47de82e5e
description: Indique une ligne du jeu d'enregistrements de données qui est liée à une forme en conflit après l'actualisation du jeu d'enregistrements de données.
ms.openlocfilehash: 2da6f98cf7b047564331aaf5a4167e392927a155
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360136"
---
# <a name="refreshconflict-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="cd398-103">Élément RefreshConflict (complexType DataRecordSet_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="cd398-103">RefreshConflict element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="cd398-104">Indique une ligne du jeu d'enregistrements de données qui est liée à une forme en conflit après l'actualisation du jeu d'enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="cd398-104">Indicates a row in the data recordset linked to a shape that is in conflict after the data recordset is refreshed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd398-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="cd398-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd398-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="cd398-106">**Element type**</span></span> <br/> |[<span data-ttu-id="cd398-107">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="cd398-107">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="cd398-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="cd398-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="cd398-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="cd398-109">**Schema file**</span></span> <br/> |<span data-ttu-id="cd398-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="cd398-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="cd398-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="cd398-111">**Document parts**</span></span> <br/> |<span data-ttu-id="cd398-112">recordsets. Xml</span><span class="sxs-lookup"><span data-stu-id="cd398-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="cd398-113">Définition</span><span class="sxs-lookup"><span data-stu-id="cd398-113">Definition</span></span>

```XML
< xs:element name="RefreshConflict" type="RefreshConflict_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a><span data-ttu-id="cd398-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="cd398-114">Elements and attributes</span></span>

<span data-ttu-id="cd398-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="cd398-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="cd398-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="cd398-116">Parent elements</span></span>

|<span data-ttu-id="cd398-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="cd398-117">**Element**</span></span>|<span data-ttu-id="cd398-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="cd398-118">**Type**</span></span>|<span data-ttu-id="cd398-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd398-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="cd398-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="cd398-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="cd398-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="cd398-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="cd398-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="cd398-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="cd398-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cd398-123">Child elements</span></span>

<span data-ttu-id="cd398-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="cd398-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd398-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="cd398-125">Attributes</span></span>

|<span data-ttu-id="cd398-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="cd398-126">**Attribute**</span></span>|<span data-ttu-id="cd398-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="cd398-127">**Type**</span></span>|<span data-ttu-id="cd398-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="cd398-128">**Required**</span></span>|<span data-ttu-id="cd398-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="cd398-129">**Description**</span></span>|<span data-ttu-id="cd398-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="cd398-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="cd398-131">PageID</span><span class="sxs-lookup"><span data-stu-id="cd398-131">PageID</span></span>  <br/> |<span data-ttu-id="cd398-132">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cd398-132">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cd398-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd398-133">required</span></span>  <br/> |<span data-ttu-id="cd398-134">ID de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="cd398-134">Page ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="cd398-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cd398-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cd398-136">RowID</span><span class="sxs-lookup"><span data-stu-id="cd398-136">RowID</span></span>  <br/> |<span data-ttu-id="cd398-137">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cd398-137">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cd398-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd398-138">required</span></span>  <br/> |<span data-ttu-id="cd398-139">L'ID de ligne d'origine de la ligne est maintenant en conflit après l'actualisation des données.</span><span class="sxs-lookup"><span data-stu-id="cd398-139">The original row ID of the row now in conflict after data was refreshed .</span></span>  <br/> |<span data-ttu-id="cd398-140">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cd398-140">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="cd398-141">ShapeID</span><span class="sxs-lookup"><span data-stu-id="cd398-141">ShapeID</span></span>  <br/> |<span data-ttu-id="cd398-142">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="cd398-142">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="cd398-143">obligatoire</span><span class="sxs-lookup"><span data-stu-id="cd398-143">required</span></span>  <br/> |<span data-ttu-id="cd398-144">ID de la forme impliquée dans le conflit.</span><span class="sxs-lookup"><span data-stu-id="cd398-144">Shape ID of the shape involved in the conflict.</span></span>  <br/> |<span data-ttu-id="cd398-145">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="cd398-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

