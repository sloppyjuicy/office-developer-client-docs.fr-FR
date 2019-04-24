---
title: Élément ProtectMasters (complexType DocumentSettings_Type) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Indique si l'utilisateur ne peut pas créer, modifier ou supprimer des formes de base. L'utilisateur peut toujours créer de nouvelles formes à partir d'une forme de base, quelle que soit la valeur de ce paramètre.
ms.openlocfilehash: 2730fa3aa3f9f4f7529d6b939e48d3533e31e1f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314818"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="e5eb8-104">Élément ProtectMasters (complexType DocumentSettings_Type) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="e5eb8-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="e5eb8-105">Indique si l'utilisateur ne peut pas créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="e5eb8-106">L'utilisateur peut toujours créer de nouvelles formes à partir d'une forme de base, quelle que soit la valeur de ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="e5eb8-107">La plage de valeurs possibles pour cet élément est «0» ou «1».</span><span class="sxs-lookup"><span data-stu-id="e5eb8-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="e5eb8-108">La valeur «0» indique que les utilisateurs peuvent créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="e5eb8-109">La valeur «1» indique que les utilisateurs ne peuvent pas créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5eb8-110">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="e5eb8-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5eb8-111">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-111">**Element type**</span></span> <br/> |[<span data-ttu-id="e5eb8-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="e5eb8-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="e5eb8-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-113">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="e5eb8-114">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-114">**Schema file**</span></span> <br/> |<span data-ttu-id="e5eb8-115">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="e5eb8-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="e5eb8-116">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-116">**Document parts**</span></span> <br/> |<span data-ttu-id="e5eb8-117">document. Xml</span><span class="sxs-lookup"><span data-stu-id="e5eb8-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e5eb8-118">Définition</span><span class="sxs-lookup"><span data-stu-id="e5eb8-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="e5eb8-119">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="e5eb8-119">Elements and attributes</span></span>

<span data-ttu-id="e5eb8-120">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e5eb8-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="e5eb8-121">Parent elements</span></span>

|<span data-ttu-id="e5eb8-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-122">**Element**</span></span>|<span data-ttu-id="e5eb8-123">**Type**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-123">**Type**</span></span>|<span data-ttu-id="e5eb8-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5eb8-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e5eb8-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="e5eb8-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="e5eb8-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="e5eb8-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="e5eb8-127">Contient les éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e5eb8-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="e5eb8-128">Child elements</span></span>

<span data-ttu-id="e5eb8-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5eb8-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="e5eb8-130">Attributes</span></span>

<span data-ttu-id="e5eb8-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="e5eb8-131">None.</span></span>
  

