---
title: ComplexType RowKeyValue_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e4c971f4-e3e3-11be-6b3f-45565e56cb23
ms.openlocfilehash: e629a3a38927b7497d8d4f50299dc6be1b51c37b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541721"
---
# <a name="rowkeyvaluetype-complextype-visio-xml"></a><span data-ttu-id="69e1b-102">ComplexType RowKeyValue_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="69e1b-102">RowKeyValue_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="69e1b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="69e1b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69e1b-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="69e1b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="69e1b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="69e1b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="69e1b-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="69e1b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="69e1b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="69e1b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="69e1b-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="69e1b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="69e1b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="69e1b-109">Definition</span></span>

```XML
      <xs:complexType name="RowKeyValue_Type">
    <xs:attribute name="RowID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Value"
  type="xsd:string"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="69e1b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="69e1b-110">Elements and attributes</span></span>

<span data-ttu-id="69e1b-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="69e1b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="69e1b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="69e1b-112">Child elements</span></span>

<span data-ttu-id="69e1b-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="69e1b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69e1b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="69e1b-114">Attributes</span></span>

|<span data-ttu-id="69e1b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="69e1b-115">**Attribute**</span></span>|<span data-ttu-id="69e1b-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="69e1b-116">**Type**</span></span>|<span data-ttu-id="69e1b-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="69e1b-117">**Required**</span></span>|<span data-ttu-id="69e1b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="69e1b-118">**Description**</span></span>|<span data-ttu-id="69e1b-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="69e1b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69e1b-120">RowID</span><span class="sxs-lookup"><span data-stu-id="69e1b-120">RowID</span></span>  <br/> |<span data-ttu-id="69e1b-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="69e1b-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="69e1b-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="69e1b-122">required</span></span>  <br/> ||<span data-ttu-id="69e1b-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="69e1b-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="69e1b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="69e1b-124">Value</span></span>  <br/> |<span data-ttu-id="69e1b-125">xsd: String</span><span class="sxs-lookup"><span data-stu-id="69e1b-125">xsd:string</span></span>  <br/> |<span data-ttu-id="69e1b-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="69e1b-126">required</span></span>  <br/> ||<span data-ttu-id="69e1b-127">Valeurs du type xsd: String.</span><span class="sxs-lookup"><span data-stu-id="69e1b-127">Values of the xsd:string type.</span></span>  <br/> |
   

