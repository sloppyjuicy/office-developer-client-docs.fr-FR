---
title: Type complexe FooterMargin_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: db8d1e5b-cd29-f9ff-994a-25c28672db81
ms.openlocfilehash: 69f5ce201bd1859aa716e0967939f0c1e5a5a2c6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398933"
---
# <a name="footermargintype-complextype-visio-xml"></a><span data-ttu-id="92e6b-102">Type complexe FooterMargin_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="92e6b-102">FooterMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="92e6b-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="92e6b-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92e6b-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="92e6b-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="92e6b-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="92e6b-105">**Schema file**</span></span> <br/> |<span data-ttu-id="92e6b-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="92e6b-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="92e6b-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="92e6b-107">**Extension base**</span></span> <br/> |<span data-ttu-id="92e6b-108">XSD : double</span><span class="sxs-lookup"><span data-stu-id="92e6b-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="92e6b-109">Définition</span><span class="sxs-lookup"><span data-stu-id="92e6b-109">Definition</span></span>

```XML
      <xs:complexType name="FooterMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="92e6b-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="92e6b-110">Elements and attributes</span></span>

<span data-ttu-id="92e6b-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="92e6b-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="92e6b-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="92e6b-112">Child elements</span></span>

<span data-ttu-id="92e6b-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="92e6b-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92e6b-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="92e6b-114">Attributes</span></span>

|<span data-ttu-id="92e6b-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="92e6b-115">**Attribute**</span></span>|<span data-ttu-id="92e6b-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="92e6b-116">**Type**</span></span>|<span data-ttu-id="92e6b-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="92e6b-117">**Required**</span></span>|<span data-ttu-id="92e6b-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="92e6b-118">**Description**</span></span>|<span data-ttu-id="92e6b-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="92e6b-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="92e6b-120">Unité</span><span class="sxs-lookup"><span data-stu-id="92e6b-120">Unit</span></span>  <br/> |<span data-ttu-id="92e6b-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="92e6b-121">xsd:string</span></span>  <br/> |<span data-ttu-id="92e6b-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="92e6b-122">optional</span></span>  <br/> ||<span data-ttu-id="92e6b-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="92e6b-123">Values of the xsd:string type.</span></span>  <br/> |
   

