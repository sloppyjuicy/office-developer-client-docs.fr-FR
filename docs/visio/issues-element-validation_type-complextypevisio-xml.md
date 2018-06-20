---
title: Élément de problèmes (Validation_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contient tous les éléments de problème pour le document.
ms.openlocfilehash: 9205bf014c81aa699b8bc4a2a7412c5ce59c5fd0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788868"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="48c95-103">Élément de problèmes (Validation_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="48c95-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="48c95-104">Contient tous les éléments de problème pour le document.</span><span class="sxs-lookup"><span data-stu-id="48c95-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="48c95-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="48c95-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="48c95-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="48c95-106">**Element type**</span></span> <br/> |[<span data-ttu-id="48c95-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="48c95-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="48c95-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="48c95-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="48c95-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="48c95-109">**Schema file**</span></span> <br/> |<span data-ttu-id="48c95-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="48c95-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="48c95-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="48c95-111">**Document parts**</span></span> <br/> |<span data-ttu-id="48c95-112">validation.Xml</span><span class="sxs-lookup"><span data-stu-id="48c95-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="48c95-113">Définition</span><span class="sxs-lookup"><span data-stu-id="48c95-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="48c95-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="48c95-114">Elements and attributes</span></span>

<span data-ttu-id="48c95-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="48c95-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="48c95-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="48c95-116">Parent elements</span></span>

|<span data-ttu-id="48c95-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48c95-117">**Element**</span></span>|<span data-ttu-id="48c95-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="48c95-118">**Type**</span></span>|<span data-ttu-id="48c95-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="48c95-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48c95-120">Valider</span><span class="sxs-lookup"><span data-stu-id="48c95-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="48c95-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="48c95-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="48c95-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="48c95-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="48c95-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="48c95-123">Child elements</span></span>

|<span data-ttu-id="48c95-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="48c95-124">**Element**</span></span>|<span data-ttu-id="48c95-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="48c95-125">**Type**</span></span>|<span data-ttu-id="48c95-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="48c95-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="48c95-127">Problème</span><span class="sxs-lookup"><span data-stu-id="48c95-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="48c95-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="48c95-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="48c95-129">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="48c95-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="48c95-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="48c95-130">Attributes</span></span>

<span data-ttu-id="48c95-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="48c95-131">None.</span></span>
  

