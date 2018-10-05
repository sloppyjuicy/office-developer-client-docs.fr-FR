---
title: Type complexe DataColumns_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ad003c9e-5e72-2df0-f9c5-dea20a220ab5
ms.openlocfilehash: 6d802bf646ee87f4c96b9ce041352af3cab48a16
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382378"
---
# <a name="datacolumnstype-complextype-visio-xml"></a><span data-ttu-id="b8c22-102">Type complexe DataColumns_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b8c22-102">DataColumns_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b8c22-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b8c22-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b8c22-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b8c22-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b8c22-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b8c22-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b8c22-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b8c22-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b8c22-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b8c22-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b8c22-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="b8c22-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b8c22-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b8c22-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b8c22-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b8c22-110">Elements and attributes</span></span>

<span data-ttu-id="b8c22-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b8c22-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b8c22-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b8c22-112">Child elements</span></span>

|<span data-ttu-id="b8c22-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b8c22-113">**Element**</span></span>|<span data-ttu-id="b8c22-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="b8c22-114">**Type**</span></span>|<span data-ttu-id="b8c22-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8c22-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b8c22-116">DataColumn</span><span class="sxs-lookup"><span data-stu-id="b8c22-116">DataColumn</span></span>](datacolumn-element-datacolumns_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b8c22-117">DataColumn_Type</span><span class="sxs-lookup"><span data-stu-id="b8c22-117">DataColumn_Type</span></span>](datacolumn_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b8c22-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="b8c22-118">Attributes</span></span>

|<span data-ttu-id="b8c22-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b8c22-119">**Attribute**</span></span>|<span data-ttu-id="b8c22-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="b8c22-120">**Type**</span></span>|<span data-ttu-id="b8c22-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b8c22-121">**Required**</span></span>|<span data-ttu-id="b8c22-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8c22-122">**Description**</span></span>|<span data-ttu-id="b8c22-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b8c22-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b8c22-124">SortAsc</span><span class="sxs-lookup"><span data-stu-id="b8c22-124">SortAsc</span></span>  <br/> |<span data-ttu-id="b8c22-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="b8c22-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="b8c22-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="b8c22-126">optional</span></span>  <br/> ||<span data-ttu-id="b8c22-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="b8c22-127">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="b8c22-128">SortColumn</span><span class="sxs-lookup"><span data-stu-id="b8c22-128">SortColumn</span></span>  <br/> |<span data-ttu-id="b8c22-129">XSD : String</span><span class="sxs-lookup"><span data-stu-id="b8c22-129">xsd:string</span></span>  <br/> |<span data-ttu-id="b8c22-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="b8c22-130">optional</span></span>  <br/> ||<span data-ttu-id="b8c22-131">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="b8c22-131">Values of the xsd:string type.</span></span>  <br/> |
   

