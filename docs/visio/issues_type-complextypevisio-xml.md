---
title: Type complexe Issues_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 1ebec9e42c71b93637155037bd881c8ddf330367
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788878"
---
# <a name="issuestype-complextype-visio-xml"></a><span data-ttu-id="de0e1-102">Type complexe Issues_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="de0e1-102">Issues_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="de0e1-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="de0e1-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de0e1-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="de0e1-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="de0e1-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="de0e1-105">**Schema file**</span></span> <br/> |<span data-ttu-id="de0e1-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="de0e1-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="de0e1-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="de0e1-107">**Extension base**</span></span> <br/> |<span data-ttu-id="de0e1-108">Aucune</span><span class="sxs-lookup"><span data-stu-id="de0e1-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="de0e1-109">Définition</span><span class="sxs-lookup"><span data-stu-id="de0e1-109">Definition</span></span>

```XML
          <xs:complexType name="Issues_Type">
          
          <xs:sequence>
    <xs:element name="Issue"  type="Issue_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="de0e1-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="de0e1-110">Elements and attributes</span></span>

<span data-ttu-id="de0e1-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="de0e1-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="de0e1-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="de0e1-112">Child elements</span></span>

|<span data-ttu-id="de0e1-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="de0e1-113">**Element**</span></span>|<span data-ttu-id="de0e1-114">**Type**</span><span class="sxs-lookup"><span data-stu-id="de0e1-114">**Type**</span></span>|<span data-ttu-id="de0e1-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="de0e1-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="de0e1-116">Problème</span><span class="sxs-lookup"><span data-stu-id="de0e1-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="de0e1-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="de0e1-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="de0e1-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="de0e1-118">Attributes</span></span>

<span data-ttu-id="de0e1-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="de0e1-119">None.</span></span>
  

