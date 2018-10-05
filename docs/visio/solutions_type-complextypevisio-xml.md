---
title: Type complexe Solutions_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: bf43b971399ec69c6f73cbfaaa6cade8c583d3c2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400536"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="089c1-102">Type complexe Solutions_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="089c1-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="089c1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="089c1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="089c1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="089c1-104">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="089c1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="089c1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="089c1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="089c1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="089c1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="089c1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="089c1-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="089c1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="089c1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="089c1-109">Definition</span></span>

```XML
          <xs:complexType name="Solutions_Type">
          
          <xs:sequence>
    <xs:element name="Solution"  type="Solution_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="089c1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="089c1-110">Elements and attributes</span></span>

<span data-ttu-id="089c1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="089c1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="089c1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="089c1-112">Child elements</span></span>

|<span data-ttu-id="089c1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="089c1-113">**Element**</span></span>|<span data-ttu-id="089c1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="089c1-114">**Type**</span></span>|<span data-ttu-id="089c1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="089c1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="089c1-116">Probl?me</span><span class="sxs-lookup"><span data-stu-id="089c1-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="089c1-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="089c1-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="089c1-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="089c1-118">Attributes</span></span>

<span data-ttu-id="089c1-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="089c1-119">None.</span></span>
  

