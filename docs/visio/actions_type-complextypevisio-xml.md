---
title: Type complexe Actions_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 158a0dfa31c2da3ac9e530c07edd075b4fabbd75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389560"
---
# <a name="actionstype-complextype-visio-xml"></a><span data-ttu-id="1a16a-102">Type complexe Actions_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="1a16a-102">Actions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="1a16a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="1a16a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a16a-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="1a16a-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="1a16a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="1a16a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="1a16a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="1a16a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="1a16a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="1a16a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="1a16a-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="1a16a-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1a16a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="1a16a-109">Definition</span></span>

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="1a16a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="1a16a-110">Elements and attributes</span></span>

<span data-ttu-id="1a16a-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="1a16a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="1a16a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1a16a-112">Child elements</span></span>

|<span data-ttu-id="1a16a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="1a16a-113">**Element**</span></span>|<span data-ttu-id="1a16a-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="1a16a-114">**Type**</span></span>|<span data-ttu-id="1a16a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1a16a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1a16a-116">Row</span><span class="sxs-lookup"><span data-stu-id="1a16a-116">Row</span></span>](row-element-actions-sectionvisio-xml.md) <br/> |[<span data-ttu-id="1a16a-117">ActionsRow_Type</span><span class="sxs-lookup"><span data-stu-id="1a16a-117">ActionsRow_Type</span></span>](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="1a16a-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="1a16a-118">Attributes</span></span>

<span data-ttu-id="1a16a-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="1a16a-119">None.</span></span>
  

