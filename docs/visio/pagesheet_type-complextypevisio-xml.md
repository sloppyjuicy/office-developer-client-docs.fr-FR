---
title: Type complexe PageSheet_Type (« Visio XML »)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f7bce473-9a3d-65f2-8323-1e00db110c71
ms.openlocfilehash: 70cd45ad803f9342b582f324b31f12ac5dff54c8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789217"
---
# <a name="pagesheettype-complextype-visio-xml"></a><span data-ttu-id="77b71-102">Type complexe PageSheet_Type (« Visio XML »)</span><span class="sxs-lookup"><span data-stu-id="77b71-102">PageSheet_Type complexType ('Visio XML')</span></span>

## <a name="type-information"></a><span data-ttu-id="77b71-103">Informations sur le type</span><span class="sxs-lookup"><span data-stu-id="77b71-103">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="77b71-104">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="77b71-104">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|<span data-ttu-id="77b71-105">**Fichier de schéma**</span><span class="sxs-lookup"><span data-stu-id="77b71-105">**Schema file**</span></span> <br/> |<span data-ttu-id="77b71-106">VisioSchema15-2012-06-05.xsd</span><span class="sxs-lookup"><span data-stu-id="77b71-106">VisioSchema15-2012-06-05.xsd</span></span>  <br/> |
|<span data-ttu-id="77b71-107">**Base d’extension**</span><span class="sxs-lookup"><span data-stu-id="77b71-107">**Extension base**</span></span> <br/> |<span data-ttu-id="77b71-108">Sheet_Type</span><span class="sxs-lookup"><span data-stu-id="77b71-108">Sheet_Type</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="77b71-109">Définition</span><span class="sxs-lookup"><span data-stu-id="77b71-109">Definition</span></span>

```XML
      <xs:complexType name="PageSheet_Type">
        <xs:complexContent>
        <xs:extension base="Sheet_Type">
      
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a><span data-ttu-id="77b71-110">Éléments et attributs</span><span class="sxs-lookup"><span data-stu-id="77b71-110">Elements and attributes</span></span>

<span data-ttu-id="77b71-111">Si le schéma définit des exigences spécifiques, telles que **sequence**, **minOccurs**, **maxOccurs**et **choice**, voir la section Définition.</span><span class="sxs-lookup"><span data-stu-id="77b71-111">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="77b71-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="77b71-112">Child elements</span></span>

<span data-ttu-id="77b71-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="77b71-113">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="77b71-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="77b71-114">Attributes</span></span>

|<span data-ttu-id="77b71-115">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="77b71-115">**Attribute**</span></span>|<span data-ttu-id="77b71-116">**Type**</span><span class="sxs-lookup"><span data-stu-id="77b71-116">**Type**</span></span>|<span data-ttu-id="77b71-117">**Obligatoire**</span><span class="sxs-lookup"><span data-stu-id="77b71-117">**Required**</span></span>|<span data-ttu-id="77b71-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="77b71-118">**Description**</span></span>|<span data-ttu-id="77b71-119">**Valeurs possibles**</span><span class="sxs-lookup"><span data-stu-id="77b71-119">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="77b71-120">UniqueID</span><span class="sxs-lookup"><span data-stu-id="77b71-120">UniqueID</span></span>  <br/> |<span data-ttu-id="77b71-121">XSD : String</span><span class="sxs-lookup"><span data-stu-id="77b71-121">xsd:string</span></span>  <br/> |<span data-ttu-id="77b71-122">facultatif</span><span class="sxs-lookup"><span data-stu-id="77b71-122">optional</span></span>  <br/> ||<span data-ttu-id="77b71-123">Valeurs du type xsd : String.</span><span class="sxs-lookup"><span data-stu-id="77b71-123">Values of the xsd:string type.</span></span>  <br/> |
   

