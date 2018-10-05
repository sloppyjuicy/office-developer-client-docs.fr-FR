---
title: HeaderMargin, élément (HeaderFooter_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2bb0f4c5-eacf-e09b-2fce-dcff2d927557
description: Indique la marge de l’en-tête d’un document.
ms.openlocfilehash: d8126ae73b1fb330234698343d14468fcbb3eed8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393375"
---
# <a name="headermargin-element-headerfootertype-complextype-visio-xml"></a><span data-ttu-id="62dec-103">HeaderMargin, élément (HeaderFooter_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="62dec-103">HeaderMargin element (HeaderFooter_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="62dec-104">Indique la marge de l’en-tête d’un document.</span><span class="sxs-lookup"><span data-stu-id="62dec-104">Specifies the margin of a document's header.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="62dec-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="62dec-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="62dec-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="62dec-106">**Element type**</span></span> <br/> |[<span data-ttu-id="62dec-107">HeaderMargin_Type</span><span class="sxs-lookup"><span data-stu-id="62dec-107">HeaderMargin_Type</span></span>](headermargin_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="62dec-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="62dec-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="62dec-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="62dec-109">**Schema file**</span></span> <br/> |<span data-ttu-id="62dec-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="62dec-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="62dec-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="62dec-111">**Document parts**</span></span> <br/> |<span data-ttu-id="62dec-112">document.Xml</span><span class="sxs-lookup"><span data-stu-id="62dec-112">document.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="62dec-113">Définition</span><span class="sxs-lookup"><span data-stu-id="62dec-113">Definition</span></span>

```XML
< xs:element name="HeaderMargin" type="HeaderMargin_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="62dec-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="62dec-114">Elements and attributes</span></span>

<span data-ttu-id="62dec-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="62dec-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="62dec-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="62dec-116">Parent elements</span></span>

|<span data-ttu-id="62dec-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="62dec-117">**Element**</span></span>|<span data-ttu-id="62dec-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="62dec-118">**Type**</span></span>|<span data-ttu-id="62dec-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="62dec-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="62dec-120">HeaderFooter</span><span class="sxs-lookup"><span data-stu-id="62dec-120">HeaderFooter</span></span>](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="62dec-121">HeaderFooter_Type</span><span class="sxs-lookup"><span data-stu-id="62dec-121">HeaderFooter_Type</span></span>](headerfooter_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="62dec-122">Contient les éléments d’en-tête et de pied de page d’un document.</span><span class="sxs-lookup"><span data-stu-id="62dec-122">Contains elements for a document's header and footer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="62dec-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="62dec-123">Child elements</span></span>

<span data-ttu-id="62dec-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="62dec-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="62dec-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="62dec-125">Attributes</span></span>

|<span data-ttu-id="62dec-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="62dec-126">**Attribute**</span></span>|<span data-ttu-id="62dec-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="62dec-127">**Type**</span></span>|<span data-ttu-id="62dec-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="62dec-128">**Required**</span></span>|<span data-ttu-id="62dec-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="62dec-129">**Description**</span></span>|<span data-ttu-id="62dec-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="62dec-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="62dec-131">Unité</span><span class="sxs-lookup"><span data-stu-id="62dec-131">Unit</span></span>  <br/> |<span data-ttu-id="62dec-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="62dec-132">xsd:string</span></span>  <br/> |<span data-ttu-id="62dec-133">facultatif</span><span class="sxs-lookup"><span data-stu-id="62dec-133">optional</span></span>  <br/> |<span data-ttu-id="62dec-134">Représente une unité de mesure.</span><span class="sxs-lookup"><span data-stu-id="62dec-134">Represents a unit of measure.</span></span> <span data-ttu-id="62dec-135">La valeur par défaut est le point de distribution.</span><span class="sxs-lookup"><span data-stu-id="62dec-135">The default is DP.</span></span>  <br/> |<span data-ttu-id="62dec-136">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="62dec-136">Values of the xsd:string type.</span></span>  <br/> |
   

