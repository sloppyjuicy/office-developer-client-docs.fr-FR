---
title: Type complexe Windows_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386557"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="3ac72-102">Type complexe Windows_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="3ac72-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="3ac72-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="3ac72-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3ac72-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3ac72-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="3ac72-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="3ac72-105">**Schema file**</span></span> <br/> |<span data-ttu-id="3ac72-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="3ac72-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="3ac72-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="3ac72-107">**Extension base**</span></span> <br/> |<span data-ttu-id="3ac72-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="3ac72-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="3ac72-109">Définition</span><span class="sxs-lookup"><span data-stu-id="3ac72-109">Definition</span></span>

```XML
          <xs:complexType name="Windows_Type">
          
          <xs:sequence>
    <xs:element name="Window"  type="Window_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ClientWidth"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ClientHeight"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="3ac72-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="3ac72-110">Elements and attributes</span></span>

<span data-ttu-id="3ac72-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="3ac72-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="3ac72-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3ac72-112">Child elements</span></span>

|<span data-ttu-id="3ac72-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="3ac72-113">**Element**</span></span>|<span data-ttu-id="3ac72-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="3ac72-114">**Type**</span></span>|<span data-ttu-id="3ac72-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ac72-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="3ac72-116">Window</span><span class="sxs-lookup"><span data-stu-id="3ac72-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="3ac72-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="3ac72-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="3ac72-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="3ac72-118">Attributes</span></span>

|<span data-ttu-id="3ac72-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="3ac72-119">**Attribute**</span></span>|<span data-ttu-id="3ac72-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="3ac72-120">**Type**</span></span>|<span data-ttu-id="3ac72-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="3ac72-121">**Required**</span></span>|<span data-ttu-id="3ac72-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="3ac72-122">**Description**</span></span>|<span data-ttu-id="3ac72-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="3ac72-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="3ac72-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="3ac72-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="3ac72-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3ac72-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3ac72-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ac72-126">optional</span></span>  <br/> ||<span data-ttu-id="3ac72-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3ac72-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="3ac72-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="3ac72-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="3ac72-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="3ac72-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="3ac72-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="3ac72-130">optional</span></span>  <br/> ||<span data-ttu-id="3ac72-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="3ac72-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

