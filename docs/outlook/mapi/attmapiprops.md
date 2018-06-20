---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: eef480e8b024565ab282fb242a36336cd17384a1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782952"
---
# <a name="attmapiprops"></a><span data-ttu-id="3eb82-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="3eb82-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="3eb82-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3eb82-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3eb82-105">L’attribut **attMAPIProps** est spécial en ce sens qu’il peut être utilisé pour encoder des propriétés MAPI qui n’ont pas un équivalent dans l’ensemble des attributs définis par le format TNEF existants.</span><span class="sxs-lookup"><span data-stu-id="3eb82-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="3eb82-106">Les données d’attribut sont un ensemble de propriétés MAPI définies de bout en bout compté.</span><span class="sxs-lookup"><span data-stu-id="3eb82-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="3eb82-107">Le format de codage, qui permet à n’importe quel jeu de propriétés MAPI, est comme suit :</span><span class="sxs-lookup"><span data-stu-id="3eb82-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="3eb82-108">_Property_Seq :_</span><span class="sxs-lookup"><span data-stu-id="3eb82-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="3eb82-109">compte de la propriété _nom..._</span><span class="sxs-lookup"><span data-stu-id="3eb82-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="3eb82-110">Il doit exister autant d’éléments _nom_ comme l’indique la valeur de nombre de propriétés.</span><span class="sxs-lookup"><span data-stu-id="3eb82-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="3eb82-111">_Nom :_</span><span class="sxs-lookup"><span data-stu-id="3eb82-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="3eb82-112">balise de propriété _Property_property-balise _Propriété Proptag_Name_</span><span class="sxs-lookup"><span data-stu-id="3eb82-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="3eb82-113">La balise de propriété est simplement la valeur associée à l’identificateur de la propriété, tel que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3eb82-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="3eb82-114">_Propriété :_</span><span class="sxs-lookup"><span data-stu-id="3eb82-114">_Property:_</span></span>
  
>  <span data-ttu-id="3eb82-115">_Valeur_ -nombre de valeurs _valeur..._</span><span class="sxs-lookup"><span data-stu-id="3eb82-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="3eb82-116">_Valeur :_</span><span class="sxs-lookup"><span data-stu-id="3eb82-116">_Value:_</span></span>
  
> <span data-ttu-id="3eb82-117">valeur-taille de la valeur valeur données-remplissage du remplissage de données de la valeur taille de la valeur valeur-IID</span><span class="sxs-lookup"><span data-stu-id="3eb82-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="3eb82-118">_Proptag_Name :_</span><span class="sxs-lookup"><span data-stu-id="3eb82-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="3eb82-119">remplissage de chaîne de nom guid-nom nom-id de type-nom nom-guid Nom-type longueur de chaîne de nom</span><span class="sxs-lookup"><span data-stu-id="3eb82-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="3eb82-120">L’encapsulation de chaque propriété varie en fonction de l’identificateur de propriété et le type de propriété.</span><span class="sxs-lookup"><span data-stu-id="3eb82-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="3eb82-121">Types, les identificateurs et les balises de propriété sont définies dans les fichiers d’en-tête Mapitags.h et Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="3eb82-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="3eb82-122">Si la propriété est une propriété nommée, la balise de propriété est immédiatement suivie par le nom de la propriété MAPI, constitué d’un identificateur global unique (GUID), un type et un identificateur ou une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="3eb82-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="3eb82-123">Propriétés à valeurs multiples et des propriétés avec les valeurs de longueur variable, telles que les types de propriété PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="3eb82-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="3eb82-124">Tout d’abord le nombre de valeurs, codées en tant que 32 bits long, non signée est placé dans le flux TNEF, suivi par les valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="3eb82-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="3eb82-125">Données de valeur de chaque propriété sont codée en tant que sa taille en octets, suivi par les données de valeur proprement dite.</span><span class="sxs-lookup"><span data-stu-id="3eb82-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="3eb82-126">Données de la valeur sont remplie avec une limite de 4 octets, bien que la taille de la marge n’est pas inclus dans la taille de la valeur.</span><span class="sxs-lookup"><span data-stu-id="3eb82-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="3eb82-127">Si la propriété est de type PT_OBJECT, la taille de la valeur est suivie de l’identificateur d’interface de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3eb82-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="3eb82-128">L’implémentation actuelle du format TNEF prend uniquement en charge les identificateurs d’interface IID_Istream, IID_IStorage et IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="3eb82-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="3eb82-129">La taille de l’identificateur d’interface est incluse dans la taille de la valeur.</span><span class="sxs-lookup"><span data-stu-id="3eb82-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="3eb82-130">Si l’objet est un message incorporé (autrement dit, elle possède un type de propriété de PT_OBJECT et un identificateur d’interface de IID_Imessage), la valeur des données sont codées en tant qu’un flux TNEF intégré.</span><span class="sxs-lookup"><span data-stu-id="3eb82-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="3eb82-131">Le codage d’un message incorporé dans implémentation TNEF est effectué en ouvrant un deuxième objet TNEF pour le flux d’origine et de traitement inline flux.</span><span class="sxs-lookup"><span data-stu-id="3eb82-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

