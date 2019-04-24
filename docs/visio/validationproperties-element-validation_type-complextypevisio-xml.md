---
title: Élément ValidationProperties (complexType Validation_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a51a60c9-479b-7d7b-860f-bb46fc8b4d63
description: EnCapsule les propriétés liées à la validation du document.
ms.openlocfilehash: 9eccb85bd7463411d81c867eda3216d6c9a207f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355957"
---
# <a name="validationproperties-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="071bb-103">Élément ValidationProperties (complexType Validation_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="071bb-103">ValidationProperties element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="071bb-104">EnCapsule les propriétés liées à la validation du document.</span><span class="sxs-lookup"><span data-stu-id="071bb-104">Encapsulates the properties that are related to the document's validation.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="071bb-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="071bb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="071bb-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="071bb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="071bb-107">ValidationProperties_Type</span><span class="sxs-lookup"><span data-stu-id="071bb-107">ValidationProperties_Type</span></span>](validationproperties_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="071bb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="071bb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="071bb-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="071bb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="071bb-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="071bb-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="071bb-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="071bb-111">**Document parts**</span></span> <br/> |<span data-ttu-id="071bb-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="071bb-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="071bb-113">Définition</span><span class="sxs-lookup"><span data-stu-id="071bb-113">Definition</span></span>

```XML
< xs:element name="ValidationProperties" type="ValidationProperties_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="071bb-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="071bb-114">Elements and attributes</span></span>

<span data-ttu-id="071bb-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="071bb-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="071bb-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="071bb-116">Parent elements</span></span>

|<span data-ttu-id="071bb-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="071bb-117">**Element**</span></span>|<span data-ttu-id="071bb-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="071bb-118">**Type**</span></span>|<span data-ttu-id="071bb-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="071bb-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="071bb-120">Valider</span><span class="sxs-lookup"><span data-stu-id="071bb-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="071bb-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="071bb-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="071bb-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="071bb-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="071bb-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="071bb-123">Child elements</span></span>

<span data-ttu-id="071bb-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="071bb-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="071bb-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="071bb-125">Attributes</span></span>

|<span data-ttu-id="071bb-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="071bb-126">**Attribute**</span></span>|<span data-ttu-id="071bb-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="071bb-127">**Type**</span></span>|<span data-ttu-id="071bb-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="071bb-128">**Required**</span></span>|<span data-ttu-id="071bb-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="071bb-129">**Description**</span></span>|<span data-ttu-id="071bb-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="071bb-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="071bb-131">LastValidated</span><span class="sxs-lookup"><span data-stu-id="071bb-131">LastValidated</span></span>  <br/> |<span data-ttu-id="071bb-132">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="071bb-132">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="071bb-133">obligatoire</span><span class="sxs-lookup"><span data-stu-id="071bb-133">required</span></span>  <br/> |<span data-ttu-id="071bb-134">Date et heure de la dernière validation du document.</span><span class="sxs-lookup"><span data-stu-id="071bb-134">The date and time that the document was last validated.</span></span>  <br/> |<span data-ttu-id="071bb-135">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="071bb-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="071bb-136">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="071bb-136">ShowIgnored</span></span>  <br/> |<span data-ttu-id="071bb-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="071bb-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="071bb-138">obligatoire</span><span class="sxs-lookup"><span data-stu-id="071bb-138">required</span></span>  <br/> |<span data-ttu-id="071bb-139">Spécifie s'il faut afficher les problèmes de validation ignorés dans la fenêtre problèmes.</span><span class="sxs-lookup"><span data-stu-id="071bb-139">Specifies whether to show ignored validation issues in the Issues window.</span></span>  <br/> |<span data-ttu-id="071bb-140">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="071bb-140">Values of the xsd:boolean type.</span></span>  <br/> |
   

