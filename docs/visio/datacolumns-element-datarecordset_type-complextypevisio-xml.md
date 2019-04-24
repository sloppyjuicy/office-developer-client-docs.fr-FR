---
title: DataColumns, élément (DataRecordSet_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 34e25349-d0fa-b3a0-425b-778184e9f58f
description: Contient tous les éléments DataColumn d'un jeu d'enregistrements de données.
ms.openlocfilehash: a7a0a8faefdb965384e435ee3a9b059a3acbc3f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345247"
---
# <a name="datacolumns-element-datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="68661-103">DataColumns, élément (DataRecordSet_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="68661-103">DataColumns element (DataRecordSet_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="68661-104">Contient tous les éléments **DataColumn** d'un jeu d'enregistrements de données.</span><span class="sxs-lookup"><span data-stu-id="68661-104">Contains all the **DataColumn** elements in a data recordset.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="68661-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="68661-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68661-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="68661-106">**Element type**</span></span> <br/> |[<span data-ttu-id="68661-107">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="68661-107">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="68661-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="68661-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="68661-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="68661-109">**Schema file**</span></span> <br/> |<span data-ttu-id="68661-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="68661-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="68661-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="68661-111">**Document parts**</span></span> <br/> |<span data-ttu-id="68661-112">recordsets. Xml</span><span class="sxs-lookup"><span data-stu-id="68661-112">recordsets.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68661-113">Définition</span><span class="sxs-lookup"><span data-stu-id="68661-113">Definition</span></span>

```XML
< xs:element name="DataColumns" type="DataColumns_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="68661-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="68661-114">Elements and attributes</span></span>

<span data-ttu-id="68661-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="68661-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="68661-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="68661-116">Parent elements</span></span>

|<span data-ttu-id="68661-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68661-117">**Element**</span></span>|<span data-ttu-id="68661-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="68661-118">**Type**</span></span>|<span data-ttu-id="68661-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="68661-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68661-120">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="68661-120">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68661-121">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="68661-121">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68661-122">Stocke, met en forme, actualise et expose dans Microsoft Visio les données qui ont fait l’objet d’une requête dans une base de données.</span><span class="sxs-lookup"><span data-stu-id="68661-122">Stores, formats, refreshes, and exposes data queried from a database in Microsoft Visio.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="68661-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="68661-123">Child elements</span></span>

|<span data-ttu-id="68661-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68661-124">**Element**</span></span>|<span data-ttu-id="68661-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="68661-125">**Type**</span></span>|<span data-ttu-id="68661-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="68661-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68661-127">Nommée</span><span class="sxs-lookup"><span data-stu-id="68661-127">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68661-128">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="68661-128">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="68661-129">Définit le mode d'affichage d'une colonne de données dans la fenêtre **données externes** de l'interface utilisateur de Visio et qualifie les données dans la colonne en définissant le type de données et la mise en forme.</span><span class="sxs-lookup"><span data-stu-id="68661-129">Defines how a data column appears in the **External Data** window in the Visio user interface and qualifies the data in the column by defining its data type and formatting.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="68661-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="68661-130">Attributes</span></span>

|<span data-ttu-id="68661-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="68661-131">**Attribute**</span></span>|<span data-ttu-id="68661-132">**Type**</span><span class="sxs-lookup"><span data-stu-id="68661-132">**Type**</span></span>|<span data-ttu-id="68661-133">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="68661-133">**Required**</span></span>|<span data-ttu-id="68661-134">**Description**</span><span class="sxs-lookup"><span data-stu-id="68661-134">**Description**</span></span>|<span data-ttu-id="68661-135">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="68661-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="68661-136">SortAsc</span><span class="sxs-lookup"><span data-stu-id="68661-136">SortAsc</span></span>  <br/> |<span data-ttu-id="68661-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="68661-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="68661-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="68661-138">optional</span></span>  <br/> |<span data-ttu-id="68661-139">Colonne sur laquelle doit s'effectuer le tri des données.</span><span class="sxs-lookup"><span data-stu-id="68661-139">The column on which to sort the data.</span></span>  <br/> |<span data-ttu-id="68661-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="68661-140">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="68661-141">SortColumn</span><span class="sxs-lookup"><span data-stu-id="68661-141">SortColumn</span></span>  <br/> |<span data-ttu-id="68661-142">xsd: String</span><span class="sxs-lookup"><span data-stu-id="68661-142">xsd:string</span></span>  <br/> |<span data-ttu-id="68661-143">facultatif</span><span class="sxs-lookup"><span data-stu-id="68661-143">optional</span></span>  <br/> |<span data-ttu-id="68661-144">Indique si la colonne **SortColumn** doit être triée par ordre croissant (1) ou décroissant (0).</span><span class="sxs-lookup"><span data-stu-id="68661-144">Whether to sort the **SortColumn** column in ascending (1) or descending (0) order.</span></span>  <br/> |<span data-ttu-id="68661-145">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="68661-145">Values of the xsd:string type.</span></span>  <br/> |
   

