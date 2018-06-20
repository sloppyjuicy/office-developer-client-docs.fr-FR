---
title: Élément REL (Master_Type, complexType) (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Spécifie une relation vers un composant avec le code XML maître correspondant.
ms.openlocfilehash: 8cd16c55b24cd6edec993cb913709beff72ee325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789423"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a><span data-ttu-id="2b678-103">Élément REL (Master_Type, complexType) (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="2b678-103">Rel element (Master_Type complexType) ('Visio XML')</span></span>

<span data-ttu-id="2b678-104">Spécifie une relation vers un composant avec le code XML maître correspondant.</span><span class="sxs-lookup"><span data-stu-id="2b678-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="2b678-105">Informations sur l'élément</span><span class="sxs-lookup"><span data-stu-id="2b678-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2b678-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="2b678-106">**Element type**</span></span> <br/> |[<span data-ttu-id="2b678-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="2b678-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="2b678-108">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="2b678-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="2b678-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="2b678-109">**Schema file**</span></span> <br/> |<span data-ttu-id="2b678-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="2b678-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="2b678-111">**Parties de document**</span><span class="sxs-lookup"><span data-stu-id="2b678-111">**Document parts**</span></span> <br/> |<span data-ttu-id="2b678-112">pages.XML, masters.xml, recordsets.xml, page # .xml, maître # .xml</span><span class="sxs-lookup"><span data-stu-id="2b678-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="2b678-113">Définition</span><span class="sxs-lookup"><span data-stu-id="2b678-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="2b678-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="2b678-114">Elements and attributes</span></span>

<span data-ttu-id="2b678-115">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="2b678-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="2b678-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="2b678-116">Parent elements</span></span>

|<span data-ttu-id="2b678-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="2b678-117">**Element**</span></span>|<span data-ttu-id="2b678-118">**Type**</span><span class="sxs-lookup"><span data-stu-id="2b678-118">**Type**</span></span>|<span data-ttu-id="2b678-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="2b678-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="2b678-120">Forme de base</span><span class="sxs-lookup"><span data-stu-id="2b678-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="2b678-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="2b678-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="2b678-122">Spécifie une instance de principal XML dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="2b678-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="2b678-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2b678-123">Child elements</span></span>

<span data-ttu-id="2b678-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="2b678-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="2b678-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="2b678-125">Attributes</span></span>

|<span data-ttu-id="2b678-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="2b678-126">**Attribute**</span></span>|<span data-ttu-id="2b678-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="2b678-127">**Type**</span></span>|<span data-ttu-id="2b678-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="2b678-128">**Required**</span></span>|<span data-ttu-id="2b678-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="2b678-129">**Description**</span></span>|<span data-ttu-id="2b678-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="2b678-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="2b678-131">r : id</span><span class="sxs-lookup"><span data-stu-id="2b678-131">r:id</span></span>  <br/> |<span data-ttu-id="2b678-132">XSD : String</span><span class="sxs-lookup"><span data-stu-id="2b678-132">xsd:string</span></span>  <br/> <span data-ttu-id="2b678-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="2b678-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="2b678-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="2b678-134">required</span></span>  <br/> |<span data-ttu-id="2b678-135">Spécifie une relation à un composant.</span><span class="sxs-lookup"><span data-stu-id="2b678-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="2b678-136">« Supprimer # »</span><span class="sxs-lookup"><span data-stu-id="2b678-136">"rId#"</span></span>  <br/> <span data-ttu-id="2b678-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="2b678-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2b678-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="2b678-138">Remarks</span></span>

<span data-ttu-id="2b678-139">La valeur de l’attribut **r : id** doit être un type **ST_RelationshipID** .</span><span class="sxs-lookup"><span data-stu-id="2b678-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="2b678-140">Le type **ST_RelationshipID** est une chaîne qui doit être au format « débarrasser # », où le dernier caractère doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="2b678-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="2b678-141">Le numéro doit être unique parmi tous les éléments frères de l’élément **Rel** .</span><span class="sxs-lookup"><span data-stu-id="2b678-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="2b678-142">Pour plus d’informations sur le type ST_RelationshipID, consultez la [spécification ISO/IEC 29500 partie 1](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span><span class="sxs-lookup"><span data-stu-id="2b678-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

