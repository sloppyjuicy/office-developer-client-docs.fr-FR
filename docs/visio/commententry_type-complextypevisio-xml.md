---
title: Type complexe CommentEntry_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: eabfe218414874cdc7f10234ed6eeb1fa2f75cf4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384793"
---
# <a name="commententrytype-complextype-visio-xml"></a><span data-ttu-id="1cf31-102">Type complexe CommentEntry_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1cf31-102">CommentEntry_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1cf31-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1cf31-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1cf31-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1cf31-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1cf31-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1cf31-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1cf31-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1cf31-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1cf31-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1cf31-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1cf31-108">XSD : String</span><span class="sxs-lookup"><span data-stu-id="1cf31-108">xsd:string</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1cf31-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1cf31-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1cf31-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1cf31-110">Elements and attributes</span></span>

<span data-ttu-id="1cf31-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1cf31-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1cf31-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1cf31-112">Child elements</span></span>

<span data-ttu-id="1cf31-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1cf31-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1cf31-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="1cf31-114">Attributes</span></span>

|<span data-ttu-id="1cf31-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1cf31-115">**Attribute**</span></span>|<span data-ttu-id="1cf31-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="1cf31-116">**Type**</span></span>|<span data-ttu-id="1cf31-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="1cf31-117">**Required**</span></span>|<span data-ttu-id="1cf31-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="1cf31-118">**Description**</span></span>|<span data-ttu-id="1cf31-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="1cf31-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1cf31-120">AuthorID</span><span class="sxs-lookup"><span data-stu-id="1cf31-120">AuthorID</span></span>  <br/> |<span data-ttu-id="1cf31-121">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf31-121">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf31-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cf31-122">required</span></span>  <br/> ||<span data-ttu-id="1cf31-123">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf31-123">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-124">AutoCommentType</span><span class="sxs-lookup"><span data-stu-id="1cf31-124">AutoCommentType</span></span>  <br/> |<span data-ttu-id="1cf31-125">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf31-125">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf31-126">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cf31-126">optional</span></span>  <br/> ||<span data-ttu-id="1cf31-127">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf31-127">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-128">CommentID</span><span class="sxs-lookup"><span data-stu-id="1cf31-128">CommentID</span></span>  <br/> |<span data-ttu-id="1cf31-129">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf31-129">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf31-130">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cf31-130">required</span></span>  <br/> ||<span data-ttu-id="1cf31-131">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf31-131">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-132">Date</span><span class="sxs-lookup"><span data-stu-id="1cf31-132">Date</span></span>  <br/> |<span data-ttu-id="1cf31-133">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="1cf31-133">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="1cf31-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cf31-134">required</span></span>  <br/> ||<span data-ttu-id="1cf31-135">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="1cf31-135">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-136">Terminé</span><span class="sxs-lookup"><span data-stu-id="1cf31-136">Done</span></span>  <br/> |<span data-ttu-id="1cf31-137">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="1cf31-137">xsd:boolean</span></span>  <br/> |<span data-ttu-id="1cf31-138">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cf31-138">optional</span></span>  <br/> ||<span data-ttu-id="1cf31-139">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="1cf31-139">Values of the xsd:boolean type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-140">EditDate</span><span class="sxs-lookup"><span data-stu-id="1cf31-140">EditDate</span></span>  <br/> |<span data-ttu-id="1cf31-141">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="1cf31-141">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="1cf31-142">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cf31-142">optional</span></span>  <br/> ||<span data-ttu-id="1cf31-143">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="1cf31-143">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-144">PageID</span><span class="sxs-lookup"><span data-stu-id="1cf31-144">PageID</span></span>  <br/> |<span data-ttu-id="1cf31-145">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf31-145">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf31-146">obligatoire</span><span class="sxs-lookup"><span data-stu-id="1cf31-146">required</span></span>  <br/> ||<span data-ttu-id="1cf31-147">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf31-147">Values of the xsd:unsignedInt type.</span></span>  <br/> |
|<span data-ttu-id="1cf31-148">ShapeID</span><span class="sxs-lookup"><span data-stu-id="1cf31-148">ShapeID</span></span>  <br/> |<span data-ttu-id="1cf31-149">XSD:unsignedInt</span><span class="sxs-lookup"><span data-stu-id="1cf31-149">xsd:unsignedInt</span></span>  <br/> |<span data-ttu-id="1cf31-150">facultatif</span><span class="sxs-lookup"><span data-stu-id="1cf31-150">optional</span></span>  <br/> ||<span data-ttu-id="1cf31-151">Valeurs du type xsd:unsignedInt.</span><span class="sxs-lookup"><span data-stu-id="1cf31-151">Values of the xsd:unsignedInt type.</span></span>  <br/> |
   

