---
title: Élément DataColumns (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contient tous les éléments DataColumn d’un ensemble d’enregistrements de données.
ms.openlocfilehash: e42354076c5e3e34c118145e7ec7fcdbd4977372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541196"
---
# <a name="datacolumns-element-datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="81f71-103">Élément DataColumns (DataRecordSet_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="81f71-103">DataColumns element (DataRecordSet_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="81f71-104">Contient tous les **éléments DataColumn** d’un ensemble d’enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="81f71-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="81f71-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="81f71-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="81f71-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="81f71-106">**Element type**</span></span> <br/> |[<span data-ttu-id="81f71-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="81f71-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="81f71-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="81f71-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="81f71-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="81f71-109">**Schema file**</span></span> <br/> |<span data-ttu-id="81f71-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="81f71-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="81f71-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="81f71-111">**Document parts**</span></span> <br/> |<span data-ttu-id="81f71-112">recordsets.xml</span><span class="sxs-lookup"><span data-stu-id="81f71-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="81f71-113">Définition</span><span class="sxs-lookup"><span data-stu-id="81f71-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="81f71-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="81f71-114">Elements and attributes</span></span>

<span data-ttu-id="81f71-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="81f71-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="81f71-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="81f71-116">Parent elements</span></span>

|<span data-ttu-id="81f71-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="81f71-117">**Element**</span></span>|<span data-ttu-id="81f71-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="81f71-118">**Type**</span></span>|<span data-ttu-id="81f71-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="81f71-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81f71-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="81f71-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81f71-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="81f71-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="81f71-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="81f71-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="81f71-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="81f71-123">Child elements</span></span>

|<span data-ttu-id="81f71-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="81f71-124">**Element**</span></span>|<span data-ttu-id="81f71-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="81f71-125">**Type**</span></span>|<span data-ttu-id="81f71-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="81f71-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="81f71-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="81f71-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="81f71-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="81f71-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="81f71-129">Définit l’apparition d’une  colonne de données dans la fenêtre Données externes de l’interface utilisateur Visio et qualifie les données de la colonne en définissant son type de données et sa mise en forme.</span><span class="sxs-lookup"><span data-stu-id="81f71-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="81f71-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="81f71-130">Attributes</span></span>

|<span data-ttu-id="81f71-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="81f71-131">**Attribute**</span></span>|<span data-ttu-id="81f71-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="81f71-132">**Type**</span></span>|<span data-ttu-id="81f71-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="81f71-133">**Required**</span></span>|<span data-ttu-id="81f71-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="81f71-134">**Description**</span></span>|<span data-ttu-id="81f71-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="81f71-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="81f71-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="81f71-136">SortAsc</span></span>  <br/> |<span data-ttu-id="81f71-137">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="81f71-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="81f71-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="81f71-138">optional</span></span>  <br/> |<span data-ttu-id="81f71-139">Colonne sur laquelle trier les données.</span><span class="sxs-lookup"><span data-stu-id="81f71-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="81f71-140">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="81f71-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="81f71-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="81f71-141">SortColumn</span></span>  <br/> |<span data-ttu-id="81f71-142">xsd:string</span><span class="sxs-lookup"><span data-stu-id="81f71-142">xsd:string</span></span>  <br/> |<span data-ttu-id="81f71-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="81f71-143">optional</span></span>  <br/> |<span data-ttu-id="81f71-144">Indique si la colonne **TriColumn** doit être trié par ordre croissant (1) ou décroit (0).</span><span class="sxs-lookup"><span data-stu-id="81f71-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="81f71-145">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="81f71-145">Values of the xsd:string type.</span></span>  <br/> |
   

