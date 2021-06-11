---
title: Élément Rel (Master_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: Spécifie une relation à un élément avec le XML maître correspondant.
ms.openlocfilehash: 032c1ef4a94bb6acf18587a1257fe82285124e87
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542799"
---
# <a name="rel-element-master_type-complextype-visio-xml"></a><span data-ttu-id="c02f6-103">Élément Rel (Master_Type complexType) (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c02f6-103">Rel element (Master_Type complexType) (Visio XML)</span></span>

<span data-ttu-id="c02f6-104">Spécifie une relation à un élément avec le XML maître correspondant.</span><span class="sxs-lookup"><span data-stu-id="c02f6-104">Specifies a relationship to a part with the corresponding master XML.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c02f6-105">Informations sur l’élément</span><span class="sxs-lookup"><span data-stu-id="c02f6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c02f6-106">**Type d’élément**</span><span class="sxs-lookup"><span data-stu-id="c02f6-106">**Element type**</span></span> <br/> |[<span data-ttu-id="c02f6-107">Rel_Type</span><span class="sxs-lookup"><span data-stu-id="c02f6-107">Rel_Type</span></span>](rel_type-complextypevisio-xml.md) <br/> |
|<span data-ttu-id="c02f6-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c02f6-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|<span data-ttu-id="c02f6-109">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c02f6-109">**Schema file**</span></span> <br/> |<span data-ttu-id="c02f6-110">VisioSchema15.xsd</span><span class="sxs-lookup"><span data-stu-id="c02f6-110">VisioSchema15.xsd</span></span>  <br/> |
|<span data-ttu-id="c02f6-111">**Composants de document**</span><span class="sxs-lookup"><span data-stu-id="c02f6-111">**Document parts**</span></span> <br/> |<span data-ttu-id="c02f6-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span><span class="sxs-lookup"><span data-stu-id="c02f6-112">pages.xml, masters.xml, recordsets.xml, page#.xml, master#.xml</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c02f6-113">Définition</span><span class="sxs-lookup"><span data-stu-id="c02f6-113">Definition</span></span>

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a><span data-ttu-id="c02f6-114">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c02f6-114">Elements and attributes</span></span>

<span data-ttu-id="c02f6-115">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c02f6-115">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c02f6-116">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c02f6-116">Parent elements</span></span>

|<span data-ttu-id="c02f6-117">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c02f6-117">**Element**</span></span>|<span data-ttu-id="c02f6-118">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c02f6-118">**Type**</span></span>|<span data-ttu-id="c02f6-119">**Description**</span><span class="sxs-lookup"><span data-stu-id="c02f6-119">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c02f6-120">Master</span><span class="sxs-lookup"><span data-stu-id="c02f6-120">Master</span></span>](master-element-masters_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c02f6-121">Master_Type</span><span class="sxs-lookup"><span data-stu-id="c02f6-121">Master_Type</span></span>](master_type-complextypevisio-xml.md) <br/> |<span data-ttu-id="c02f6-122">Spécifie une instance de master XML stockée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="c02f6-122">Specifies one instance of master XML stored in the drawing.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="c02f6-123">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c02f6-123">Child elements</span></span>

<span data-ttu-id="c02f6-124">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c02f6-124">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c02f6-125">Attributs</span><span class="sxs-lookup"><span data-stu-id="c02f6-125">Attributes</span></span>

|<span data-ttu-id="c02f6-126">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="c02f6-126">**Attribute**</span></span>|<span data-ttu-id="c02f6-127">**Type**</span><span class="sxs-lookup"><span data-stu-id="c02f6-127">**Type**</span></span>|<span data-ttu-id="c02f6-128">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="c02f6-128">**Required**</span></span>|<span data-ttu-id="c02f6-129">**Description**</span><span class="sxs-lookup"><span data-stu-id="c02f6-129">**Description**</span></span>|<span data-ttu-id="c02f6-130">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="c02f6-130">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c02f6-131">r:id</span><span class="sxs-lookup"><span data-stu-id="c02f6-131">r:id</span></span>  <br/> |<span data-ttu-id="c02f6-132">xsd:string</span><span class="sxs-lookup"><span data-stu-id="c02f6-132">xsd:string</span></span>  <br/> <span data-ttu-id="c02f6-133">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="c02f6-133">See Remarks.</span></span>  <br/> |<span data-ttu-id="c02f6-134">obligatoire</span><span class="sxs-lookup"><span data-stu-id="c02f6-134">required</span></span>  <br/> |<span data-ttu-id="c02f6-135">Spécifie une relation à un élément.</span><span class="sxs-lookup"><span data-stu-id="c02f6-135">Specifies a relationship to a part.</span></span>  <br/> |<span data-ttu-id="c02f6-136">« rId# »</span><span class="sxs-lookup"><span data-stu-id="c02f6-136">"rId#"</span></span>  <br/> <span data-ttu-id="c02f6-137">Voir les remarques.</span><span class="sxs-lookup"><span data-stu-id="c02f6-137">See Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c02f6-138">Remarques</span><span class="sxs-lookup"><span data-stu-id="c02f6-138">Remarks</span></span>

<span data-ttu-id="c02f6-139">La valeur de **l’attribut r:id** doit être **ST_RelationshipID** type.</span><span class="sxs-lookup"><span data-stu-id="c02f6-139">The value of the **r:id** attribute must be an **ST_RelationshipID** type.</span></span> <span data-ttu-id="c02f6-140">Le ST_RelationshipID type est une chaîne qui doit être au format « rId# **»** où le caractère final doit être un nombre.</span><span class="sxs-lookup"><span data-stu-id="c02f6-140">The **ST_RelationshipID** type is a string that must be in the format 'rId#', where the final character must be a number.</span></span> <span data-ttu-id="c02f6-141">Le nombre doit être unique parmi tous les éléments frères de **l’élément Rel.**</span><span class="sxs-lookup"><span data-stu-id="c02f6-141">The number must be unique among all sibling elements of the **Rel** element.</span></span> 
  
<span data-ttu-id="c02f6-142">Pour plus d’informations sur le type ST_RelationshipID, voir la spécification [ISO/IEC 29500 Partie 1.](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)</span><span class="sxs-lookup"><span data-stu-id="c02f6-142">For more information about the ST_RelationshipID type, see the [ISO/IEC 29500 Part 1 specification](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750).</span></span>
  

