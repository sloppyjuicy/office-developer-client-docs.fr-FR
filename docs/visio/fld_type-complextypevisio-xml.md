---
title: type complexe fld_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: c4ea016adea237258ba699c54bf05b902119eca1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788650"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="4987c-102">type complexe fld_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="4987c-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="4987c-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="4987c-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4987c-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="4987c-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="4987c-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="4987c-105">**Schema file**</span></span> <br/> |<span data-ttu-id="4987c-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="4987c-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="4987c-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="4987c-107">**Extension base**</span></span> <br/> |<span data-ttu-id="4987c-108">XSD : String</span><span class="sxs-lookup"><span data-stu-id="4987c-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="4987c-109">Définition</span><span class="sxs-lookup"><span data-stu-id="4987c-109">Definition</span></span>

```XML
      <xs:complexType name="fld_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="IX"
  type="xsd:unsignedInt"
     use="required"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="4987c-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="4987c-110">Elements and attributes</span></span>

<span data-ttu-id="4987c-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="4987c-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="4987c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4987c-112">Child elements</span></span>

<span data-ttu-id="4987c-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="4987c-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4987c-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4987c-114">Attributes</span></span>

|<span data-ttu-id="4987c-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4987c-115">**Attribute**</span></span>|<span data-ttu-id="4987c-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="4987c-116">**Type**</span></span>|<span data-ttu-id="4987c-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="4987c-117">**Required**</span></span>|<span data-ttu-id="4987c-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="4987c-118">**Description**</span></span>|<span data-ttu-id="4987c-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="4987c-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4987c-120">IX</span><span class="sxs-lookup"><span data-stu-id="4987c-120">IX</span></span>  <br/> |<span data-ttu-id="4987c-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="4987c-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="4987c-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="4987c-122">required</span></span>  <br/> ||<span data-ttu-id="4987c-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="4987c-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

