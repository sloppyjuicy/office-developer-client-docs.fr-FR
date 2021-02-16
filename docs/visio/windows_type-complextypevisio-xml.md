---
title: Windows_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: b8d8ed39637bdd692b2ba113525f40a3f91ffc9c
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538437"
---
# <a name="windows_type-complextype-visio-xml"></a><span data-ttu-id="f74c2-102">Windows_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="f74c2-102">Windows_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="f74c2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f74c2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f74c2-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f74c2-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f74c2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f74c2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f74c2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="f74c2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f74c2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f74c2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f74c2-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f74c2-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f74c2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f74c2-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f74c2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f74c2-110">Elements and attributes</span></span>

<span data-ttu-id="f74c2-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="f74c2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f74c2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f74c2-112">Child elements</span></span>

|<span data-ttu-id="f74c2-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f74c2-113">**Element**</span></span>|<span data-ttu-id="f74c2-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="f74c2-114">**Type**</span></span>|<span data-ttu-id="f74c2-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="f74c2-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f74c2-116">Window</span><span class="sxs-lookup"><span data-stu-id="f74c2-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f74c2-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="f74c2-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="f74c2-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="f74c2-118">Attributes</span></span>

|<span data-ttu-id="f74c2-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f74c2-119">**Attribute**</span></span>|<span data-ttu-id="f74c2-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="f74c2-120">**Type**</span></span>|<span data-ttu-id="f74c2-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f74c2-121">**Required**</span></span>|<span data-ttu-id="f74c2-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="f74c2-122">**Description**</span></span>|<span data-ttu-id="f74c2-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f74c2-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f74c2-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="f74c2-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="f74c2-125">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f74c2-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f74c2-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="f74c2-126">optional</span></span>  <br/> ||<span data-ttu-id="f74c2-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f74c2-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="f74c2-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="f74c2-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="f74c2-129">xsd:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="f74c2-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="f74c2-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="f74c2-130">optional</span></span>  <br/> ||<span data-ttu-id="f74c2-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="f74c2-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

