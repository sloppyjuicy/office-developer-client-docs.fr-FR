---
title: Se connecte, élément (PageContents_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contient un élément de connexion pour chaque connexion entre deux formes dans un dessin.
ms.openlocfilehash: 93930a8f21f9d250bf24d821b0eeb4036f6fe187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788345"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="913ff-103">Se connecte, élément (PageContents_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="913ff-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="913ff-104">Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="913ff-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="913ff-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="913ff-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="913ff-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="913ff-106">**Element type**</span></span> <br/> |[<span data-ttu-id="913ff-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="913ff-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="913ff-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="913ff-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="913ff-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="913ff-109">**Schema file**</span></span> <br/> |<span data-ttu-id="913ff-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="913ff-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="913ff-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="913ff-111">**Document parts**</span></span> <br/> |<span data-ttu-id="913ff-112">page # .xml, master # .xml</span><span class="sxs-lookup"><span data-stu-id="913ff-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="913ff-113">Définition</span><span class="sxs-lookup"><span data-stu-id="913ff-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="913ff-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="913ff-114">Elements and attributes</span></span>

<span data-ttu-id="913ff-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="913ff-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="913ff-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="913ff-116">Parent elements</span></span>

|<span data-ttu-id="913ff-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="913ff-117">**Element**</span></span>|<span data-ttu-id="913ff-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="913ff-118">**Type**</span></span>|<span data-ttu-id="913ff-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="913ff-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="913ff-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="913ff-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="913ff-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="913ff-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="913ff-122">Spécifie les informations concernant les formes dans une page maître ou dessin d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="913ff-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="913ff-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="913ff-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="913ff-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="913ff-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="913ff-125">Spécifie les informations concernant les formes dans une page maître ou dessin d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="913ff-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="913ff-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="913ff-126">Child elements</span></span>

|<span data-ttu-id="913ff-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="913ff-127">**Element**</span></span>|<span data-ttu-id="913ff-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="913ff-128">**Type**</span></span>|<span data-ttu-id="913ff-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="913ff-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="913ff-130">Connect</span><span class="sxs-lookup"><span data-stu-id="913ff-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="913ff-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="913ff-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="913ff-132">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="913ff-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="913ff-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="913ff-133">Attributes</span></span>

<span data-ttu-id="913ff-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="913ff-134">None.</span></span>
  

