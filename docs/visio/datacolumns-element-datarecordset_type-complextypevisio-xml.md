---
title: DataColumns, élément (DataRecordSet_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contient tous les éléments dans un jeu d’enregistrements de données DataColumn.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382518"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="7d108-103">DataColumns, élément (DataRecordSet_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7d108-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="7d108-104">Contient tous les éléments dans un jeu d’enregistrements de données **DataColumn** .</span><span class="sxs-lookup"><span data-stu-id="7d108-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="7d108-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="7d108-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7d108-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="7d108-106">**Element type**</span></span> <br/> |[<span data-ttu-id="7d108-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="7d108-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="7d108-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7d108-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="7d108-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7d108-109">**Schema file**</span></span> <br/> |<span data-ttu-id="7d108-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="7d108-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="7d108-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="7d108-111">**Document parts**</span></span> <br/> |<span data-ttu-id="7d108-112">recordsets.Xml</span><span class="sxs-lookup"><span data-stu-id="7d108-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7d108-113">Définition</span><span class="sxs-lookup"><span data-stu-id="7d108-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7d108-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7d108-114">Elements and attributes</span></span>

<span data-ttu-id="7d108-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7d108-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="7d108-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="7d108-116">Parent elements</span></span>

|<span data-ttu-id="7d108-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7d108-117">**Element**</span></span>|<span data-ttu-id="7d108-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="7d108-118">**Type**</span></span>|<span data-ttu-id="7d108-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d108-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d108-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="7d108-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d108-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="7d108-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7d108-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="7d108-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7d108-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7d108-123">Child elements</span></span>

|<span data-ttu-id="7d108-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7d108-124">**Element**</span></span>|<span data-ttu-id="7d108-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="7d108-125">**Type**</span></span>|<span data-ttu-id="7d108-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d108-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7d108-127">DataColumn</span><span class="sxs-lookup"><span data-stu-id="7d108-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7d108-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="7d108-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="7d108-129">Définit comment une colonne de données apparaît dans la fenêtre **Données externes** dans l’interface utilisateur Visio et qualifiant les données dans la colonne en définissant son type de données et de la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="7d108-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="7d108-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="7d108-130">Attributes</span></span>

|<span data-ttu-id="7d108-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7d108-131">**Attribute**</span></span>|<span data-ttu-id="7d108-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="7d108-132">**Type**</span></span>|<span data-ttu-id="7d108-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7d108-133">**Required**</span></span>|<span data-ttu-id="7d108-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d108-134">**Description**</span></span>|<span data-ttu-id="7d108-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7d108-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7d108-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="7d108-136">SortAsc</span></span>  <br/> |<span data-ttu-id="7d108-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="7d108-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7d108-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="7d108-138">optional</span></span>  <br/> |<span data-ttu-id="7d108-139">La colonne sur lequel trier les données.</span><span class="sxs-lookup"><span data-stu-id="7d108-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="7d108-140">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="7d108-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7d108-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="7d108-141">SortColumn</span></span>  <br/> |<span data-ttu-id="7d108-142">XSD : String</span><span class="sxs-lookup"><span data-stu-id="7d108-142">xsd:string</span></span>  <br/> |<span data-ttu-id="7d108-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="7d108-143">optional</span></span>  <br/> |<span data-ttu-id="7d108-144">Si le tri de la colonne **SortColumn** (1) par ordre croissant ou décroissant (0).</span><span class="sxs-lookup"><span data-stu-id="7d108-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="7d108-145">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="7d108-145">Values of the xsd:string type.</span></span>  <br/> |
   

