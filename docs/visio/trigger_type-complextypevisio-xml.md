---
title: ComplexType Trigger_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: 53a9efabe698e6b9c98c0471b97551c8ea2406da
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541896"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="18075-102">ComplexType Trigger_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="18075-102">Trigger_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="18075-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="18075-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="18075-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="18075-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="18075-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="18075-105">**Schema file**</span></span> <br/> |<span data-ttu-id="18075-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="18075-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="18075-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="18075-107">**Extension base**</span></span> <br/> |<span data-ttu-id="18075-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="18075-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="18075-109">Définition</span><span class="sxs-lookup"><span data-stu-id="18075-109">Definition</span></span>

```XML
          <xs:complexType name="Trigger_Type">
          
          <xs:sequence>
    <xs:element name="RefBy"  type="RefBy_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="N"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="18075-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="18075-110">Elements and attributes</span></span>

<span data-ttu-id="18075-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="18075-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="18075-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="18075-112">Child elements</span></span>

|<span data-ttu-id="18075-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="18075-113">**Element**</span></span>|<span data-ttu-id="18075-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="18075-114">**Type**</span></span>|<span data-ttu-id="18075-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="18075-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="18075-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="18075-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="18075-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="18075-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="18075-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="18075-118">Attributes</span></span>

|<span data-ttu-id="18075-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="18075-119">**Attribute**</span></span>|<span data-ttu-id="18075-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="18075-120">**Type**</span></span>|<span data-ttu-id="18075-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="18075-121">**Required**</span></span>|<span data-ttu-id="18075-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="18075-122">**Description**</span></span>|<span data-ttu-id="18075-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="18075-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="18075-124">N</span><span class="sxs-lookup"><span data-stu-id="18075-124">N</span></span>  <br/> |<span data-ttu-id="18075-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="18075-125">xsd:string</span></span>  <br/> |<span data-ttu-id="18075-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="18075-126">required</span></span>  <br/> ||<span data-ttu-id="18075-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="18075-127">Values of the xsd:string type.</span></span>  <br/> |
   

