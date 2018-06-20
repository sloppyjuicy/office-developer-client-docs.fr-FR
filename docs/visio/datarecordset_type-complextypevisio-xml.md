---
title: Type complexe DataRecordSet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59544910-6bd5-2c89-71b3-5c8ee91a1dea
ms.openlocfilehash: 79fe048c578e8b9d8095d3fe7cd456af8ce08549
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788419"
---
# <a name="datarecordsettype-complextype-visio-xml"></a><span data-ttu-id="c9671-102">Type complexe DataRecordSet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="c9671-102">DataRecordSet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c9671-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c9671-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9671-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="c9671-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c9671-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c9671-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c9671-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c9671-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c9671-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c9671-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c9671-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="c9671-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c9671-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c9671-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c9671-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c9671-110">Elements and attributes</span></span>

<span data-ttu-id="c9671-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="c9671-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c9671-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c9671-112">Child elements</span></span>

|<span data-ttu-id="c9671-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c9671-113">**Element**</span></span>|<span data-ttu-id="c9671-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c9671-114">**Type**</span></span>|<span data-ttu-id="c9671-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9671-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c9671-116">AutoLinkComparison</span><span class="sxs-lookup"><span data-stu-id="c9671-116">AutoLinkComparison</span></span>](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-117">AutoLinkComparison_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-117">AutoLinkComparison_Type</span></span>](autolinkcomparison_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9671-118">DataColumns</span><span class="sxs-lookup"><span data-stu-id="c9671-118">DataColumns</span></span>](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-119">DataColumns_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-119">DataColumns_Type</span></span>](datacolumns_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9671-120">PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c9671-120">PrimaryKey</span></span>](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-121">PrimaryKey_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-121">PrimaryKey_Type</span></span>](primarykey_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9671-122">RefreshConflict</span><span class="sxs-lookup"><span data-stu-id="c9671-122">RefreshConflict</span></span>](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-123">RefreshConflict_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-123">RefreshConflict_Type</span></span>](refreshconflict_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9671-124">Rel</span><span class="sxs-lookup"><span data-stu-id="c9671-124">Rel</span></span>](rel-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-125">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-125">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> ||
|[<span data-ttu-id="c9671-126">RowMap</span><span class="sxs-lookup"><span data-stu-id="c9671-126">RowMap</span></span>](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c9671-127">RowMap_Type</span><span class="sxs-lookup"><span data-stu-id="c9671-127">RowMap_Type</span></span>](rowmap_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c9671-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="c9671-128">Attributes</span></span>

|<span data-ttu-id="c9671-129">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c9671-129">**Attribute**</span></span>|<span data-ttu-id="c9671-130">**Type**</span><span class="sxs-lookup"><span data-stu-id="c9671-130">**Type**</span></span>|<span data-ttu-id="c9671-131">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c9671-131">**Required**</span></span>|<span data-ttu-id="c9671-132">**Description**</span><span class="sxs-lookup"><span data-stu-id="c9671-132">**Description**</span></span>|<span data-ttu-id="c9671-133">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c9671-133">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c9671-134">Somme de contrôle</span><span class="sxs-lookup"><span data-stu-id="c9671-134">Checksum</span></span>  <br/> |<span data-ttu-id="c9671-135">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-135">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-136">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-136">optional</span></span>  <br/> ||<span data-ttu-id="c9671-137">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-137">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-138">Commande</span><span class="sxs-lookup"><span data-stu-id="c9671-138">Command</span></span>  <br/> |<span data-ttu-id="c9671-139">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c9671-139">xsd:string</span></span>  <br/> |<span data-ttu-id="c9671-140">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-140">optional</span></span>  <br/> ||<span data-ttu-id="c9671-141">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c9671-141">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9671-142">ID de connexion</span><span class="sxs-lookup"><span data-stu-id="c9671-142">ConnectionID</span></span>  <br/> |<span data-ttu-id="c9671-143">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-143">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-144">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-144">optional</span></span>  <br/> ||<span data-ttu-id="c9671-145">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-145">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-146">ID</span><span class="sxs-lookup"><span data-stu-id="c9671-146">ID</span></span>  <br/> |<span data-ttu-id="c9671-147">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-147">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-148">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c9671-148">required</span></span>  <br/> ||<span data-ttu-id="c9671-149">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-149">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-150">Nom</span><span class="sxs-lookup"><span data-stu-id="c9671-150">Name</span></span>  <br/> |<span data-ttu-id="c9671-151">XSD : String</span><span class="sxs-lookup"><span data-stu-id="c9671-151">xsd:string</span></span>  <br/> |<span data-ttu-id="c9671-152">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-152">optional</span></span>  <br/> ||<span data-ttu-id="c9671-153">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="c9671-153">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="c9671-154">NextRowID</span><span class="sxs-lookup"><span data-stu-id="c9671-154">NextRowID</span></span>  <br/> |<span data-ttu-id="c9671-155">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-155">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-156">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-156">optional</span></span>  <br/> ||<span data-ttu-id="c9671-157">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-157">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-158">Options</span><span class="sxs-lookup"><span data-stu-id="c9671-158">Options</span></span>  <br/> |<span data-ttu-id="c9671-159">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-159">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-160">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-160">optional</span></span>  <br/> ||<span data-ttu-id="c9671-161">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-161">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-162">RefreshInterval</span><span class="sxs-lookup"><span data-stu-id="c9671-162">RefreshInterval</span></span>  <br/> |<span data-ttu-id="c9671-163">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-163">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-164">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-164">optional</span></span>  <br/> ||<span data-ttu-id="c9671-165">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-165">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-166">RefreshNoReconciliationUI</span><span class="sxs-lookup"><span data-stu-id="c9671-166">RefreshNoReconciliationUI</span></span>  <br/> |<span data-ttu-id="c9671-167">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c9671-167">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c9671-168">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-168">optional</span></span>  <br/> ||<span data-ttu-id="c9671-169">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c9671-169">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c9671-170">RefreshOverwriteAll</span><span class="sxs-lookup"><span data-stu-id="c9671-170">RefreshOverwriteAll</span></span>  <br/> |<span data-ttu-id="c9671-171">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c9671-171">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c9671-172">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-172">optional</span></span>  <br/> ||<span data-ttu-id="c9671-173">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c9671-173">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c9671-174">ReplaceLinks</span><span class="sxs-lookup"><span data-stu-id="c9671-174">ReplaceLinks</span></span>  <br/> |<span data-ttu-id="c9671-175">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c9671-175">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c9671-176">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-176">optional</span></span>  <br/> ||<span data-ttu-id="c9671-177">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c9671-177">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="c9671-178">RowOrder</span><span class="sxs-lookup"><span data-stu-id="c9671-178">RowOrder</span></span>  <br/> |<span data-ttu-id="c9671-179">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="c9671-179">xsd:boolean</span></span>  <br/> |<span data-ttu-id="c9671-180">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-180">optional</span></span>  <br/> ||<span data-ttu-id="c9671-181">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="c9671-181">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="c9671-182">TimeRefreshed</span><span class="sxs-lookup"><span data-stu-id="c9671-182">TimeRefreshed</span></span>  <br/> |<span data-ttu-id="c9671-183">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="c9671-183">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="c9671-184">facultatif</span><span class="sxs-lookup"><span data-stu-id="c9671-184">optional</span></span>  <br/> ||<span data-ttu-id="c9671-185">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="c9671-185">Values of the xsd:dateTime type.</span></span>  <br/> |
   

