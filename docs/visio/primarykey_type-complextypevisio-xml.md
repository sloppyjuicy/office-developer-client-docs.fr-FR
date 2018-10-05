---
title: Type complexe PrimaryKey_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3396f11b-f06e-03d9-fc9d-a23e9cfccabd
ms.openlocfilehash: 679c6335d89855febd82bdeb6e9ac88f4089e1c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391366"
---
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="2a66d-102">Type complexe PrimaryKey_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2a66d-102">PrimaryKey_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="2a66d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="2a66d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a66d-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2a66d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="2a66d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2a66d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="2a66d-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="2a66d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="2a66d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="2a66d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="2a66d-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="2a66d-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2a66d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="2a66d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="2a66d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2a66d-110">Elements and attributes</span></span>

<span data-ttu-id="2a66d-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2a66d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="2a66d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2a66d-112">Child elements</span></span>

|<span data-ttu-id="2a66d-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2a66d-113">**Element**</span></span>|<span data-ttu-id="2a66d-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a66d-114">**Type**</span></span>|<span data-ttu-id="2a66d-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a66d-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2a66d-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="2a66d-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2a66d-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="2a66d-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="2a66d-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="2a66d-118">Attributes</span></span>

|<span data-ttu-id="2a66d-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2a66d-119">**Attribute**</span></span>|<span data-ttu-id="2a66d-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="2a66d-120">**Type**</span></span>|<span data-ttu-id="2a66d-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2a66d-121">**Required**</span></span>|<span data-ttu-id="2a66d-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="2a66d-122">**Description**</span></span>|<span data-ttu-id="2a66d-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2a66d-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2a66d-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="2a66d-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="2a66d-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2a66d-125">xsd:string</span></span>  <br/> |<span data-ttu-id="2a66d-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2a66d-126">required</span></span>  <br/> ||<span data-ttu-id="2a66d-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="2a66d-127">Values of the xsd:string type.</span></span>  <br/> |
   

