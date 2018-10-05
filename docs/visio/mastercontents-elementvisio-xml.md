---
title: Élément MasterContents (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 71e75e9a-1392-b40b-1d51-167cd28b2c53
description: Spécifie des informations sur les formes dans une forme de base dans un dessin.
ms.openlocfilehash: 381afe288864553dc56bdf8bb6dc19861abdcc8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385465"
---
# <a name="mastercontents-element-visio-xml"></a><span data-ttu-id="aaccd-103">Élément MasterContents (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="aaccd-103">MasterContents element ('Visio XML')</span></span>

<span data-ttu-id="aaccd-104">Spécifie des informations sur les formes dans une forme de base dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="aaccd-104">Specifies information about the shapes in a master in a drawing.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="aaccd-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="aaccd-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aaccd-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="aaccd-106">**Element type**</span></span> <br/> |[<span data-ttu-id="aaccd-107">PageContents_Type</span><span class="sxs-lookup"><span data-stu-id="aaccd-107">PageContents_Type</span></span>](pagecontents_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="aaccd-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="aaccd-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="aaccd-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="aaccd-109">**Schema file**</span></span> <br/> |<span data-ttu-id="aaccd-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="aaccd-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="aaccd-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="aaccd-111">**Document parts**</span></span> <br/> |<span data-ttu-id="aaccd-112">maître # .xml</span><span class="sxs-lookup"><span data-stu-id="aaccd-112">master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="aaccd-113">Définition</span><span class="sxs-lookup"><span data-stu-id="aaccd-113">Definition</span></span>

```XML
< xs:element name="MasterContents" type="PageContents_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="aaccd-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="aaccd-114">Elements and attributes</span></span>

<span data-ttu-id="aaccd-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="aaccd-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="aaccd-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="aaccd-116">Parent elements</span></span>

<span data-ttu-id="aaccd-117">Aucune.</span><span class="sxs-lookup"><span data-stu-id="aaccd-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aaccd-118">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="aaccd-118">Child elements</span></span>

|<span data-ttu-id="aaccd-119">**Élément**</span><span class="sxs-lookup"><span data-stu-id="aaccd-119">**Element**</span></span>|<span data-ttu-id="aaccd-120">**Type**</span><span class="sxs-lookup"><span data-stu-id="aaccd-120">**Type**</span></span>|<span data-ttu-id="aaccd-121">**Description**</span><span class="sxs-lookup"><span data-stu-id="aaccd-121">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aaccd-122">Connects</span><span class="sxs-lookup"><span data-stu-id="aaccd-122">Connects</span></span>](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aaccd-123">Connects_Type</span><span class="sxs-lookup"><span data-stu-id="aaccd-123">Connects_Type</span></span>](connects_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aaccd-124">Contient un élément de **connexion** pour chaque connexion entre deux formes dans un dessin.</span><span class="sxs-lookup"><span data-stu-id="aaccd-124">Contains a **Connect** element for each connection between two shapes in a drawing.</span></span>  <br/> |
|[<span data-ttu-id="aaccd-125">Shapes</span><span class="sxs-lookup"><span data-stu-id="aaccd-125">Shapes</span></span>](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="aaccd-126">Shapes_Type</span><span class="sxs-lookup"><span data-stu-id="aaccd-126">Shapes_Type</span></span>](shapes_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="aaccd-127">Contient une collection d’éléments de la **forme** .</span><span class="sxs-lookup"><span data-stu-id="aaccd-127">Contains a collection of **Shape** elements.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="aaccd-128">Attributs</span><span class="sxs-lookup"><span data-stu-id="aaccd-128">Attributes</span></span>

<span data-ttu-id="aaccd-129">Aucun.</span><span class="sxs-lookup"><span data-stu-id="aaccd-129">None.</span></span>
  

