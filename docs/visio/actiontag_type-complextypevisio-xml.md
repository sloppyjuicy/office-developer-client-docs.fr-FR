---
title: Type complexe ActionTag_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bcc17e7-d59d-d392-f299-78d7665202fc
ms.openlocfilehash: e5061e4a4e6e51437ba53ec01f1bfcc33a17d6ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787998"
---
# <a name="actiontagtype-complextype-visio-xml"></a><span data-ttu-id="32186-102">Type complexe ActionTag_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="32186-102">ActionTag_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="32186-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="32186-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="32186-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="32186-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="32186-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="32186-105">**Schema file**</span></span> <br/> |<span data-ttu-id="32186-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="32186-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="32186-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="32186-107">**Extension base**</span></span> <br/> |<span data-ttu-id="32186-108">Section_Type</span><span class="sxs-lookup"><span data-stu-id="32186-108">Section_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="32186-109">Définition</span><span class="sxs-lookup"><span data-stu-id="32186-109">Definition</span></span>

```XML
          <xs:complexType name="ActionTag_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionTagRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="32186-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="32186-110">Elements and attributes</span></span>

<span data-ttu-id="32186-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="32186-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="32186-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="32186-112">Child elements</span></span>

|<span data-ttu-id="32186-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="32186-113">**Element**</span></span>|<span data-ttu-id="32186-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="32186-114">**Type**</span></span>|<span data-ttu-id="32186-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="32186-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="32186-116">Row</span><span class="sxs-lookup"><span data-stu-id="32186-116">Row</span></span>](row-element-action-tag-sectionvisio-xml.md) <br/> |[<span data-ttu-id="32186-117">ActionTagRow_Type</span><span class="sxs-lookup"><span data-stu-id="32186-117">ActionTagRow_Type</span></span>](actiontagrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="32186-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="32186-118">Attributes</span></span>

<span data-ttu-id="32186-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="32186-119">None.</span></span>
  

