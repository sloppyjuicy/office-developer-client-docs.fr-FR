---
title: Type complexe CommentEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 5ee3c9f2aa8b0af91289ce1cd6bb2355adec3426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788282"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="04269-102">Type complexe CommentEntry_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="04269-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="04269-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="04269-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="04269-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="04269-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="04269-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="04269-105">**Schema file**</span></span> <br/> |<span data-ttu-id="04269-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="04269-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="04269-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="04269-107">**Extension base**</span></span> <br/> |<span data-ttu-id="04269-108">XSD : String</span><span class="sxs-lookup"><span data-stu-id="04269-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="04269-109">Définition</span><span class="sxs-lookup"><span data-stu-id="04269-109">Definition</span></span>

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="04269-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="04269-110">Elements and attributes</span></span>

<span data-ttu-id="04269-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="04269-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="04269-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="04269-112">Child elements</span></span>

<span data-ttu-id="04269-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="04269-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="04269-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="04269-114">Attributes</span></span>

|<span data-ttu-id="04269-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="04269-115">**Attribute**</span></span>|<span data-ttu-id="04269-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="04269-116">**Type**</span></span>|<span data-ttu-id="04269-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="04269-117">**Required**</span></span>|<span data-ttu-id="04269-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="04269-118">**Description**</span></span>|<span data-ttu-id="04269-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="04269-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="04269-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="04269-120">AuthorID</span></span>  <br/> |<span data-ttu-id="04269-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04269-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04269-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="04269-122">required</span></span>  <br/> ||<span data-ttu-id="04269-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04269-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04269-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="04269-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="04269-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04269-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04269-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="04269-126">optional</span></span>  <br/> ||<span data-ttu-id="04269-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04269-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04269-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="04269-128">CommentID</span></span>  <br/> |<span data-ttu-id="04269-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04269-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04269-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="04269-130">required</span></span>  <br/> ||<span data-ttu-id="04269-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04269-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04269-132">Date</span><span class="sxs-lookup"><span data-stu-id="04269-132">Date</span></span>  <br/> |<span data-ttu-id="04269-133">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="04269-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="04269-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="04269-134">required</span></span>  <br/> ||<span data-ttu-id="04269-135">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="04269-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="04269-136">Terminé</span><span class="sxs-lookup"><span data-stu-id="04269-136">Done</span></span>  <br/> |<span data-ttu-id="04269-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="04269-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="04269-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="04269-138">optional</span></span>  <br/> ||<span data-ttu-id="04269-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="04269-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="04269-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="04269-140">EditDate</span></span>  <br/> |<span data-ttu-id="04269-141">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="04269-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="04269-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="04269-142">optional</span></span>  <br/> ||<span data-ttu-id="04269-143">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="04269-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="04269-144">PageID</span><span class="sxs-lookup"><span data-stu-id="04269-144">PageID</span></span>  <br/> |<span data-ttu-id="04269-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04269-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04269-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="04269-146">required</span></span>  <br/> ||<span data-ttu-id="04269-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04269-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="04269-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="04269-148">ShapeID</span></span>  <br/> |<span data-ttu-id="04269-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="04269-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="04269-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="04269-150">optional</span></span>  <br/> ||<span data-ttu-id="04269-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="04269-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

