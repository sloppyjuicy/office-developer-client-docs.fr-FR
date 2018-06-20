---
title: Type complexe DataColumns_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: f125bce02fab43b808608ef6b14d59dfc08a1179
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788404"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="3f41b-102">Type complexe DataColumns_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="3f41b-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3f41b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3f41b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f41b-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3f41b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3f41b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3f41b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3f41b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3f41b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3f41b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3f41b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3f41b-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="3f41b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3f41b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3f41b-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="3f41b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3f41b-110">Elements and attributes</span></span>

<span data-ttu-id="3f41b-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="3f41b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3f41b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3f41b-112">Child elements</span></span>

|<span data-ttu-id="3f41b-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3f41b-113">**Element**</span></span>|<span data-ttu-id="3f41b-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="3f41b-114">**Type**</span></span>|<span data-ttu-id="3f41b-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f41b-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3f41b-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="3f41b-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3f41b-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="3f41b-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3f41b-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="3f41b-118">Attributes</span></span>

|<span data-ttu-id="3f41b-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3f41b-119">**Attribute**</span></span>|<span data-ttu-id="3f41b-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="3f41b-120">**Type**</span></span>|<span data-ttu-id="3f41b-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3f41b-121">**Required**</span></span>|<span data-ttu-id="3f41b-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f41b-122">**Description**</span></span>|<span data-ttu-id="3f41b-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3f41b-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3f41b-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="3f41b-124">SortAsc</span></span>  <br/> |<span data-ttu-id="3f41b-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="3f41b-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="3f41b-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="3f41b-126">optional</span></span>  <br/> ||<span data-ttu-id="3f41b-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="3f41b-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="3f41b-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="3f41b-128">SortColumn</span></span>  <br/> |<span data-ttu-id="3f41b-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="3f41b-129">xsd:string</span></span>  <br/> |<span data-ttu-id="3f41b-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="3f41b-130">optional</span></span>  <br/> ||<span data-ttu-id="3f41b-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="3f41b-131">Values of the xsd:string type.</span></span>  <br/> |
   

