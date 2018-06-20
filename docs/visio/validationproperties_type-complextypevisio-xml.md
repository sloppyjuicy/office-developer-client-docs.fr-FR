---
title: Type complexe ValidationProperties_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: eb1373881b1584b77c6663dd4ec375c50a61efd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789991"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="7457b-102">Type complexe ValidationProperties_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="7457b-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="7457b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="7457b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7457b-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="7457b-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="7457b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="7457b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="7457b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="7457b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="7457b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="7457b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="7457b-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="7457b-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="7457b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="7457b-109">Definition</span></span>

```XML
      <xs:complexType name="ValidationProperties_Type">
    <xs:attribute name="LastValidated"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="ShowIgnored"
  type="xsd:boolean"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="7457b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="7457b-110">Elements and attributes</span></span>

<span data-ttu-id="7457b-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="7457b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="7457b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="7457b-112">Child elements</span></span>

<span data-ttu-id="7457b-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="7457b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7457b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="7457b-114">Attributes</span></span>

|<span data-ttu-id="7457b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7457b-115">**Attribute**</span></span>|<span data-ttu-id="7457b-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="7457b-116">**Type**</span></span>|<span data-ttu-id="7457b-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="7457b-117">**Required**</span></span>|<span data-ttu-id="7457b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="7457b-118">**Description**</span></span>|<span data-ttu-id="7457b-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="7457b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="7457b-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="7457b-120">LastValidated</span></span>  <br/> |<span data-ttu-id="7457b-121">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="7457b-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="7457b-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7457b-122">required</span></span>  <br/> ||<span data-ttu-id="7457b-123">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="7457b-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="7457b-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="7457b-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="7457b-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="7457b-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="7457b-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="7457b-126">required</span></span>  <br/> ||<span data-ttu-id="7457b-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="7457b-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

