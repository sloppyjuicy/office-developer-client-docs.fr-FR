---
title: ComplexType DataRecordSet_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 36d6cf3b34ad0aa81f7b097d6452c46679342a02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360359"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="7c034-102">ComplexType DataRecordSet_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="7c034-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7c034-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7c034-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7c034-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="7c034-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7c034-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7c034-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7c034-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="7c034-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7c034-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7c034-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7c034-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="7c034-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7c034-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7c034-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="7c034-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7c034-110">Elements and attributes</span></span>

<span data-ttu-id="7c034-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="7c034-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7c034-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7c034-112">Child elements</span></span>

|<span data-ttu-id="7c034-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7c034-113">**Element**</span></span>|<span data-ttu-id="7c034-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="7c034-114">**Type**</span></span>|<span data-ttu-id="7c034-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c034-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="7c034-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="7c034-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7c034-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="7c034-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7c034-120">Primaire</span><span class="sxs-lookup"><span data-stu-id="7c034-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7c034-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="7c034-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7c034-124">Ver</span><span class="sxs-lookup"><span data-stu-id="7c034-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="7c034-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="7c034-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="7c034-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="7c034-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="7c034-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="7c034-128">Attributes</span></span>

|<span data-ttu-id="7c034-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7c034-129">**Attribute**</span></span>|<span data-ttu-id="7c034-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="7c034-130">**Type**</span></span>|<span data-ttu-id="7c034-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7c034-131">**Required**</span></span>|<span data-ttu-id="7c034-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="7c034-132">**Description**</span></span>|<span data-ttu-id="7c034-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7c034-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7c034-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="7c034-134">Checksum</span></span>  <br/> |<span data-ttu-id="7c034-135">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-136">optional</span></span>  <br/> ||<span data-ttu-id="7c034-137">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-138">Command</span><span class="sxs-lookup"><span data-stu-id="7c034-138">Command</span></span>  <br/> |<span data-ttu-id="7c034-139">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7c034-139">xsd:string</span></span>  <br/> |<span data-ttu-id="7c034-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-140">optional</span></span>  <br/> ||<span data-ttu-id="7c034-141">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7c034-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c034-142">ID</span><span class="sxs-lookup"><span data-stu-id="7c034-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="7c034-143">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-144">optional</span></span>  <br/> ||<span data-ttu-id="7c034-145">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-146">ID</span><span class="sxs-lookup"><span data-stu-id="7c034-146">ID</span></span>  <br/> |<span data-ttu-id="7c034-147">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7c034-148">required</span></span>  <br/> ||<span data-ttu-id="7c034-149">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-150">Nom</span><span class="sxs-lookup"><span data-stu-id="7c034-150">Name</span></span>  <br/> |<span data-ttu-id="7c034-151">xsd: String</span><span class="sxs-lookup"><span data-stu-id="7c034-151">xsd:string</span></span>  <br/> |<span data-ttu-id="7c034-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-152">optional</span></span>  <br/> ||<span data-ttu-id="7c034-153">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="7c034-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="7c034-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="7c034-154">NextRowID</span></span>  <br/> |<span data-ttu-id="7c034-155">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-156">optional</span></span>  <br/> ||<span data-ttu-id="7c034-157">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-158">Options</span><span class="sxs-lookup"><span data-stu-id="7c034-158">Options</span></span>  <br/> |<span data-ttu-id="7c034-159">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-160">optional</span></span>  <br/> ||<span data-ttu-id="7c034-161">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="7c034-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="7c034-163">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-164">optional</span></span>  <br/> ||<span data-ttu-id="7c034-165">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="7c034-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="7c034-167">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c034-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c034-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-168">optional</span></span>  <br/> ||<span data-ttu-id="7c034-169">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7c034-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c034-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="7c034-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="7c034-171">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c034-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c034-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-172">optional</span></span>  <br/> ||<span data-ttu-id="7c034-173">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7c034-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c034-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="7c034-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="7c034-175">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="7c034-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="7c034-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-176">optional</span></span>  <br/> ||<span data-ttu-id="7c034-177">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="7c034-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="7c034-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="7c034-178">RowOrder</span></span>  <br/> |<span data-ttu-id="7c034-179">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="7c034-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7c034-180">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-180">optional</span></span>  <br/> ||<span data-ttu-id="7c034-181">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="7c034-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="7c034-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="7c034-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="7c034-183">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="7c034-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="7c034-184">facultatif</span><span class="sxs-lookup"><span data-stu-id="7c034-184">optional</span></span>  <br/> ||<span data-ttu-id="7c034-185">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="7c034-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

