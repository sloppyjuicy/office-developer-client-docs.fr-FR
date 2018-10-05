---
title: type complexe fld_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f680eb55-2dbb-a7b9-0879-6e91576983f3
ms.openlocfilehash: 2b1ecb21090658e1d2b042ac0f7e394d929d43c1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390603"
---
# <a name="fldtype-complextype-visio-xml"></a><span data-ttu-id="0c5a1-102">type complexe fld_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="0c5a1-102">fld_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="0c5a1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="0c5a1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0c5a1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="0c5a1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="0c5a1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="0c5a1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="0c5a1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="0c5a1-108">XSD : String</span><span class="sxs-lookup"><span data-stu-id="0c5a1-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0c5a1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="0c5a1-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="0c5a1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="0c5a1-110">Elements and attributes</span></span>

<span data-ttu-id="0c5a1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0c5a1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0c5a1-112">Child elements</span></span>

<span data-ttu-id="0c5a1-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0c5a1-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="0c5a1-114">Attributes</span></span>

|<span data-ttu-id="0c5a1-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-115">**Attribute**</span></span>|<span data-ttu-id="0c5a1-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-116">**Type**</span></span>|<span data-ttu-id="0c5a1-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-117">**Required**</span></span>|<span data-ttu-id="0c5a1-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-118">**Description**</span></span>|<span data-ttu-id="0c5a1-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="0c5a1-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0c5a1-120">IX</span><span class="sxs-lookup"><span data-stu-id="0c5a1-120">IX</span></span>  <br/> |<span data-ttu-id="0c5a1-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="0c5a1-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="0c5a1-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="0c5a1-122">required</span></span>  <br/> ||<span data-ttu-id="0c5a1-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="0c5a1-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

