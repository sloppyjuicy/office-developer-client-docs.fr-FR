---
title: Type complexe DataRecordSets_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04448cfa-7eb4-62ca-97d2-409b59a8db90
ms.openlocfilehash: b646e7a0d4e1f49aa71b162aecdd901813b01f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788422"
---
# <a name="datarecordsetstype-complextype-visio-xml"></a><span data-ttu-id="ab1ef-102">Type complexe DataRecordSets_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ab1ef-102">DataRecordSets_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="ab1ef-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="ab1ef-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab1ef-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="ab1ef-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-105">**Schema file**</span></span> <br/> |<span data-ttu-id="ab1ef-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="ab1ef-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="ab1ef-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-107">**Extension base**</span></span> <br/> |<span data-ttu-id="ab1ef-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="ab1ef-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="ab1ef-109">Définition</span><span class="sxs-lookup"><span data-stu-id="ab1ef-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="ab1ef-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ab1ef-110">Elements and attributes</span></span>

<span data-ttu-id="ab1ef-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="ab1ef-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ab1ef-112">Child elements</span></span>

|<span data-ttu-id="ab1ef-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-113">**Element**</span></span>|<span data-ttu-id="ab1ef-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-114">**Type**</span></span>|<span data-ttu-id="ab1ef-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ab1ef-116">DataRecordSet</span><span class="sxs-lookup"><span data-stu-id="ab1ef-116">DataRecordSet</span></span>](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="ab1ef-117">DataRecordSet_Type</span><span class="sxs-lookup"><span data-stu-id="ab1ef-117">DataRecordSet_Type</span></span>](datarecordset_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="ab1ef-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="ab1ef-118">Attributes</span></span>

|<span data-ttu-id="ab1ef-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-119">**Attribute**</span></span>|<span data-ttu-id="ab1ef-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-120">**Type**</span></span>|<span data-ttu-id="ab1ef-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-121">**Required**</span></span>|<span data-ttu-id="ab1ef-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-122">**Description**</span></span>|<span data-ttu-id="ab1ef-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ab1ef-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ab1ef-124">ActiveRecordsetID</span><span class="sxs-lookup"><span data-stu-id="ab1ef-124">ActiveRecordsetID</span></span>  <br/> |<span data-ttu-id="ab1ef-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ab1ef-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ab1ef-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="ab1ef-126">optional</span></span>  <br/> ||<span data-ttu-id="ab1ef-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ab1ef-128">DataWindowOrder</span><span class="sxs-lookup"><span data-stu-id="ab1ef-128">DataWindowOrder</span></span>  <br/> |<span data-ttu-id="ab1ef-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ab1ef-129">xsd:string</span></span>  <br/> |<span data-ttu-id="ab1ef-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="ab1ef-130">optional</span></span>  <br/> ||<span data-ttu-id="ab1ef-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-131">Values of the xsd:string type.</span></span>  <br/> |
|<span data-ttu-id="ab1ef-132">NextID</span><span class="sxs-lookup"><span data-stu-id="ab1ef-132">NextID</span></span>  <br/> |<span data-ttu-id="ab1ef-133">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ab1ef-133">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ab1ef-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ab1ef-134">required</span></span>  <br/> ||<span data-ttu-id="ab1ef-135">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ab1ef-135">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

