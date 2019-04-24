---
title: ComplexType Windows_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 5aeffa7b78c4c402d03b6a2774a2df8b339e03e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346444"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="c8c08-102">ComplexType Windows_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="c8c08-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="c8c08-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c8c08-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8c08-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c8c08-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c8c08-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c8c08-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c8c08-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="c8c08-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c8c08-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c8c08-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c8c08-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="c8c08-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c8c08-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c8c08-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c8c08-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c8c08-110">Elements and attributes</span></span>

<span data-ttu-id="c8c08-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="c8c08-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c8c08-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c8c08-112">Child elements</span></span>

|<span data-ttu-id="c8c08-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c8c08-113">**Element**</span></span>|<span data-ttu-id="c8c08-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="c8c08-114">**Type**</span></span>|<span data-ttu-id="c8c08-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8c08-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c8c08-116">Window</span><span class="sxs-lookup"><span data-stu-id="c8c08-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c8c08-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="c8c08-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c8c08-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c8c08-118">Attributes</span></span>

|<span data-ttu-id="c8c08-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c8c08-119">**Attribute**</span></span>|<span data-ttu-id="c8c08-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="c8c08-120">**Type**</span></span>|<span data-ttu-id="c8c08-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c8c08-121">**Required**</span></span>|<span data-ttu-id="c8c08-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="c8c08-122">**Description**</span></span>|<span data-ttu-id="c8c08-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c8c08-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c8c08-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="c8c08-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="c8c08-125">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c8c08-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c8c08-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="c8c08-126">optional</span></span>  <br/> ||<span data-ttu-id="c8c08-127">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c8c08-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="c8c08-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="c8c08-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="c8c08-129">xsd: unsignedShort</span><span class="sxs-lookup"><span data-stu-id="c8c08-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="c8c08-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="c8c08-130">optional</span></span>  <br/> ||<span data-ttu-id="c8c08-131">Valeurs du type xsd: unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="c8c08-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

