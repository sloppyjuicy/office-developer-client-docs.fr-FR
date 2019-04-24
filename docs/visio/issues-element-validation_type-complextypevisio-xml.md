---
title: Élément issues (Validation_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contient tous les éléments de problème pour le document.
ms.openlocfilehash: da3156e34af1536fab39d3d4949acac1efe67264
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339486"
---
# <a name="issues-element-validationtype-complextype-visio-xml"></a><span data-ttu-id="fcff9-103">Élément issues (Validation_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="fcff9-103">Issues element (Validation_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="fcff9-104">Contient tous les éléments de problème pour le document.</span><span class="sxs-lookup"><span data-stu-id="fcff9-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fcff9-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="fcff9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fcff9-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="fcff9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="fcff9-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="fcff9-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="fcff9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="fcff9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="fcff9-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="fcff9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="fcff9-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="fcff9-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="fcff9-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="fcff9-111">**Document parts**</span></span> <br/> |<span data-ttu-id="fcff9-112">validation. Xml</span><span class="sxs-lookup"><span data-stu-id="fcff9-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="fcff9-113">Définition</span><span class="sxs-lookup"><span data-stu-id="fcff9-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="fcff9-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="fcff9-114">Elements and attributes</span></span>

<span data-ttu-id="fcff9-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="fcff9-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="fcff9-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="fcff9-116">Parent elements</span></span>

|<span data-ttu-id="fcff9-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fcff9-117">**Element**</span></span>|<span data-ttu-id="fcff9-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcff9-118">**Type**</span></span>|<span data-ttu-id="fcff9-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcff9-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcff9-120">Valider</span><span class="sxs-lookup"><span data-stu-id="fcff9-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="fcff9-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="fcff9-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fcff9-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="fcff9-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="fcff9-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fcff9-123">Child elements</span></span>

|<span data-ttu-id="fcff9-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="fcff9-124">**Element**</span></span>|<span data-ttu-id="fcff9-125">**Type**</span><span class="sxs-lookup"><span data-stu-id="fcff9-125">**Type**</span></span>|<span data-ttu-id="fcff9-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcff9-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="fcff9-127">Problème</span><span class="sxs-lookup"><span data-stu-id="fcff9-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="fcff9-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="fcff9-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="fcff9-129">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="fcff9-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="fcff9-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="fcff9-130">Attributes</span></span>

<span data-ttu-id="fcff9-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fcff9-131">None.</span></span>
  

