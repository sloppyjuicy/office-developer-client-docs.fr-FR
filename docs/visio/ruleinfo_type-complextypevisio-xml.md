---
title: ComplexType RuleInfo_Type (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 8e7b04e938997786cf0dc99e92057f77cfe0cf76
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541644"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="eb0d9-102">ComplexType RuleInfo_Type (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="eb0d9-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="eb0d9-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="eb0d9-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="eb0d9-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="eb0d9-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-105">**Schema file**</span></span> <br/> |<span data-ttu-id="eb0d9-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="eb0d9-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="eb0d9-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-107">**Extension base**</span></span> <br/> |<span data-ttu-id="eb0d9-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="eb0d9-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="eb0d9-109">Définition</span><span class="sxs-lookup"><span data-stu-id="eb0d9-109">Definition</span></span>

```XML
      <xs:complexType name="RuleInfo_Type">
    <xs:attribute name="RuleSetID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="RuleID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="eb0d9-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="eb0d9-110">Elements and attributes</span></span>

<span data-ttu-id="eb0d9-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="eb0d9-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="eb0d9-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="eb0d9-112">Child elements</span></span>

<span data-ttu-id="eb0d9-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="eb0d9-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="eb0d9-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="eb0d9-114">Attributes</span></span>

|<span data-ttu-id="eb0d9-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-115">**Attribute**</span></span>|<span data-ttu-id="eb0d9-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-116">**Type**</span></span>|<span data-ttu-id="eb0d9-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-117">**Required**</span></span>|<span data-ttu-id="eb0d9-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-118">**Description**</span></span>|<span data-ttu-id="eb0d9-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="eb0d9-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="eb0d9-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="eb0d9-120">RuleID</span></span>  <br/> |<span data-ttu-id="eb0d9-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb0d9-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb0d9-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="eb0d9-122">required</span></span>  <br/> ||<span data-ttu-id="eb0d9-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb0d9-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="eb0d9-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="eb0d9-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="eb0d9-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="eb0d9-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="eb0d9-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="eb0d9-126">required</span></span>  <br/> ||<span data-ttu-id="eb0d9-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="eb0d9-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

