---
title: Élément RefBy (Trigger_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09f2430a-184d-eaa2-2cb9-51bb24345c51
description: Spécifie une référence à une page dans le dessin.
ms.openlocfilehash: e4726a8fe49a7492cd2f7833bbcf5e6810bae18d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572430"
---
# <a name="refby-element-triggertype-complextype-visio-xml"></a><span data-ttu-id="ff59e-103">Élément RefBy (Trigger_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="ff59e-103">RefBy element (Trigger_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="ff59e-104">Spécifie une référence à une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="ff59e-104">Specifies a reference to a page in the drawing.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ff59e-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="ff59e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ff59e-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="ff59e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="ff59e-107">RefBy_Type</span><span class="sxs-lookup"><span data-stu-id="ff59e-107">RefBy_Type</span></span>](refby_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="ff59e-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="ff59e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="ff59e-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="ff59e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="ff59e-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="ff59e-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="ff59e-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="ff59e-111">**Document parts**</span></span> <br/> ||
   
## <a name="definition"></a><span data-ttu-id="ff59e-112">Définition</span><span class="sxs-lookup"><span data-stu-id="ff59e-112">Definition</span></span>

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="ff59e-113">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="ff59e-113">Elements and attributes</span></span>

<span data-ttu-id="ff59e-114">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="ff59e-114">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="ff59e-115">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="ff59e-115">Parent elements</span></span>

|<span data-ttu-id="ff59e-116">**Élément**</span><span class="sxs-lookup"><span data-stu-id="ff59e-116">**Element**</span></span>|<span data-ttu-id="ff59e-117">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff59e-117">**Type**</span></span>|<span data-ttu-id="ff59e-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff59e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="ff59e-119">Trigger</span><span class="sxs-lookup"><span data-stu-id="ff59e-119">Trigger</span></span>](trigger-elementvisio-xml.md) <br/> |[<span data-ttu-id="ff59e-120">Trigger_Type</span><span class="sxs-lookup"><span data-stu-id="ff59e-120">Trigger_Type</span></span>](trigger_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="ff59e-121">Fournit des instructions pour Microsoft Visio recalcule une relation entre les parties de document dans un fichier Visio.</span><span class="sxs-lookup"><span data-stu-id="ff59e-121">Provides instructions to Microsoft Visio to recalculate a relationship between document parts in a Visio file.</span></span>  <br/> |

   
### <a name="child-elements"></a><span data-ttu-id="ff59e-122">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="ff59e-122">Child elements</span></span>

<span data-ttu-id="ff59e-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="ff59e-123">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ff59e-124">Attributs</span><span class="sxs-lookup"><span data-stu-id="ff59e-124">Attributes</span></span>

|<span data-ttu-id="ff59e-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="ff59e-125">**Attribute**</span></span>|<span data-ttu-id="ff59e-126">**Type**</span><span class="sxs-lookup"><span data-stu-id="ff59e-126">**Type**</span></span>|<span data-ttu-id="ff59e-127">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="ff59e-127">**Required**</span></span>|<span data-ttu-id="ff59e-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff59e-128">**Description**</span></span>|<span data-ttu-id="ff59e-129">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="ff59e-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ff59e-130">ID</span><span class="sxs-lookup"><span data-stu-id="ff59e-130">ID</span></span>  <br/> |<span data-ttu-id="ff59e-131">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="ff59e-131">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="ff59e-132">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff59e-132">required</span></span>  <br/> |<span data-ttu-id="ff59e-133">Spécifie l’attribut ID d’une page dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="ff59e-133">Specifies the ID attribute of a page in the drawing.</span></span>  <br/> |<span data-ttu-id="ff59e-134">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="ff59e-134">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="ff59e-135">T</span><span class="sxs-lookup"><span data-stu-id="ff59e-135">T</span></span>  <br/> |<span data-ttu-id="ff59e-136">XSD : String</span><span class="sxs-lookup"><span data-stu-id="ff59e-136">xsd:string</span></span>  <br/> |<span data-ttu-id="ff59e-137">obligatoire</span><span class="sxs-lookup"><span data-stu-id="ff59e-137">required</span></span>  <br/> |<span data-ttu-id="ff59e-138">Spécifie le type de référence.</span><span class="sxs-lookup"><span data-stu-id="ff59e-138">Specifies the reference type.</span></span>  <br/> |<span data-ttu-id="ff59e-139">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="ff59e-139">Values of the xsd:string type.</span></span>  <br/> |
   

