---
title: Élément Connects (PageContents_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contient un élément Connect pour chaque connexion entre deux formes dans un dessin.
ms.openlocfilehash: d421068926a40a8f7c24a783388d06091700211f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538710"
---
# <a name="connects-element-pagecontents_type-complextype-visio-xml"></a><span data-ttu-id="c3ee4-103">Élément Connects (PageContents_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c3ee4-103">Connects element (PageContents_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c3ee4-104">Contient un **élément Connect** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="c3ee4-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c3ee4-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3ee4-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c3ee4-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="c3ee4-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c3ee4-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c3ee4-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c3ee4-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c3ee4-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c3ee4-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c3ee4-112">page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="c3ee4-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3ee4-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c3ee4-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c3ee4-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c3ee4-114">Elements and attributes</span></span>

<span data-ttu-id="c3ee4-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3ee4-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c3ee4-116">Parent elements</span></span>

|<span data-ttu-id="c3ee4-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-117">**Element**</span></span>|<span data-ttu-id="c3ee4-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-118">**Type**</span></span>|<span data-ttu-id="c3ee4-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3ee4-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="c3ee4-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c3ee4-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c3ee4-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3ee4-122">Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="c3ee4-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="c3ee4-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="c3ee4-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="c3ee4-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3ee4-125">Spécifie les informations sur les formes d’une forme de base ou d’une page de dessin d’un dessin.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c3ee4-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c3ee4-126">Child elements</span></span>

|<span data-ttu-id="c3ee4-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-127">**Element**</span></span>|<span data-ttu-id="c3ee4-128">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-128">**Type**</span></span>|<span data-ttu-id="c3ee4-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3ee4-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3ee4-130">Connect</span><span class="sxs-lookup"><span data-stu-id="c3ee4-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3ee4-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="c3ee4-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c3ee4-132">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c3ee4-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="c3ee4-133">Attributes</span></span>

<span data-ttu-id="c3ee4-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c3ee4-134">None.</span></span>
  

