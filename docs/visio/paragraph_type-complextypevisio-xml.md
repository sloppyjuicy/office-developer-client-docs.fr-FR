---
title: Type complexe Paragraph_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 23409c92-5e66-1e11-54a0-677d18e4e03a
ms.openlocfilehash: 4d15d262d66a2d247aa432d08b22e6fe3a460e2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789235"
---
# <a name="paragraphtype-complextype-visio-xml"></a><span data-ttu-id="17786-102">Type complexe Paragraph_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="17786-102">Paragraph_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="17786-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="17786-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17786-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="17786-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="17786-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="17786-105">**Schema file**</span></span> <br/> |<span data-ttu-id="17786-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="17786-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="17786-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="17786-107">**Extension base**</span></span> <br/> |<span data-ttu-id="17786-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="17786-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17786-109">Définition</span><span class="sxs-lookup"><span data-stu-id="17786-109">Definition</span></span>

```XML
          <xs:complexType name="Paragraph_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ParagraphRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="17786-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="17786-110">Elements and attributes</span></span>

<span data-ttu-id="17786-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="17786-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="17786-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="17786-112">Child elements</span></span>

|<span data-ttu-id="17786-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="17786-113">**Element**</span></span>|<span data-ttu-id="17786-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="17786-114">**Type**</span></span>|<span data-ttu-id="17786-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="17786-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17786-116">Row</span><span class="sxs-lookup"><span data-stu-id="17786-116">Row</span></span>](row-element-paragraph-sectionvisio-xml.md) <br/> |[<span data-ttu-id="17786-117">ParagraphRow_Type</span><span class="sxs-lookup"><span data-stu-id="17786-117">ParagraphRow_Type</span></span>](paragraphrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="17786-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="17786-118">Attributes</span></span>

<span data-ttu-id="17786-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="17786-119">None.</span></span>
  

