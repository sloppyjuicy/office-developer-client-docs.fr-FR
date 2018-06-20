---
title: Section de formulaire Configuration de fichier [propriétés]
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f31a08ce-3a56-4c90-9502-5bcb09d8d80f
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: f582322c8ba2ffa0369792e531adf1ec4ccb3e28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783361"
---
# <a name="form-configuration-file-properties-section"></a><span data-ttu-id="cf952-103">Section de formulaire Configuration de fichier [propriétés]</span><span class="sxs-lookup"><span data-stu-id="cf952-103">Form Configuration File [Properties] Section</span></span>

  
  
<span data-ttu-id="cf952-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf952-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf952-105">La section **[propriétés]** répertorie l’ensemble complet des propriétés qui utilise le formulaire et qui publie ; Autrement dit, les propriétés qu’il crée dans ses messages personnalisés que MAPI client applications peuvent utiliser lors de l’affichage des colonnes, le filtrage des tables de contenu, configuration des dossiers de résultats de recherche et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="cf952-105">The **[Properties]** section lists the complete set of properties that the form uses and publishes; that is, the properties it creates in its custom messages that MAPI client applications can use when displaying columns, filtering contents tables, setting up search-results folders, and so on.</span></span> <span data-ttu-id="cf952-106">Chaque entrée de liste de cette propriété fait référence suivante **[propriété.**</span><span class="sxs-lookup"><span data-stu-id="cf952-106">Each entry in this property list references a subsequent **[Property.**</span></span> <span data-ttu-id="cf952-107">_chaîne_ section **]** comme suit indiqué.</span><span class="sxs-lookup"><span data-stu-id="cf952-107">_string_ **]** section as shown following.</span></span> 
  
 <span data-ttu-id="cf952-108">**[Propriétés]**</span><span class="sxs-lookup"><span data-stu-id="cf952-108">**[Properties]**</span></span>
  
 <span data-ttu-id="cf952-109">**Propriété.**</span><span class="sxs-lookup"><span data-stu-id="cf952-109">**Property.**</span></span> <span data-ttu-id="cf952-110">_chaîne_ =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-110">_string_ =  _string_</span></span>
  
<span data-ttu-id="cf952-111">Le format d’un [ **propriété.**</span><span class="sxs-lookup"><span data-stu-id="cf952-111">The format of a [ **Property.**</span></span> <span data-ttu-id="cf952-112">_chaîne_] section est la suivante :</span><span class="sxs-lookup"><span data-stu-id="cf952-112">_string_] section is:</span></span> 
  
 <span data-ttu-id="cf952-113">**[Property.**</span><span class="sxs-lookup"><span data-stu-id="cf952-113">**[Property.**</span></span> <span data-ttu-id="cf952-114">_chaîne_ **]**</span><span class="sxs-lookup"><span data-stu-id="cf952-114">_string_ **]**</span></span>
  
 <span data-ttu-id="cf952-115">**Type de** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-115">**Type** =  _integer_</span></span>
  
 <span data-ttu-id="cf952-116">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="cf952-116">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="cf952-117">**NmidString** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-117">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="cf952-118">**Touche** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-118">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="cf952-119">**DisplayName** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-119">**DisplayName** =  _string_</span></span>
  
 <span data-ttu-id="cf952-120">**Indicateurs** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-120">**Flags** =  _integer_</span></span>
  
 <span data-ttu-id="cf952-121">**SpecialType** = 0 | 1</span><span class="sxs-lookup"><span data-stu-id="cf952-121">**SpecialType** = 0|1</span></span> 
  
 <span data-ttu-id="cf952-122">**Enum1** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-122">**Enum1** =  _string_</span></span>
  
<span data-ttu-id="cf952-123">Chaque **[propriété.**</span><span class="sxs-lookup"><span data-stu-id="cf952-123">Each **[Property.**</span></span> <span data-ttu-id="cf952-124">_chaîne_ section **]** décrit une propriété unique.</span><span class="sxs-lookup"><span data-stu-id="cf952-124">_string_ **]** section describes a single property.</span></span> <span data-ttu-id="cf952-125">L’entrée de **Type** Spécifie le type de propriété MAPI, par exemple 3 (PT_I4), de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cf952-125">The **Type** entry specifies the MAPI property type, for example 3 (PT_I4), of the property.</span></span> <span data-ttu-id="cf952-126">L’entrée **NmidPropset** est facultative ; avec l’entrée **NmidString** ou la **touche** entrée, l’entrée **NmidPropset** donne le nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cf952-126">The **NmidPropset** entry is optional; together with either the **NmidString** entry or the **NmidInteger** entry, the **NmidPropset** entry gives the name of the property.</span></span> <span data-ttu-id="cf952-127">**NmidString** attribue le nom de la propriété, tandis que la **touche** donne l’identificateur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cf952-127">**NmidString** gives the name of the property, while **NmidInteger** gives the identifier of the property.</span></span> <span data-ttu-id="cf952-128">**NmidString** et **nécessite** s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="cf952-128">**NmidString** and **NmidInteger** are mutually exclusive.</span></span> 
  
<span data-ttu-id="cf952-129">Si set, **NmidPropset** doit contenir le nom du jeu de propriétés ; Si absent, **NmidPropset** est défini sur une valeur par défaut en fonction de la règle suivante : si la **touche** est présente et que sa valeur est inférieure à 0 x 8000, **NmidPropset** est défini sur PS_MAPI.</span><span class="sxs-lookup"><span data-stu-id="cf952-129">If set, **NmidPropset** should contain the name of the property set; if absent, **NmidPropset** is set to a default based on the following rule: If **NmidInteger** is present and its value is less than 0x8000, **NmidPropset** is set to PS_MAPI.</span></span> <span data-ttu-id="cf952-130">Si la valeur de la **touche** est définie à un nombre entier supérieure à 0 x 8000, ou si elle est absente, **NmidPropset** est définie sur PS_PUBLIC_STRINGS.</span><span class="sxs-lookup"><span data-stu-id="cf952-130">If the value of **NmidInteger** is set to an integer greater than 0x8000, or if it is absent, **NmidPropset** is set to PS_PUBLIC_STRINGS.</span></span> 
  
<span data-ttu-id="cf952-131">L’entrée **DisplayName** contient l’étiquette de la propriété.</span><span class="sxs-lookup"><span data-stu-id="cf952-131">The **DisplayName** entry contains the label for the property.</span></span> <span data-ttu-id="cf952-132">L’entrée **SpecialType** , si présent et différente de zéro indique que cette propriété est une propriété spéciale.</span><span class="sxs-lookup"><span data-stu-id="cf952-132">The **SpecialType** entry, if present and nonzero indicates that this property is a special property.</span></span> <span data-ttu-id="cf952-133">À présent, le type de propriété spéciale uniquement défini est **SpecialType** = 1, ce qui indique les propriétés de la chaîne énumérée.</span><span class="sxs-lookup"><span data-stu-id="cf952-133">At present, the only special property type defined is **SpecialType** = 1, which indicates string enumerated properties.</span></span> <span data-ttu-id="cf952-134">Si **SpecialType** est défini sur 1, l’entrée **Enum1** fait référence à la **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="cf952-134">If **SpecialType** is set to 1, the **Enum1** entry references the **[Enum1.**</span></span> <span data-ttu-id="cf952-135">_chaîne_ section **]** .</span><span class="sxs-lookup"><span data-stu-id="cf952-135">_string_ **]** section.</span></span> 
  
<span data-ttu-id="cf952-136">Voici un exemple d’une section **[propriétés]** et **[Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="cf952-136">Following is an example of a **[Properties]** section and a **[Properties.**</span></span> <span data-ttu-id="cf952-137">_chaîne_ section **]** .</span><span class="sxs-lookup"><span data-stu-id="cf952-137">_string_ **]** section.</span></span> 
  
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

<span data-ttu-id="cf952-138">L’entrée **Enum1** dans les références d’exemple précédent d’un **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="cf952-138">The **Enum1** entry in the preceeding example references to a subsequent **[Enum1.**</span></span> <span data-ttu-id="cf952-139">_chaîne_ section **]** décrivant une énumération d’un type particulier.</span><span class="sxs-lookup"><span data-stu-id="cf952-139">_string_ **]** section describing an enumeration of a particular type.</span></span> <span data-ttu-id="cf952-140">Cette énumération associe la première propriété de la **[propriété.**</span><span class="sxs-lookup"><span data-stu-id="cf952-140">Such an enumeration associates the first property in the **[Property.**</span></span> <span data-ttu-id="cf952-141">_chaîne_ section **]** avec une propriété entière, appelé l’index.</span><span class="sxs-lookup"><span data-stu-id="cf952-141">_string_ **]** section with an integer property, called the index.</span></span> <span data-ttu-id="cf952-142">Cette énumération contient également une liste de la paire d’affichage-index peut prendre les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="cf952-142">Such an enumeration also contains a list of the possible values that the display-index pair can assume.</span></span> <span data-ttu-id="cf952-143">Spécification d’un type de propriété pour l’énumération n’est pas nécessaire, car, par définition une entrée **Enum1** a toujours le type PT_I4.</span><span class="sxs-lookup"><span data-stu-id="cf952-143">Specifying a property type for the enumeration is unnecessary because by definition an **Enum1** entry always has the PT_I4 type.</span></span> <span data-ttu-id="cf952-144">Le format de la **[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="cf952-144">The format for the **[Enum1.**</span></span> <span data-ttu-id="cf952-145">_chaîne_ section **]** est :</span><span class="sxs-lookup"><span data-stu-id="cf952-145">_string_ **]** section is:</span></span> 
  
 <span data-ttu-id="cf952-146">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="cf952-146">**[Enum1.**</span></span> <span data-ttu-id="cf952-147">_chaîne_ **]**</span><span class="sxs-lookup"><span data-stu-id="cf952-147">_string_ **]**</span></span>
  
 <span data-ttu-id="cf952-148">**NmidPropset** =  _guid_</span><span class="sxs-lookup"><span data-stu-id="cf952-148">**NmidPropset** =  _guid_</span></span>
  
 <span data-ttu-id="cf952-149">**NmidString** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-149">**NmidString** =  _string_</span></span>
  
 <span data-ttu-id="cf952-150">**Touche** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-150">**NmidInteger** =  _integer_</span></span>
  
 <span data-ttu-id="cf952-151">**EnumCount** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-151">**EnumCount** =  _integer_</span></span>
  
 <span data-ttu-id="cf952-152">**Val.**</span><span class="sxs-lookup"><span data-stu-id="cf952-152">**Val.**</span></span> <span data-ttu-id="cf952-153">_entier_ **. Affichage** =  _chaîne_</span><span class="sxs-lookup"><span data-stu-id="cf952-153">_integer_ **.Display** =  _string_</span></span>
  
 <span data-ttu-id="cf952-154">**Val.**</span><span class="sxs-lookup"><span data-stu-id="cf952-154">**Val.**</span></span> <span data-ttu-id="cf952-155">_entier_ **. Index** =  _entier_</span><span class="sxs-lookup"><span data-stu-id="cf952-155">_integer_ **.Index** =  _integer_</span></span>
  
<span data-ttu-id="cf952-156">Voici un exemple de définition de propriété pour une propriété énumérée nommée risque d’incendie avec les valeurs possibles de faible, moyen et élevé.</span><span class="sxs-lookup"><span data-stu-id="cf952-156">The following is an example property definition for an enumerated property named Fire Hazard with possible values of Low, Medium, and High.</span></span>
  
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

 <span data-ttu-id="cf952-157">**[Enum1.**</span><span class="sxs-lookup"><span data-stu-id="cf952-157">**[Enum1.**</span></span> <span data-ttu-id="cf952-158">_chaîne_ sections **]** peuvent être utilisées par les applications pour deux raisons : pour accélérer le filtrage de propriétés à l’aide de l’index au lieu de la chaîne et pour trier selon un ordre différent de celui de l’ordre alphanumérique des valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="cf952-158">_string_ **]** sections can be used by applications for two purposes: to speed up the filtering of properties by using the index instead of the string and to sort by a different order than the alphanumeric order of the string values.</span></span> <span data-ttu-id="cf952-159">Par exemple, le tri peut être effectué en fonction de l’ordre de faible moyen élevé au lieu d’ordre haut-bas moyenne.</span><span class="sxs-lookup"><span data-stu-id="cf952-159">For example, sorting could be done based on Low-Medium-High order instead of High-Medium-Low order.</span></span> 
  

