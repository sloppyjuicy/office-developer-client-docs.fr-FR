---
title: Élément REL (Page_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d61b1b97-c360-4d9d-217f-e6f45f760e42
description: Spécifie une relation vers un composant à la page correspondante XML.
ms.openlocfilehash: 7a45764817175f670cdb009157e21a1a25f31cc5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398905"
---
# <a name="rel-element-pagetype-complextype-visio-xml"></a><span data-ttu-id="f754f-103">Élément REL (Page_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="f754f-103">Rel element (Page_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="f754f-104">Spécifie une relation vers un composant à la page correspondante XML.</span><span class="sxs-lookup"><span data-stu-id="f754f-104">Specifies a relationship to a part with the corresponding page XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f754f-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="f754f-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f754f-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="f754f-106">**Element type**</span></span> <br/> |[<span data-ttu-id="f754f-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="f754f-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="f754f-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="f754f-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="f754f-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="f754f-109">**Schema file**</span></span> <br/> |<span data-ttu-id="f754f-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="f754f-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="f754f-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="f754f-111">**Document parts**</span></span> <br/> |<span data-ttu-id="f754f-112">pages.XML, masters.xml, recordsets.xml, page # .xml, maître # .xml</span><span class="sxs-lookup"><span data-stu-id="f754f-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="f754f-113">Définition</span><span class="sxs-lookup"><span data-stu-id="f754f-113">Definition</span></span>

```XML
< xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="f754f-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="f754f-114">Elements and attributes</span></span>

<span data-ttu-id="f754f-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="f754f-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="f754f-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f754f-116">Parent elements</span></span>

|<span data-ttu-id="f754f-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="f754f-117">**Element**</span></span>|<span data-ttu-id="f754f-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="f754f-118">**Type**</span></span>|<span data-ttu-id="f754f-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="f754f-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="f754f-120">Page</span><span class="sxs-lookup"><span data-stu-id="f754f-120">Page</span></span>](page-element-pages_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="f754f-121">Page_Type</span><span class="sxs-lookup"><span data-stu-id="f754f-121">Page_Type</span></span>](page_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="f754f-122">Spécifie une instance d’une page que XML stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="f754f-122">Specifies one instance of page XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="f754f-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f754f-123">Child elements</span></span>

<span data-ttu-id="f754f-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f754f-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f754f-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="f754f-125">Attributes</span></span>

|<span data-ttu-id="f754f-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="f754f-126">**Attribute**</span></span>|<span data-ttu-id="f754f-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="f754f-127">**Type**</span></span>|<span data-ttu-id="f754f-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="f754f-128">**Required**</span></span>|<span data-ttu-id="f754f-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="f754f-129">**Description**</span></span>|<span data-ttu-id="f754f-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="f754f-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="f754f-131">r : id</span><span class="sxs-lookup"><span data-stu-id="f754f-131">r:id</span></span>  <br/> |<span data-ttu-id="f754f-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="f754f-132">xsd:string</span></span>  <br/> <span data-ttu-id="f754f-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="f754f-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="f754f-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="f754f-134">required</span></span>  <br/> |<span data-ttu-id="f754f-135">Spécifie une relation à un composant.</span><span class="sxs-lookup"><span data-stu-id="f754f-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="f754f-136">« Supprimer # »</span><span class="sxs-lookup"><span data-stu-id="f754f-136">"rId#"</span></span>  <br/> <span data-ttu-id="f754f-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="f754f-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f754f-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="f754f-138">Remarks</span></span>

<span data-ttu-id="f754f-139">La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="f754f-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="f754f-140">Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="f754f-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="f754f-141">Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** .</span><span class="sxs-lookup"><span data-stu-id="f754f-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="f754f-142">Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="f754f-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

