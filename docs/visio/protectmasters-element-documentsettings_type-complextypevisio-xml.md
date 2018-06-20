---
title: Élément ProtectMasters (DocumentSettings_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: edc46630-c320-6b4e-4747-961075dd5fd7
description: Spécifie si l’utilisateur est empêché de création, modification ou la suppression des formes de base. L’utilisateur peut toujours créer des nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.
ms.openlocfilehash: cb576f267e076b06f2088ce53a18e9af36a46b0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789357"
---
# <a name="protectmasters-element-documentsettingstype-complextype-visio-xml"></a><span data-ttu-id="54e52-104">Élément ProtectMasters (DocumentSettings_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="54e52-104">ProtectMasters element (DocumentSettings_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="54e52-105">Spécifie si l’utilisateur est empêché de création, modification ou la suppression des formes de base.</span><span class="sxs-lookup"><span data-stu-id="54e52-105">Specifies whether the user is prevented from creating, editing, or deleting master shapes.</span></span> <span data-ttu-id="54e52-106">L’utilisateur peut toujours créer des nouvelles formes à partir d’une forme de base, quel que soit ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="54e52-106">The user can still create new shapes from a master shape, regardless of this setting.</span></span> 
  
<span data-ttu-id="54e52-107">La plage de valeurs possibles pour cet élément est « 0 » ou « 1 ».</span><span class="sxs-lookup"><span data-stu-id="54e52-107">The range of possible values for this element is either '0' or '1'.</span></span> <span data-ttu-id="54e52-108">Une valeur de « 0 » indique que les utilisateurs peuvent créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="54e52-108">A value of '0' indicates that users can create, edit, or delete master shapes.</span></span> <span data-ttu-id="54e52-109">La valeur « 1 » indique que les utilisateurs ne peuvent pas créer, modifier ou supprimer des formes de base.</span><span class="sxs-lookup"><span data-stu-id="54e52-109">A value of '1' indicates that users cannot create, edit, or delete master shapes.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="54e52-110">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="54e52-110">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="54e52-111">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="54e52-111">**Element type**</span></span> <br/> |[<span data-ttu-id="54e52-112">ProtectMasters_Type</span><span class="sxs-lookup"><span data-stu-id="54e52-112">ProtectMasters_Type</span></span>](protectmasters_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="54e52-113">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="54e52-113">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="54e52-114">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="54e52-114">**Schema file**</span></span> <br/> |<span data-ttu-id="54e52-115">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="54e52-115">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="54e52-116">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="54e52-116">**Document parts**</span></span> <br/> |<span data-ttu-id="54e52-117">document.Xml</span><span class="sxs-lookup"><span data-stu-id="54e52-117">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="54e52-118">Définition</span><span class="sxs-lookup"><span data-stu-id="54e52-118">Definition</span></span>

```XML
< xs:element name="ProtectMasters" type="ProtectMasters_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="54e52-119">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="54e52-119">Elements and attributes</span></span>

<span data-ttu-id="54e52-120">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="54e52-120">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="54e52-121">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="54e52-121">Parent elements</span></span>

|<span data-ttu-id="54e52-122">**Élément**</span><span class="sxs-lookup"><span data-stu-id="54e52-122">**Element**</span></span>|<span data-ttu-id="54e52-123">**Type**</span><span class="sxs-lookup"><span data-stu-id="54e52-123">**Type**</span></span>|<span data-ttu-id="54e52-124">**Description**</span><span class="sxs-lookup"><span data-stu-id="54e52-124">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="54e52-125">DocumentSettings</span><span class="sxs-lookup"><span data-stu-id="54e52-125">DocumentSettings</span></span>](documentsettings-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="54e52-126">DocumentSettings_Type</span><span class="sxs-lookup"><span data-stu-id="54e52-126">DocumentSettings_Type</span></span>](documentsettings_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="54e52-127">Contient des éléments qui spécifient les paramètres de document.</span><span class="sxs-lookup"><span data-stu-id="54e52-127">Contains elements that specify document settings.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="54e52-128">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="54e52-128">Child elements</span></span>

<span data-ttu-id="54e52-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54e52-129">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="54e52-130">Attributs</span><span class="sxs-lookup"><span data-stu-id="54e52-130">Attributes</span></span>

<span data-ttu-id="54e52-131">Aucun.</span><span class="sxs-lookup"><span data-stu-id="54e52-131">None.</span></span>
  

