---
title: Type complexe PrimaryKey_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 2d13ac2b6d55fdda752f16af28a0843d5a388f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789354"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="79b59-102">Type complexe PrimaryKey_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="79b59-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="79b59-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="79b59-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="79b59-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="79b59-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="79b59-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="79b59-105">**Schema file**</span></span> <br/> |<span data-ttu-id="79b59-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="79b59-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="79b59-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="79b59-107">**Extension base**</span></span> <br/> |<span data-ttu-id="79b59-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="79b59-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="79b59-109">Définition</span><span class="sxs-lookup"><span data-stu-id="79b59-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="79b59-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="79b59-110">Elements and attributes</span></span>

<span data-ttu-id="79b59-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="79b59-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="79b59-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="79b59-112">Child elements</span></span>

|<span data-ttu-id="79b59-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="79b59-113">**Element**</span></span>|<span data-ttu-id="79b59-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="79b59-114">**Type**</span></span>|<span data-ttu-id="79b59-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="79b59-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="79b59-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="79b59-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="79b59-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="79b59-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="79b59-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="79b59-118">Attributes</span></span>

|<span data-ttu-id="79b59-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="79b59-119">**Attribute**</span></span>|<span data-ttu-id="79b59-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="79b59-120">**Type**</span></span>|<span data-ttu-id="79b59-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="79b59-121">**Required**</span></span>|<span data-ttu-id="79b59-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="79b59-122">**Description**</span></span>|<span data-ttu-id="79b59-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="79b59-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="79b59-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="79b59-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="79b59-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="79b59-125">xsd:string</span></span>  <br/> |<span data-ttu-id="79b59-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="79b59-126">required</span></span>  <br/> ||<span data-ttu-id="79b59-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="79b59-127">Values of the xsd:string type.</span></span>  <br/> |
   

