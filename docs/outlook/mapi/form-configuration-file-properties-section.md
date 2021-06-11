---
title: Section Fichier de configuration de formulaire [Propriétés]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 86d2257b821622094ff8d5ad3a5d7b1bfc74942b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421290"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="0aa4d-103">Section Fichier de configuration de formulaire [Propriétés]</span><span class="sxs-lookup"><span data-stu-id="0aa4d-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="0aa4d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0aa4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0aa4d-105">La section **[Propriétés]** répertorie l’ensemble complet des propriétés que le formulaire utilise et publie ; autrement dit, les propriétés qu’elle crée dans ses messages personnalisés que les applications clientes MAPI peuvent utiliser lors de l’affichage des colonnes, du filtrage des tables des matières, de la configuration de dossiers de résultats de recherche, etc.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="0aa4d-106">Chaque entrée de cette liste de propriétés fait référence à une **autre [Propriété.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="0aa4d-107">_section_ **de chaîne ]** comme illustré ci-après.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="0aa4d-108">**[Propriétés]**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-108">**[Properties]**</span></span>
  
 <span data-ttu-id="0aa4d-109">**Propriété.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-109">**Property.**</span></span> <span data-ttu-id="0aa4d-110">_string_  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="0aa4d-111">Format d’un [ **Propriété.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-111">The format of a [ **Property.**</span></span> <span data-ttu-id="0aa4d-112">_string_] est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0aa4d-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="0aa4d-113">**[Propriété.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-113">**[Property.**</span></span> <span data-ttu-id="0aa4d-114">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-114">_string_ **]**</span></span>
  
 <span data-ttu-id="0aa4d-115">**Type**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="0aa4d-116">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="0aa4d-117">**NmidString**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="0aa4d-118">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="0aa4d-119">**DisplayName**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="0aa4d-120">**Indicateurs**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="0aa4d-121">**SpecialType** = 0|1</span><span class="sxs-lookup"><span data-stu-id="0aa4d-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="0aa4d-122">**Enum1**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="0aa4d-123">Chaque **[Propriété.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-123">Each **[Property.**</span></span> <span data-ttu-id="0aa4d-124">_section_ **]** décrit une seule propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="0aa4d-125">**L’entrée** Type spécifie le type de propriété MAPI, par exemple 3 (PT_I4), de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="0aa4d-126">**L’entrée NmidPropset** est facultative . avec l’entrée **NmidString** ou **NmidInteger,** l’entrée **NmidPropset** donne le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="0aa4d-127">**NmidString** donne le nom de la propriété, tandis que **NmidInteger** donne l’identificateur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="0aa4d-128">**NmidString et** **NmidInteger** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="0aa4d-129">S’il est définie, **NmidPropset** doit contenir le nom du jeu de propriétés ; En cas d’absence, **NmidPropset** est définie sur une valeur par défaut basée sur la règle suivante : si **NmidInteger** est présent et que sa valeur est inférieure à 0x8000, **NmidPropset** est définie sur PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="0aa4d-130">Si la valeur de **NmidInteger** est définie sur un nombre supérieur à 0x8000 ou si elle est absente, **NmidPropset** est définie sur PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="0aa4d-131">**L’entrée DisplayName** contient l’étiquette de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="0aa4d-132">**L’entrée SpecialType,** si elle est présente et non zéro, indique que cette propriété est une propriété spéciale.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="0aa4d-133">Pour l’instant, le seul type de propriété spécial défini est **SpecialType** = 1, qui indique les propriétés d’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="0aa4d-134">Si **SpecialType** est définie sur 1, l’entrée **Enum1** fait référence à **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="0aa4d-135">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="0aa4d-136">Voici un exemple de section **[Propriétés]** et **de [Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="0aa4d-137">_string_ **]** section.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-137">_string_ **]** section.</span></span> 
  
```cpp
[Properties]
Property.1 = Fire Hazard
Property.2 = Safe
[Property.Fire Hazard]
Type = 1
NmidPropSet = {E47F4480-8400-101B-934D-04021C007002]
NmidString = FireHazard
DisplayName = Fire Hazard
SpecialType = 1
Enum1 = HazardEnum

```

<span data-ttu-id="0aa4d-138">**L’entrée Enum1** dans l’exemple de précédation fait référence à une **autre [Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="0aa4d-139">_section_ **de chaîne ]** décrivant une éumération d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="0aa4d-140">Une telle éumération associe la première propriété de **[Property.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="0aa4d-141">_section_ **de chaîne ]** avec une propriété de l’ensemble, appelée index.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="0aa4d-142">Cette énumération contient également une liste des valeurs possibles que la paire d’index d’affichage peut supposer.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="0aa4d-143">Il n’est pas nécessaire de spécifier un type de propriété pour l’PT_I4 car, par définition, une entrée **Enum1** a toujours le type PT_I4.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="0aa4d-144">Format de **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="0aa4d-145">_la_ section **string ]** est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0aa4d-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="0aa4d-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-146">**[Enum1.**</span></span> <span data-ttu-id="0aa4d-147">_string_ **]**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-147">_string_ **]**</span></span>
  
 <span data-ttu-id="0aa4d-148">**NmidPropset**  =   _guid_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="0aa4d-149">**NmidString**  =   _string_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="0aa4d-150">**NmidInteger**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="0aa4d-151">**EnumCount**  =   _integer_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="0aa4d-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-152">**Val.**</span></span> <span data-ttu-id="0aa4d-153">_integer_ **. Chaîne d’affichage**  =   </span><span class="sxs-lookup"><span data-stu-id="0aa4d-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="0aa4d-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-154">**Val.**</span></span> <span data-ttu-id="0aa4d-155">_integer_ **.**  =   _Integer d’index_</span><span class="sxs-lookup"><span data-stu-id="0aa4d-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="0aa4d-156">Voici un exemple de définition de propriété pour une propriété éumée nommée Fire Danger avec des valeurs possibles de Low, Medium et High.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
```cpp
[Properties]
Property1 = Fire Hazard
[Enum1.HazardEnum]
IdxNmidPropset={E47F4480-8400-101B-934D-04021C007002]
IdxNmidString=FireHazardEnum
EnumCount = 3
Val.1.Display = Low
Val.1.Index = 1
Val.2.Display = Medium
Val.2.Index = 2
Val.3.Display = High
Val.3.Index = 3

```

 <span data-ttu-id="0aa4d-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="0aa4d-157">**[Enum1.**</span></span> <span data-ttu-id="0aa4d-158"> les sections string **]** peuvent être utilisées par les applications à deux fins : pour accélérer le filtrage des propriétés à l’aide de l’index au lieu de la chaîne et pour trier dans un ordre différent de l’ordre alphanumérique des valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="0aa4d-159">Par exemple, le tri peut être effectué en fonction de l’ordre faible-moyen-élevé au lieu de l’ordre Élevé-Moyen-Bas.</span><span class="sxs-lookup"><span data-stu-id="0aa4d-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

