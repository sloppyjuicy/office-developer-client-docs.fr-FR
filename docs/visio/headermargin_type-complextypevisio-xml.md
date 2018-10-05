---
title: Type complexe HeaderMargin_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 756b87f6-aa0e-c643-c733-7db788f63ac8
ms.openlocfilehash: 9bb32471f1384c89e02e9ffdbcceebfc48d2b22e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393718"
---
# <a name="headermargintype-complextype-visio-xml"></a><span data-ttu-id="513b2-102">Type complexe HeaderMargin_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="513b2-102">HeaderMargin_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="513b2-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="513b2-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="513b2-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="513b2-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="513b2-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="513b2-105">**Schema file**</span></span> <br/> |<span data-ttu-id="513b2-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="513b2-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="513b2-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="513b2-107">**Extension base**</span></span> <br/> |<span data-ttu-id="513b2-108">XSD : double</span><span class="sxs-lookup"><span data-stu-id="513b2-108">xsd:double</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="513b2-109">Définition</span><span class="sxs-lookup"><span data-stu-id="513b2-109">Definition</span></span>

```XML
      <xs:complexType name="HeaderMargin_Type">
        <xs:complexContent>
        <xs:extension base="xsd:double">
      
    <xs:attribute name="Unit"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="513b2-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="513b2-110">Elements and attributes</span></span>

<span data-ttu-id="513b2-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="513b2-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="513b2-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="513b2-112">Child elements</span></span>

<span data-ttu-id="513b2-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="513b2-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="513b2-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="513b2-114">Attributes</span></span>

|<span data-ttu-id="513b2-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="513b2-115">**Attribute**</span></span>|<span data-ttu-id="513b2-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="513b2-116">**Type**</span></span>|<span data-ttu-id="513b2-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="513b2-117">**Required**</span></span>|<span data-ttu-id="513b2-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="513b2-118">**Description**</span></span>|<span data-ttu-id="513b2-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="513b2-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="513b2-120">Unité</span><span class="sxs-lookup"><span data-stu-id="513b2-120">Unit</span></span>  <br/> |<span data-ttu-id="513b2-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="513b2-121">xsd:string</span></span>  <br/> |<span data-ttu-id="513b2-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="513b2-122">optional</span></span>  <br/> ||<span data-ttu-id="513b2-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="513b2-123">Values of the xsd:string type.</span></span>  <br/> |
   

