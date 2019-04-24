---
title: ComplexType DataRecordSets_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: 1705d0ea92e278008c33321f135409373b7317fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360346"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="6c7ed-102">ComplexType DataRecordSets_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="6c7ed-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="6c7ed-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="6c7ed-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6c7ed-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="6c7ed-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-105">**Schema file**</span></span> <br/> |<span data-ttu-id="6c7ed-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="6c7ed-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="6c7ed-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-107">**Extension base**</span></span> <br/> |<span data-ttu-id="6c7ed-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="6c7ed-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6c7ed-109">Définition</span><span class="sxs-lookup"><span data-stu-id="6c7ed-109">Definition</span></span>

```XML
          <xs:complexType name="DataRecordSets_Type">
          
          <xs:sequence>
    <xs:element name="DataRecordSet"  type="DataRecordSet_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="NextID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ActiveRecordsetID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DataWindowOrder"
  type="xsd:string"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="6c7ed-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="6c7ed-110">Elements and attributes</span></span>

<span data-ttu-id="6c7ed-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6c7ed-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6c7ed-112">Child elements</span></span>

|<span data-ttu-id="6c7ed-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-113">**Element**</span></span>|<span data-ttu-id="6c7ed-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-114">**Type**</span></span>|<span data-ttu-id="6c7ed-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6c7ed-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="6c7ed-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="6c7ed-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="6c7ed-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="6c7ed-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="6c7ed-118">Attributes</span></span>

|<span data-ttu-id="6c7ed-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-119">**Attribute**</span></span>|<span data-ttu-id="6c7ed-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-120">**Type**</span></span>|<span data-ttu-id="6c7ed-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-121">**Required**</span></span>|<span data-ttu-id="6c7ed-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-122">**Description**</span></span>|<span data-ttu-id="6c7ed-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="6c7ed-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6c7ed-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="6c7ed-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="6c7ed-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c7ed-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c7ed-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c7ed-126">optional</span></span>  <br/> ||<span data-ttu-id="6c7ed-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="6c7ed-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="6c7ed-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="6c7ed-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="6c7ed-129">xsd:string</span></span>  <br/> |<span data-ttu-id="6c7ed-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="6c7ed-130">optional</span></span>  <br/> ||<span data-ttu-id="6c7ed-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="6c7ed-132">NextID</span><span class="sxs-lookup"><span data-stu-id="6c7ed-132">NextID</span></span>  <br/> |<span data-ttu-id="6c7ed-133">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="6c7ed-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="6c7ed-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c7ed-134">required</span></span>  <br/> ||<span data-ttu-id="6c7ed-135">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="6c7ed-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

