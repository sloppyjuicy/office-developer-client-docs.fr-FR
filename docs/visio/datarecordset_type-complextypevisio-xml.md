---
title: DataRecordSet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 132261ae823d1749676b7bdc28cdd1cb94f6ef5b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539143"
---
# <a name="datarecordset_type-complextype-visio-xml"></a><span data-ttu-id="6fe89-102">DataRecordSet_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="6fe89-102">DataRecordSet_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="6fe89-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6fe89-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fe89-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6fe89-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6fe89-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6fe89-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6fe89-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="6fe89-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6fe89-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6fe89-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6fe89-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="6fe89-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6fe89-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6fe89-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSet_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="DataColumns"  type="DataColumns_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="PrimaryKey"  type="PrimaryKey_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RowMap"  type="RowMap_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="RefreshConflict"  type="RefreshConflict_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
    <xs:element name="AutoLinkComparison"  type="AutoLinkComparison_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ConnectionID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="Options"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="TimeRefreshed"
  type="xsd:dateTime"
    />
    <xs:attribute name="NextRowID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="RowOrder"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshOverwriteAll"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshNoReconciliationUI"
  type="xsd:boolean"
    />
    <xs:attribute name="RefreshInterval"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ReplaceLinks"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Checksum"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6fe89-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6fe89-110">Elements and attributes</span></span>

<span data-ttu-id="6fe89-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="6fe89-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6fe89-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6fe89-112">Child elements</span></span>

|<span data-ttu-id="6fe89-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6fe89-113">**Element**</span></span>|<span data-ttu-id="6fe89-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="6fe89-114">**Type**</span></span>|<span data-ttu-id="6fe89-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6fe89-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6fe89-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="6fe89-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6fe89-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="6fe89-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6fe89-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="6fe89-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6fe89-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="6fe89-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6fe89-124">Rel</span><span class="sxs-lookup"><span data-stu-id="6fe89-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="6fe89-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="6fe89-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6fe89-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="6fe89-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6fe89-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="6fe89-128">Attributes</span></span>

|<span data-ttu-id="6fe89-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6fe89-129">**Attribute**</span></span>|<span data-ttu-id="6fe89-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="6fe89-130">**Type**</span></span>|<span data-ttu-id="6fe89-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6fe89-131">**Required**</span></span>|<span data-ttu-id="6fe89-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="6fe89-132">**Description**</span></span>|<span data-ttu-id="6fe89-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6fe89-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6fe89-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="6fe89-134">Checksum</span></span>  <br/> |<span data-ttu-id="6fe89-135">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-136">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-138">Commande</span><span class="sxs-lookup"><span data-stu-id="6fe89-138">Command</span></span>  <br/> |<span data-ttu-id="6fe89-139">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fe89-139">xsd:string</span></span>  <br/> |<span data-ttu-id="6fe89-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-140">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-141">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6fe89-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-142">ConnectionID</span><span class="sxs-lookup"><span data-stu-id="6fe89-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="6fe89-143">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-144">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-146">ID</span><span class="sxs-lookup"><span data-stu-id="6fe89-146">ID</span></span>  <br/> |<span data-ttu-id="6fe89-147">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6fe89-148">required</span></span>  <br/> ||<span data-ttu-id="6fe89-149">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-150">Nom</span><span class="sxs-lookup"><span data-stu-id="6fe89-150">Name</span></span>  <br/> |<span data-ttu-id="6fe89-151">xsd:string</span><span class="sxs-lookup"><span data-stu-id="6fe89-151">xsd:string</span></span>  <br/> |<span data-ttu-id="6fe89-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-152">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-153">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="6fe89-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="6fe89-154">NextRowID</span></span>  <br/> |<span data-ttu-id="6fe89-155">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-156">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-158">Options</span><span class="sxs-lookup"><span data-stu-id="6fe89-158">Options</span></span>  <br/> |<span data-ttu-id="6fe89-159">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-160">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="6fe89-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="6fe89-163">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-164">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-165">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-166">RefreshNoRecon conférencetionUI</span><span class="sxs-lookup"><span data-stu-id="6fe89-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="6fe89-167">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6fe89-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6fe89-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-168">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-169">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6fe89-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="6fe89-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="6fe89-171">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6fe89-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6fe89-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-172">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-173">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6fe89-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="6fe89-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="6fe89-175">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6fe89-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6fe89-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-176">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-177">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6fe89-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="6fe89-178">RowOrder</span></span>  <br/> |<span data-ttu-id="6fe89-179">xsd:boolean</span><span class="sxs-lookup"><span data-stu-id="6fe89-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="6fe89-180">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-180">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-181">Valeurs du type xsd:boolean.</span><span class="sxs-lookup"><span data-stu-id="6fe89-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="6fe89-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="6fe89-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="6fe89-183">xsd:dateTime</span><span class="sxs-lookup"><span data-stu-id="6fe89-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="6fe89-184">facultatif</span><span class="sxs-lookup"><span data-stu-id="6fe89-184">optional</span></span>  <br/> ||<span data-ttu-id="6fe89-185">Valeurs du type xsd:dateTime.</span><span class="sxs-lookup"><span data-stu-id="6fe89-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

