---
title: ComplexType RuleInfo_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9ec3a334-dd0e-acc1-2b4e-026568b6f265
ms.openlocfilehash: 0548f2b493677ab63ef75548149e709645c0cf75
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360465"
---
# <a name="ruleinfotype-complextype-visio-xml"></a><span data-ttu-id="f8c25-102">ComplexType RuleInfo_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="f8c25-102">RuleInfo_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="f8c25-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="f8c25-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f8c25-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="f8c25-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="f8c25-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f8c25-105">**Schema file**</span></span> <br/> |<span data-ttu-id="f8c25-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="f8c25-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="f8c25-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="f8c25-107">**Extension base**</span></span> <br/> |<span data-ttu-id="f8c25-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="f8c25-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f8c25-109">Définition</span><span class="sxs-lookup"><span data-stu-id="f8c25-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="f8c25-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f8c25-110">Elements and attributes</span></span>

<span data-ttu-id="f8c25-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="f8c25-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="f8c25-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f8c25-112">Child elements</span></span>

<span data-ttu-id="f8c25-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f8c25-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f8c25-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="f8c25-114">Attributes</span></span>

|<span data-ttu-id="f8c25-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f8c25-115">**Attribute**</span></span>|<span data-ttu-id="f8c25-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="f8c25-116">**Type**</span></span>|<span data-ttu-id="f8c25-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f8c25-117">**Required**</span></span>|<span data-ttu-id="f8c25-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="f8c25-118">**Description**</span></span>|<span data-ttu-id="f8c25-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f8c25-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f8c25-120">RuleID</span><span class="sxs-lookup"><span data-stu-id="f8c25-120">RuleID</span></span>  <br/> |<span data-ttu-id="f8c25-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f8c25-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8c25-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f8c25-122">required</span></span>  <br/> ||<span data-ttu-id="f8c25-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f8c25-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="f8c25-124">RuleSetID</span><span class="sxs-lookup"><span data-stu-id="f8c25-124">RuleSetID</span></span>  <br/> |<span data-ttu-id="f8c25-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="f8c25-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="f8c25-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f8c25-126">required</span></span>  <br/> ||<span data-ttu-id="f8c25-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="f8c25-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

