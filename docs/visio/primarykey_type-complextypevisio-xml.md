---
title: PrimaryKey_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2e8b1a8238133bf579dadf80363a70be949f48d2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538794"
---
# <a name="primarykey_type-complextype-visio-xml"></a><span data-ttu-id="4db6f-102">PrimaryKey_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="4db6f-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="4db6f-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4db6f-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4db6f-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="4db6f-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4db6f-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4db6f-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4db6f-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4db6f-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4db6f-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4db6f-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4db6f-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="4db6f-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4db6f-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4db6f-109">Definition</span></span>

```XML
          <xs:complexType name="PrimaryKey_Type">
          
          <xs:sequence>
    <xs:element name="RowKeyValue"  type="RowKeyValue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4db6f-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4db6f-110">Elements and attributes</span></span>

<span data-ttu-id="4db6f-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="4db6f-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4db6f-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4db6f-112">Child elements</span></span>

|<span data-ttu-id="4db6f-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="4db6f-113">**Element**</span></span>|<span data-ttu-id="4db6f-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="4db6f-114">**Type**</span></span>|<span data-ttu-id="4db6f-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="4db6f-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="4db6f-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="4db6f-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="4db6f-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="4db6f-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="4db6f-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="4db6f-118">Attributes</span></span>

|<span data-ttu-id="4db6f-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4db6f-119">**Attribute**</span></span>|<span data-ttu-id="4db6f-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="4db6f-120">**Type**</span></span>|<span data-ttu-id="4db6f-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4db6f-121">**Required**</span></span>|<span data-ttu-id="4db6f-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="4db6f-122">**Description**</span></span>|<span data-ttu-id="4db6f-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4db6f-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4db6f-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="4db6f-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="4db6f-125">xsd:string</span><span class="sxs-lookup"><span data-stu-id="4db6f-125">xsd:string</span></span>  <br/> |<span data-ttu-id="4db6f-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4db6f-126">required</span></span>  <br/> ||<span data-ttu-id="4db6f-127">Valeurs du type xsd:string.</span><span class="sxs-lookup"><span data-stu-id="4db6f-127">Values of the xsd:string type.</span></span>  <br/> |
   

