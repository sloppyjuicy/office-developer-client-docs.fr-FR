---
title: attMAPIProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 806270c1-30e4-494e-9b03-7d1f2fc04099
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 185bfbb151c4f8d4e36b40b94393d14d50c33edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410454"
---
# <a name="attmapiprops"></a><span data-ttu-id="6c29c-103">attMAPIProps</span><span class="sxs-lookup"><span data-stu-id="6c29c-103">attMAPIProps</span></span>

  
  
<span data-ttu-id="6c29c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c29c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c29c-105">**L’attribut attMAPIProps** est spécial en ce sens qu’il peut être utilisé pour encoder n’importe quelle propriété MAPI qui n’a pas d’équivalent dans l’ensemble des attributs définis par TNEF existants.</span><span class="sxs-lookup"><span data-stu-id="6c29c-105">The **attMAPIProps** attribute is special in that it can be used to encode any MAPI property that does not have a counterpart in the set of existing TNEF-defined attributes.</span></span> <span data-ttu-id="6c29c-106">Les données d’attribut sont un ensemble compté de propriétés MAPI disposés de bout en bout.</span><span class="sxs-lookup"><span data-stu-id="6c29c-106">The attribute data is a counted set of MAPI properties laid end-to-end.</span></span> <span data-ttu-id="6c29c-107">Le format de ce codage, qui autorise tout ensemble de propriétés MAPI, est le suivant :</span><span class="sxs-lookup"><span data-stu-id="6c29c-107">The format of this encoding, which allows for any set of MAPI properties, is as follows:</span></span>  
  
 <span data-ttu-id="6c29c-108">_Property_Seq :_</span><span class="sxs-lookup"><span data-stu-id="6c29c-108">_Property_Seq:_</span></span>
  
> <span data-ttu-id="6c29c-109">propriété-count  _Property_Value,..._</span><span class="sxs-lookup"><span data-stu-id="6c29c-109">property-count  _Property_Value,..._</span></span>
    
<span data-ttu-id="6c29c-110">Il doit y avoir autant  _d Property_Value_ que la valeur du nombre de propriétés l’indique.</span><span class="sxs-lookup"><span data-stu-id="6c29c-110">There must be as many  _Property_Value_ items as the property-count value indicates.</span></span> 
  
 <span data-ttu-id="6c29c-111">_Property_Value :_</span><span class="sxs-lookup"><span data-stu-id="6c29c-111">_Property_Value:_</span></span>
  
> <span data-ttu-id="6c29c-112">property-tag _Property_property-tag  _Proptag_Name Property_</span><span class="sxs-lookup"><span data-stu-id="6c29c-112">property-tag  _Property_property-tag  _Proptag_Name Property_</span></span>
    
<span data-ttu-id="6c29c-113">La balise de propriété est simplement la valeur associée à l’identificateur de propriété, telle que 0x0037001F pour **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6c29c-113">The property-tag is simply the value associated with the property identifier, such as 0x0037001F for **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)).</span></span>
  
 <span data-ttu-id="6c29c-114">_Propriété :_</span><span class="sxs-lookup"><span data-stu-id="6c29c-114">_Property:_</span></span>
  
>  <span data-ttu-id="6c29c-115">_Value-count_  _Value,..._</span><span class="sxs-lookup"><span data-stu-id="6c29c-115">_Value_ value-count  _Value,..._</span></span>
    
 <span data-ttu-id="6c29c-116">_Valeur :_</span><span class="sxs-lookup"><span data-stu-id="6c29c-116">_Value:_</span></span>
  
> <span data-ttu-id="6c29c-117">value-data value-size value-data padding value-size value-IID value-data padding</span><span class="sxs-lookup"><span data-stu-id="6c29c-117">value-data value-size value-data padding value-size value-IID value-data padding</span></span>
    
 <span data-ttu-id="6c29c-118">_Proptag_Name :_</span><span class="sxs-lookup"><span data-stu-id="6c29c-118">_Proptag_Name:_</span></span>
  
> <span data-ttu-id="6c29c-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span><span class="sxs-lookup"><span data-stu-id="6c29c-119">name-guid name-kind name-id name-guid name-kind name-string-length name-string padding</span></span>
    
<span data-ttu-id="6c29c-120">L’encapsulation de chaque propriété varie en fonction de l’identificateur de propriété et du type de propriété.</span><span class="sxs-lookup"><span data-stu-id="6c29c-120">The encapsulation of each property varies based on the property identifier and the property type.</span></span> <span data-ttu-id="6c29c-121">Les balises de propriété, les identificateurs et les types sont définis dans les fichiers d’en-tête Mapitags.h et Mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="6c29c-121">Property tags, identifiers, and types are defined in the Mapitags.h and Mapidefs.h header files.</span></span>
  
<span data-ttu-id="6c29c-122">Si la propriété est une propriété nommée, la balise de propriété est immédiatement suivie du nom de la propriété MAPI, constitué d’un identificateur global unique (GUID), d’un type et d’un identificateur ou d’une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="6c29c-122">If the property is a named property, then the property tag is immediately followed by the MAPI property name, consisting of a globally unique identifier (GUID), a type, and either an identifier or a Unicode string.</span></span>
  
<span data-ttu-id="6c29c-123">Les propriétés à valeurs multiples et les propriétés avec des valeurs de longueur variable, telles que les types de propriétés PT_BINARY, PT_STRING8, PT_UNICODE ou PT_OBJECT, sont traitées de la manière suivante.</span><span class="sxs-lookup"><span data-stu-id="6c29c-123">Multivalued properties and properties with variable length values, such as the PT_BINARY, PT_STRING8, PT_UNICODE, or PT_OBJECT property types, are treated in the following way.</span></span> <span data-ttu-id="6c29c-124">Tout d’abord, le nombre de valeurs, codées comme un long non signé 32 bits, est placé dans le flux TNEF, suivi des valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="6c29c-124">First the number of values, encoded as a 32-bit unsigned long, is placed in the TNEF stream, followed by the individual values.</span></span> <span data-ttu-id="6c29c-125">Les données de valeur de chaque propriété sont codées en tant que taille en octets, suivies des données de valeur proprement dite.</span><span class="sxs-lookup"><span data-stu-id="6c29c-125">Each property's value-data is encoded as its size in bytes followed by the value-data itself.</span></span> <span data-ttu-id="6c29c-126">Les données de valeur sont ajoutées à une limite de 4 byte, bien que la quantité de remplissage ne soit pas incluse dans la taille de la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c29c-126">The value-data is padded out to a 4-byte boundary, although the amount of padding is not included in the value-size.</span></span>
  
<span data-ttu-id="6c29c-127">Si la propriété est de type PT_OBJECT, la taille de la valeur est suivie de l’identificateur d’interface de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6c29c-127">If the property is of type PT_OBJECT, the value-size is followed by the interface identifier of the object.</span></span> <span data-ttu-id="6c29c-128">L’implémentation actuelle de TNEF prend uniquement en charge les identificateurs IID_IMessage, IID_IStorage et IID_Istream’interface.</span><span class="sxs-lookup"><span data-stu-id="6c29c-128">The current implementation of TNEF only supports the IID_IMessage, IID_IStorage, and IID_Istream interface identifiers.</span></span> <span data-ttu-id="6c29c-129">La taille de l’identificateur d’interface est incluse dans la taille de la valeur.</span><span class="sxs-lookup"><span data-stu-id="6c29c-129">The size of the interface identifier is included in the value-size.</span></span>
  
<span data-ttu-id="6c29c-130">Si l’objet est un message incorporé (c’est-à-dire qu’il possède un type de propriété de PT_OBJECT et un identificateur d’interface de IID_Imessage), les données de valeur sont codées en tant que flux TNEF incorporé.</span><span class="sxs-lookup"><span data-stu-id="6c29c-130">If the object is an embedded message (that is, it has a property type of PT_OBJECT and an interface identifier of IID_Imessage), the value data is encoded as an embedded TNEF stream.</span></span> <span data-ttu-id="6c29c-131">Le codage réel d’un message incorporé dans l’implémentation TNEF s’fait en ouvrant un deuxième objet TNEF pour le flux d’origine et en traitant le flux incorporé.</span><span class="sxs-lookup"><span data-stu-id="6c29c-131">The actual encoding of an embedded message in TNEF implementation is done by opening a second TNEF object for the original stream and processing the stream inline.</span></span>
  

