---
title: RuleInfo_Type complexType (Visio XML)
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
# <a name="ruleinfo_type-complextype-visio-xml"></a><span data-ttu-id="bd0cd-102">RuleInfo_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="bd0cd-102">RuleInfo_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="bd0cd-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="bd0cd-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bd0cd-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="bd0cd-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-105">**Schema file**</span></span> <br/> |<span data-ttu-id="bd0cd-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="bd0cd-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="bd0cd-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-107">**Extension base**</span></span> <br/> |<span data-ttu-id="bd0cd-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="bd0cd-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bd0cd-109">Définition</span><span class="sxs-lookup"><span data-stu-id="bd0cd-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="bd0cd-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bd0cd-110">Elements and attributes</span></span>

<span data-ttu-id="bd0cd-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="bd0cd-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bd0cd-112">Child elements</span></span>

<span data-ttu-id="bd0cd-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="bd0cd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="bd0cd-114">Attributes</span></span>

|<span data-ttu-id="bd0cd-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-115">**Attribute**</span></span>|<span data-ttu-id="bd0cd-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-116">**Type**</span></span>|<span data-ttu-id="bd0cd-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-117">**Required**</span></span>|<span data-ttu-id="bd0cd-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-118">**Description**</span></span>|<span data-ttu-id="bd0cd-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="bd0cd-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="bd0cd-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="bd0cd-120">RuleID</span></span>  <br/> |<span data-ttu-id="bd0cd-121">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd0cd-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd0cd-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="bd0cd-122">required</span></span>  <br/> ||<span data-ttu-id="bd0cd-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="bd0cd-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="bd0cd-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="bd0cd-125">xsd:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="bd0cd-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="bd0cd-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="bd0cd-126">required</span></span>  <br/> ||<span data-ttu-id="bd0cd-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="bd0cd-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

