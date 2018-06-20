---
title: Type complexe Windows_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e8257df-4af0-aab1-a979-df9fa8a56f20
ms.openlocfilehash: 33a2acaad76543115c480b5e9a32ddba8fb0d66a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790038"
---
# <a name="windowstype-complextype-visio-xml"></a><span data-ttu-id="b07df-102">Type complexe Windows_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="b07df-102">Windows_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="b07df-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="b07df-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b07df-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="b07df-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="b07df-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="b07df-105">**Schema file**</span></span> <br/> |<span data-ttu-id="b07df-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="b07df-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="b07df-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="b07df-107">**Extension base**</span></span> <br/> |<span data-ttu-id="b07df-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="b07df-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="b07df-109">Définition</span><span class="sxs-lookup"><span data-stu-id="b07df-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="b07df-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="b07df-110">Elements and attributes</span></span>

<span data-ttu-id="b07df-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="b07df-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="b07df-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b07df-112">Child elements</span></span>

|<span data-ttu-id="b07df-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="b07df-113">**Element**</span></span>|<span data-ttu-id="b07df-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="b07df-114">**Type**</span></span>|<span data-ttu-id="b07df-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="b07df-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="b07df-116">Window</span><span class="sxs-lookup"><span data-stu-id="b07df-116">Window</span></span>](window-element-windows_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="b07df-117">Window_Type</span><span class="sxs-lookup"><span data-stu-id="b07df-117">Window_Type</span></span>](window_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="b07df-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="b07df-118">Attributes</span></span>

|<span data-ttu-id="b07df-119">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="b07df-119">**Attribute**</span></span>|<span data-ttu-id="b07df-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="b07df-120">**Type**</span></span>|<span data-ttu-id="b07df-121">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="b07df-121">**Required**</span></span>|<span data-ttu-id="b07df-122">**Description**</span><span class="sxs-lookup"><span data-stu-id="b07df-122">**Description**</span></span>|<span data-ttu-id="b07df-123">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="b07df-123">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="b07df-124">ClientHeight</span><span class="sxs-lookup"><span data-stu-id="b07df-124">ClientHeight</span></span>  <br/> |<span data-ttu-id="b07df-125">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b07df-125">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b07df-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="b07df-126">optional</span></span>  <br/> ||<span data-ttu-id="b07df-127">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b07df-127">Values of the xsd:unsignedShort type.</span></span>  <br/> |
|<span data-ttu-id="b07df-128">ClientWidth</span><span class="sxs-lookup"><span data-stu-id="b07df-128">ClientWidth</span></span>  <br/> |<span data-ttu-id="b07df-129">XSD:unsignedShort</span><span class="sxs-lookup"><span data-stu-id="b07df-129">xsd:unsignedShort</span></span>  <br/> |<span data-ttu-id="b07df-130">facultatif</span><span class="sxs-lookup"><span data-stu-id="b07df-130">optional</span></span>  <br/> ||<span data-ttu-id="b07df-131">Valeurs du type xsd:unsignedShort.</span><span class="sxs-lookup"><span data-stu-id="b07df-131">Values of the xsd:unsignedShort type.</span></span>  <br/> |
   

