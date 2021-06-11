---
title: Élément Issues (Validation_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23544055-c554-28b7-c351-370ab9b3c96c
description: Contient tous les éléments Issue du document.
ms.openlocfilehash: dced8ab94b51535a47415794954b5b3062963ede
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542939"
---
# <a name="issues-element-validation_type-complextype-visio-xml"></a><span data-ttu-id="61161-103">Élément Issues (Validation_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="61161-103">Issues element (Validation_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="61161-104">Contient tous les éléments Issue du document.</span><span class="sxs-lookup"><span data-stu-id="61161-104">Contains all the Issue elements for the document.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="61161-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="61161-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="61161-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="61161-106">**Element type**</span></span> <br/> |[<span data-ttu-id="61161-107">Issues_Type</span><span class="sxs-lookup"><span data-stu-id="61161-107">Issues_Type</span></span>](issues_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="61161-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="61161-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="61161-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="61161-109">**Schema file**</span></span> <br/> |<span data-ttu-id="61161-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="61161-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="61161-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="61161-111">**Document parts**</span></span> <br/> |<span data-ttu-id="61161-112">validation.xml</span><span class="sxs-lookup"><span data-stu-id="61161-112">validation.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="61161-113">Définition</span><span class="sxs-lookup"><span data-stu-id="61161-113">Definition</span></span>

```XML
< xs:element name="Issues" type="Issues_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="61161-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="61161-114">Elements and attributes</span></span>

<span data-ttu-id="61161-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="61161-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="61161-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="61161-116">Parent elements</span></span>

|<span data-ttu-id="61161-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="61161-117">**Element**</span></span>|<span data-ttu-id="61161-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="61161-118">**Type**</span></span>|<span data-ttu-id="61161-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="61161-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61161-120">Valider</span><span class="sxs-lookup"><span data-stu-id="61161-120">Validation</span></span>](validation-elementvisio-xml.md) <br/> |[<span data-ttu-id="61161-121">Validation_Type</span><span class="sxs-lookup"><span data-stu-id="61161-121">Validation_Type</span></span>](validation_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61161-122">Stocke les informations relatives à la validation du diagramme pour le document.</span><span class="sxs-lookup"><span data-stu-id="61161-122">Stores information about diagram validation for the document.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="61161-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="61161-123">Child elements</span></span>

|<span data-ttu-id="61161-124">**Élément**</span><span class="sxs-lookup"><span data-stu-id="61161-124">**Element**</span></span>|<span data-ttu-id="61161-125">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="61161-125">**Type**</span></span>|<span data-ttu-id="61161-126">**Description**</span><span class="sxs-lookup"><span data-stu-id="61161-126">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="61161-127">Problème</span><span class="sxs-lookup"><span data-stu-id="61161-127">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="61161-128">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="61161-128">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="61161-129">Représente un problème de validation unique dans le document.</span><span class="sxs-lookup"><span data-stu-id="61161-129">Represents a single validation issue in the document.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="61161-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="61161-130">Attributes</span></span>

<span data-ttu-id="61161-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="61161-131">None.</span></span>
  

