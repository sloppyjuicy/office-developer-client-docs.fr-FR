---
title: Type complexe ValidationProperties_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b0d1209-4636-ea9c-acf7-895c3300492a
ms.openlocfilehash: 2fa6724ce6262886379f3ac22625927608184bab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389980"
---
# <a name="validationpropertiestype-complextype-visio-xml"></a><span data-ttu-id="90ca0-102">Type complexe ValidationProperties_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="90ca0-102">ValidationProperties_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="90ca0-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="90ca0-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="90ca0-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="90ca0-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="90ca0-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="90ca0-105">**Schema file**</span></span> <br/> |<span data-ttu-id="90ca0-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="90ca0-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="90ca0-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="90ca0-107">**Extension base**</span></span> <br/> |<span data-ttu-id="90ca0-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="90ca0-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="90ca0-109">Définition</span><span class="sxs-lookup"><span data-stu-id="90ca0-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="90ca0-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="90ca0-110">Elements and attributes</span></span>

<span data-ttu-id="90ca0-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="90ca0-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="90ca0-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="90ca0-112">Child elements</span></span>

<span data-ttu-id="90ca0-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="90ca0-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="90ca0-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="90ca0-114">Attributes</span></span>

|<span data-ttu-id="90ca0-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="90ca0-115">**Attribute**</span></span>|<span data-ttu-id="90ca0-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="90ca0-116">**Type**</span></span>|<span data-ttu-id="90ca0-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="90ca0-117">**Required**</span></span>|<span data-ttu-id="90ca0-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="90ca0-118">**Description**</span></span>|<span data-ttu-id="90ca0-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="90ca0-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="90ca0-120">LastValidated</span><span class="sxs-lookup"><span data-stu-id="90ca0-120">LastValidated</span></span>  <br/> |<span data-ttu-id="90ca0-121">XSD : DateTime</span><span class="sxs-lookup"><span data-stu-id="90ca0-121">xsd:dateTime</span></span>  <br/> |<span data-ttu-id="90ca0-122">obligatoire</span><span class="sxs-lookup"><span data-stu-id="90ca0-122">required</span></span>  <br/> ||<span data-ttu-id="90ca0-123">Valeurs du type xsd : DateTime.</span><span class="sxs-lookup"><span data-stu-id="90ca0-123">Values of the xsd:dateTime type.</span></span>  <br/> |
|<span data-ttu-id="90ca0-124">ShowIgnored</span><span class="sxs-lookup"><span data-stu-id="90ca0-124">ShowIgnored</span></span>  <br/> |<span data-ttu-id="90ca0-125">type xsd : Boolean</span><span class="sxs-lookup"><span data-stu-id="90ca0-125">xsd:boolean</span></span>  <br/> |<span data-ttu-id="90ca0-126">obligatoire</span><span class="sxs-lookup"><span data-stu-id="90ca0-126">required</span></span>  <br/> ||<span data-ttu-id="90ca0-127">Valeurs du type de type xsd : Boolean.</span><span class="sxs-lookup"><span data-stu-id="90ca0-127">Values of the xsd:boolean type.</span></span>  <br/> |
   

