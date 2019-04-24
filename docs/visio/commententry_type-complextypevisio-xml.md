---
title: ComplexType CommentEntry_Type ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334943"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="9ae7d-102">ComplexType CommentEntry_Type ('Visio XML')</span><span class="sxs-lookup"><span data-stu-id="9ae7d-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="9ae7d-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="9ae7d-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ae7d-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="9ae7d-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-105">**Schema file**</span></span> <br/> |<span data-ttu-id="9ae7d-106">VisioSchema15-2012-06 -05. xsd</span><span class="sxs-lookup"><span data-stu-id="9ae7d-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="9ae7d-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-107">**Extension base**</span></span> <br/> |<span data-ttu-id="9ae7d-108">xsd: String</span><span class="sxs-lookup"><span data-stu-id="9ae7d-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ae7d-109">Définition</span><span class="sxs-lookup"><span data-stu-id="9ae7d-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="9ae7d-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="9ae7d-110">Elements and attributes</span></span>

<span data-ttu-id="9ae7d-111">Si le schéma définit des exigences spécifiques, telles que **Sequence**, **minOccurs**, **maxOccurs**et **Choice**, reportez-vous à la section définition.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="9ae7d-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="9ae7d-112">Child elements</span></span>

<span data-ttu-id="9ae7d-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ae7d-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="9ae7d-114">Attributes</span></span>

|<span data-ttu-id="9ae7d-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-115">**Attribute**</span></span>|<span data-ttu-id="9ae7d-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-116">**Type**</span></span>|<span data-ttu-id="9ae7d-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-117">**Required**</span></span>|<span data-ttu-id="9ae7d-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-118">**Description**</span></span>|<span data-ttu-id="9ae7d-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="9ae7d-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ae7d-120">Faut</span><span class="sxs-lookup"><span data-stu-id="9ae7d-120">AuthorID</span></span>  <br/> |<span data-ttu-id="9ae7d-121">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ae7d-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ae7d-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ae7d-122">required</span></span>  <br/> ||<span data-ttu-id="9ae7d-123">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="9ae7d-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="9ae7d-125">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ae7d-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ae7d-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="9ae7d-126">optional</span></span>  <br/> ||<span data-ttu-id="9ae7d-127">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="9ae7d-128">CommentID</span></span>  <br/> |<span data-ttu-id="9ae7d-129">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ae7d-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ae7d-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ae7d-130">required</span></span>  <br/> ||<span data-ttu-id="9ae7d-131">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-132">Date</span><span class="sxs-lookup"><span data-stu-id="9ae7d-132">Date</span></span>  <br/> |<span data-ttu-id="9ae7d-133">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="9ae7d-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ae7d-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ae7d-134">required</span></span>  <br/> ||<span data-ttu-id="9ae7d-135">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-136">Terminé</span><span class="sxs-lookup"><span data-stu-id="9ae7d-136">Done</span></span>  <br/> |<span data-ttu-id="9ae7d-137">xsd: Boolean</span><span class="sxs-lookup"><span data-stu-id="9ae7d-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="9ae7d-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="9ae7d-138">optional</span></span>  <br/> ||<span data-ttu-id="9ae7d-139">Valeurs du type xsd: Boolean.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="9ae7d-140">EditDate</span></span>  <br/> |<span data-ttu-id="9ae7d-141">xsd: dateTime</span><span class="sxs-lookup"><span data-stu-id="9ae7d-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="9ae7d-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="9ae7d-142">optional</span></span>  <br/> ||<span data-ttu-id="9ae7d-143">Valeurs du type xsd: dateTime.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-144">PageID</span><span class="sxs-lookup"><span data-stu-id="9ae7d-144">PageID</span></span>  <br/> |<span data-ttu-id="9ae7d-145">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ae7d-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ae7d-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="9ae7d-146">required</span></span>  <br/> ||<span data-ttu-id="9ae7d-147">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="9ae7d-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="9ae7d-148">ShapeID</span></span>  <br/> |<span data-ttu-id="9ae7d-149">xsd: unsignedInt</span><span class="sxs-lookup"><span data-stu-id="9ae7d-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="9ae7d-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="9ae7d-150">optional</span></span>  <br/> ||<span data-ttu-id="9ae7d-151">Valeurs du type xsd: unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="9ae7d-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

