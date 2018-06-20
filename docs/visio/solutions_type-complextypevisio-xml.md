---
title: Type complexe Solutions_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74978183-8513-b359-0501-6094e072ac8e
ms.openlocfilehash: 69c5bf92bb9f72e9969f9687b42b9d583eb2a523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789791"
---
# <a name="solutionstype-complextype-visio-xml"></a><span data-ttu-id="68210-102">Type complexe Solutions_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="68210-102">Solutions_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="68210-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="68210-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="68210-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="68210-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="68210-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="68210-105">**Schema file**</span></span> <br/> |<span data-ttu-id="68210-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="68210-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="68210-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="68210-107">**Extension base**</span></span> <br/> |<span data-ttu-id="68210-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="68210-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="68210-109">Définition</span><span class="sxs-lookup"><span data-stu-id="68210-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="68210-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="68210-110">Elements and attributes</span></span>

<span data-ttu-id="68210-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="68210-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="68210-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="68210-112">Child elements</span></span>

|<span data-ttu-id="68210-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="68210-113">**Element**</span></span>|<span data-ttu-id="68210-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="68210-114">**Type**</span></span>|<span data-ttu-id="68210-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="68210-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="68210-116">Probl?me</span><span class="sxs-lookup"><span data-stu-id="68210-116">Solution</span></span>](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="68210-117">Solution_Type</span><span class="sxs-lookup"><span data-stu-id="68210-117">Solution_Type</span></span>](solution_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="68210-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="68210-118">Attributes</span></span>

<span data-ttu-id="68210-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="68210-119">None.</span></span>
  

