---
title: Connects, élément (PageContents_Type complexType) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 398c141c-8a40-7605-254a-2ee7cc0a7af5
description: Contient un élément Connect pour chaque connexion entre deux formes dans un dessin.
ms.openlocfilehash: 00bba6be8b32fc2a8e1d996e89c6983e1e61e3a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318962"
---
# <a name="connects-element-pagecontentstype-complextype-visio-xml"></a><span data-ttu-id="bac46-103">Connects, élément (PageContents_Type complexType) ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="bac46-103">Connects element (PageContents_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="bac46-104">Contient un élément **Connect** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="bac46-104">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="bac46-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="bac46-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bac46-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="bac46-106">**Element type**</span></span> <br/> |[<span data-ttu-id="bac46-107">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="bac46-107">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="bac46-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bac46-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="bac46-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="bac46-109">**Schema file**</span></span> <br/> |<span data-ttu-id="bac46-110">VisioSchema15. xsd</span><span class="sxs-lookup"><span data-stu-id="bac46-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="bac46-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="bac46-111">**Document parts**</span></span> <br/> |<span data-ttu-id="bac46-112">page #. xml, Master #. Xml</span><span class="sxs-lookup"><span data-stu-id="bac46-112">page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bac46-113">Définition</span><span class="sxs-lookup"><span data-stu-id="bac46-113">Definition</span></span>

```XML
< xs:element name="Connects" type="Connects_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bac46-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="bac46-114">Elements and attributes</span></span>

<span data-ttu-id="bac46-115">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="bac46-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bac46-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="bac46-116">Parent elements</span></span>

|<span data-ttu-id="bac46-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bac46-117">**Element**</span></span>|<span data-ttu-id="bac46-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="bac46-118">**Type**</span></span>|<span data-ttu-id="bac46-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="bac46-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bac46-120">MasterContents</span><span class="sxs-lookup"><span data-stu-id="bac46-120">MasterContents</span></span>](mastercontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="bac46-121">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="bac46-121">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bac46-122">Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="bac46-122">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
|[<span data-ttu-id="bac46-123">PageContents</span><span class="sxs-lookup"><span data-stu-id="bac46-123">PageContents</span></span>](pagecontents-elementvisio-xml.md) <br/> |[<span data-ttu-id="bac46-124">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="bac46-124">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bac46-125">Cette énumération spécifie les informations relatives aux formes d'une forme de base ou d'une page de dessin d'un dessin.</span><span class="sxs-lookup"><span data-stu-id="bac46-125">Specifies the information about the shapes in a master or drawing page of a drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="bac46-126">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="bac46-126">Child elements</span></span>

|<span data-ttu-id="bac46-127">**Élément**</span><span class="sxs-lookup"><span data-stu-id="bac46-127">**Element**</span></span>|<span data-ttu-id="bac46-128">**Type**</span><span class="sxs-lookup"><span data-stu-id="bac46-128">**Type**</span></span>|<span data-ttu-id="bac46-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="bac46-129">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bac46-130">Connect</span><span class="sxs-lookup"><span data-stu-id="bac46-130">Connect</span></span>](connect-element-connects_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="bac46-131">Connect_Type</span><span class="sxs-lookup"><span data-stu-id="bac46-131">Connect_Type</span></span>](connect_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="bac46-132">Représente une connexion entre deux formes dans un dessin, telles qu’un trait et un cadre dans un organigramme.</span><span class="sxs-lookup"><span data-stu-id="bac46-132">Represents a connection between two shapes in a drawing, such as a line and a box in an organization chart.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bac46-133">Attributs</span><span class="sxs-lookup"><span data-stu-id="bac46-133">Attributes</span></span>

<span data-ttu-id="bac46-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bac46-134">None.</span></span>
  

