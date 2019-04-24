---
title: ComplexType DataColumns_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344596"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="f9823-102">ComplexType DataColumns_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f9823-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f9823-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f9823-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9823-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f9823-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f9823-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f9823-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f9823-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f9823-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f9823-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f9823-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f9823-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f9823-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f9823-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f9823-109">Definition</span></span>

```XML
          <xs:complexType name="DataColumns_Type">
          
          <xs:sequence>
    <xs:element name="DataColumn"  type="DataColumn_Type"
     minOccurs="1"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="SortColumn"
  type="xsd:string"
    />
    <xs:attribute name="SortAsc"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f9823-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f9823-110">Elements and attributes</span></span>

<span data-ttu-id="f9823-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f9823-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f9823-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f9823-112">Child elements</span></span>

|<span data-ttu-id="f9823-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f9823-113">**Element**</span></span>|<span data-ttu-id="f9823-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="f9823-114">**Type**</span></span>|<span data-ttu-id="f9823-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9823-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f9823-116">Nommée</span><span class="sxs-lookup"><span data-stu-id="f9823-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f9823-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="f9823-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f9823-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="f9823-118">Attributes</span></span>

|<span data-ttu-id="f9823-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f9823-119">**Attribute**</span></span>|<span data-ttu-id="f9823-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="f9823-120">**Type**</span></span>|<span data-ttu-id="f9823-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f9823-121">**Required**</span></span>|<span data-ttu-id="f9823-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9823-122">**Description**</span></span>|<span data-ttu-id="f9823-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f9823-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f9823-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="f9823-124">SortAsc</span></span>  <br/> |<span data-ttu-id="f9823-125">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="f9823-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="f9823-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="f9823-126">optional</span></span>  <br/> ||<span data-ttu-id="f9823-127">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="f9823-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="f9823-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="f9823-128">SortColumn</span></span>  <br/> |<span data-ttu-id="f9823-129">xsd: String</span><span class="sxs-lookup"><span data-stu-id="f9823-129">xsd:string</span></span>  <br/> |<span data-ttu-id="f9823-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="f9823-130">optional</span></span>  <br/> ||<span data-ttu-id="f9823-131">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="f9823-131">Values of the xsd:string type.</span></span>  <br/> |
   

