---
title: Issues_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f326e227-f68e-27d6-268e-1ae935516dbc
ms.openlocfilehash: 160afddb1352a93050496a9b3497a3e3b6f2e585
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538108"
---
# <a name="issues_type-complextype-visio-xml"></a><span data-ttu-id="c3c9a-102">Issues_Type complexType (Visio XML)</span><span class="sxs-lookup"><span data-stu-id="c3c9a-102">Issues_Type complexType (Visio XML)</span></span>

## <a name="type-information"></a><span data-ttu-id="c3c9a-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="c3c9a-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3c9a-104">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="c3c9a-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-105">**Schema file**</span></span> <br/> |<span data-ttu-id="c3c9a-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="c3c9a-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="c3c9a-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-107">**Extension base**</span></span> <br/> |<span data-ttu-id="c3c9a-108">Aucun</span><span class="sxs-lookup"><span data-stu-id="c3c9a-108">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3c9a-109">Définition</span><span class="sxs-lookup"><span data-stu-id="c3c9a-109">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3c9a-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="c3c9a-110">Elements and attributes</span></span>

<span data-ttu-id="c3c9a-111">Si le schéma définit des exigences spécifiques, telles que **séquence**, **minOccurs**, **maxOccurs** et **choix**, voir la section de définition.</span><span class="sxs-lookup"><span data-stu-id="c3c9a-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="c3c9a-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c3c9a-112">Child elements</span></span>

|<span data-ttu-id="c3c9a-113">**Élément**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-113">**Element**</span></span>|<span data-ttu-id="c3c9a-114">**Type (Type)**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-114">**Type**</span></span>|<span data-ttu-id="c3c9a-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="c3c9a-115">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3c9a-116">Problème</span><span class="sxs-lookup"><span data-stu-id="c3c9a-116">Issue</span></span>](issue-element-issues_type-complextypevisio-xml.md) <br/> |[<span data-ttu-id="c3c9a-117">Issue_Type</span><span class="sxs-lookup"><span data-stu-id="c3c9a-117">Issue_Type</span></span>](issue_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a><span data-ttu-id="c3c9a-118">Attributs</span><span class="sxs-lookup"><span data-stu-id="c3c9a-118">Attributes</span></span>

<span data-ttu-id="c3c9a-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c3c9a-119">None.</span></span>
  

