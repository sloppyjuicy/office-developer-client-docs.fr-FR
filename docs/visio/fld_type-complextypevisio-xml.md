---
title: fld_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 5651a0b0a2d09e3fbbdb0d1dbf66f1be3d374c12
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539599"
---
# <a name="fld_type-complextype-visio-xml"></a><span data-ttu-id="c21a5-102">fld_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c21a5-102">fld_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c21a5-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c21a5-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c21a5-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c21a5-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c21a5-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c21a5-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c21a5-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c21a5-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c21a5-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c21a5-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c21a5-108">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c21a5-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c21a5-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c21a5-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c21a5-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c21a5-110">Elements and attributes</span></span>

<span data-ttu-id="c21a5-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c21a5-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c21a5-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c21a5-112">Child elements</span></span>

<span data-ttu-id="c21a5-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c21a5-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c21a5-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="c21a5-114">Attributes</span></span>

|<span data-ttu-id="c21a5-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c21a5-115">**Attribute**</span></span>|<span data-ttu-id="c21a5-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="c21a5-116">**Type**</span></span>|<span data-ttu-id="c21a5-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c21a5-117">**Required**</span></span>|<span data-ttu-id="c21a5-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="c21a5-118">**Description**</span></span>|<span data-ttu-id="c21a5-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c21a5-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c21a5-120">IX</span><span class="sxs-lookup"><span data-stu-id="c21a5-120">IX</span></span>  <br/> |<span data-ttu-id="c21a5-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="c21a5-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="c21a5-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c21a5-122">required</span></span>  <br/> ||<span data-ttu-id="c21a5-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="c21a5-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

