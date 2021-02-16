---
title: Élément ProtectMasters (DocumentSettings_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Spécifie si l’utilisateur ne peut pas créer, modifier ou supprimer des formes de base. L’utilisateur peut toujours créer de nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.
ms.openlocfilehash: 34ace8c873b133f44ea7bd7c9c2e4127a103a760
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540692"
---
# <a name="protectmasters-element-documentsettings_type-complextype-visio-xml"></a><span data-ttu-id="a70e6-104">Élément ProtectMasters (DocumentSettings_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="a70e6-104">ProtectMasters element (DocumentSettings_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="a70e6-105">Spécifie si l’utilisateur ne peut pas créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="a70e6-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="a70e6-106">L’utilisateur peut toujours créer de nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="a70e6-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="a70e6-107">La plage de valeurs possibles pour cet élément est « 0 » ou « 1 ».</span><span class="sxs-lookup"><span data-stu-id="a70e6-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="a70e6-108">La valeur « 0 » indique que les utilisateurs peuvent créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="a70e6-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="a70e6-109">La valeur « 1 » indique que les utilisateurs ne peuvent pas créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="a70e6-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a70e6-110">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="a70e6-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a70e6-111">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="a70e6-111">**Element type**</span></span> <br/> |[<span data-ttu-id="a70e6-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="a70e6-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="a70e6-113">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a70e6-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="a70e6-114">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="a70e6-114">**Schema file**</span></span> <br/> |<span data-ttu-id="a70e6-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="a70e6-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="a70e6-116">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="a70e6-116">**Document parts**</span></span> <br/> |<span data-ttu-id="a70e6-117">document.xml</span><span class="sxs-lookup"><span data-stu-id="a70e6-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a70e6-118">Définition</span><span class="sxs-lookup"><span data-stu-id="a70e6-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a70e6-119">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="a70e6-119">Elements and attributes</span></span>

<span data-ttu-id="a70e6-120">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="a70e6-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a70e6-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="a70e6-121">Parent elements</span></span>

|<span data-ttu-id="a70e6-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="a70e6-122">**Element**</span></span>|<span data-ttu-id="a70e6-123">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="a70e6-123">**Type**</span></span>|<span data-ttu-id="a70e6-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="a70e6-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a70e6-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="a70e6-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="a70e6-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="a70e6-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="a70e6-127">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="a70e6-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a70e6-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a70e6-128">Child elements</span></span>

<span data-ttu-id="a70e6-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a70e6-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a70e6-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="a70e6-130">Attributes</span></span>

<span data-ttu-id="a70e6-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="a70e6-131">None.</span></span>
  

