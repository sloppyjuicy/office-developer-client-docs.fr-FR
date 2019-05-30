---
title: ComplexType PrimaryKey_Type (Visio XML)
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
# <a name="primarykeytype-complextype-visio-xml"></a><span data-ttu-id="e2967-102">ComplexType PrimaryKey_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="e2967-102">PrimaryKey_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="e2967-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="e2967-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2967-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e2967-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="e2967-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e2967-105">**Schema file**</span></span> <br/> |<span data-ttu-id="e2967-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="e2967-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="e2967-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="e2967-107">**Extension base**</span></span> <br/> |<span data-ttu-id="e2967-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="e2967-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e2967-109">Définition</span><span class="sxs-lookup"><span data-stu-id="e2967-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="e2967-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e2967-110">Elements and attributes</span></span>

<span data-ttu-id="e2967-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e2967-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="e2967-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e2967-112">Child elements</span></span>

|<span data-ttu-id="e2967-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e2967-113">**Element**</span></span>|<span data-ttu-id="e2967-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="e2967-114">**Type**</span></span>|<span data-ttu-id="e2967-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2967-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e2967-116">RowKeyValue</span><span class="sxs-lookup"><span data-stu-id="e2967-116">RowKeyValue</span></span>](rowkeyvalue-element-primarykey_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e2967-117">RowKeyValue_Type</span><span class="sxs-lookup"><span data-stu-id="e2967-117">RowKeyValue_Type</span></span>](rowkeyvalue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="e2967-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="e2967-118">Attributes</span></span>

|<span data-ttu-id="e2967-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e2967-119">**Attribute**</span></span>|<span data-ttu-id="e2967-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="e2967-120">**Type**</span></span>|<span data-ttu-id="e2967-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="e2967-121">**Required**</span></span>|<span data-ttu-id="e2967-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2967-122">**Description**</span></span>|<span data-ttu-id="e2967-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="e2967-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2967-124">ColumnNameID</span><span class="sxs-lookup"><span data-stu-id="e2967-124">ColumnNameID</span></span>  <br/> |<span data-ttu-id="e2967-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="e2967-125">xsd:string</span></span>  <br/> |<span data-ttu-id="e2967-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2967-126">required</span></span>  <br/> ||<span data-ttu-id="e2967-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="e2967-127">Values of the xsd:string type.</span></span>  <br/> |
   

