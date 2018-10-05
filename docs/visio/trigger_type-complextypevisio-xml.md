---
title: Type complexe Trigger_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 50de80d5-c846-1bdc-55e0-c688fe3d364c
ms.openlocfilehash: e34ef122a6f0a08168f838fdaeb130d68349ecb8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396329"
---
# <a name="triggertype-complextype-visio-xml"></a><span data-ttu-id="554db-102">Type complexe Trigger_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="554db-102">Trigger_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="554db-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="554db-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="554db-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="554db-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="554db-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="554db-105">**Schema file**</span></span> <br/> |<span data-ttu-id="554db-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="554db-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="554db-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="554db-107">**Extension base**</span></span> <br/> |<span data-ttu-id="554db-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="554db-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="554db-109">Définition</span><span class="sxs-lookup"><span data-stu-id="554db-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="554db-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="554db-110">Elements and attributes</span></span>

<span data-ttu-id="554db-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="554db-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="554db-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="554db-112">Child elements</span></span>

|<span data-ttu-id="554db-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="554db-113">**Element**</span></span>|<span data-ttu-id="554db-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="554db-114">**Type**</span></span>|<span data-ttu-id="554db-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="554db-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="554db-116">RefBy</span><span class="sxs-lookup"><span data-stu-id="554db-116">RefBy</span></span>](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="554db-117">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="554db-117">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="554db-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="554db-118">Attributes</span></span>

|<span data-ttu-id="554db-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="554db-119">**Attribute**</span></span>|<span data-ttu-id="554db-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="554db-120">**Type**</span></span>|<span data-ttu-id="554db-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="554db-121">**Required**</span></span>|<span data-ttu-id="554db-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="554db-122">**Description**</span></span>|<span data-ttu-id="554db-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="554db-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="554db-124">N</span><span class="sxs-lookup"><span data-stu-id="554db-124">N</span></span>  <br/> |<span data-ttu-id="554db-125">XSD : String</span><span class="sxs-lookup"><span data-stu-id="554db-125">xsd:string</span></span>  <br/> |<span data-ttu-id="554db-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="554db-126">required</span></span>  <br/> ||<span data-ttu-id="554db-127">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="554db-127">Values of the xsd:string type.</span></span>  <br/> |
   

