---
title: Exemple de flux PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 63a8141221c0ff7a8c6ffee20587b682386f87b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406660"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="f0511-103">Exemple de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f0511-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="f0511-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f0511-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f0511-105">Cette rubrique décrit un exemple de flux PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="f0511-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="f0511-106">Le flux contient une définition d'un champ défini par l'utilisateur `TextField1`,.</span><span class="sxs-lookup"><span data-stu-id="f0511-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="f0511-107">Le type est **Text**et la définition est au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="f0511-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="f0511-108">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="f0511-108">Data dump</span></span>

<span data-ttu-id="f0511-109">Voici un dump des données du flux tel qu'il s'afficherait dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="f0511-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="f0511-110">Décalage de flux</span><span class="sxs-lookup"><span data-stu-id="f0511-110">Stream offset</span></span>|<span data-ttu-id="f0511-111">Octets de données</span><span class="sxs-lookup"><span data-stu-id="f0511-111">Data bytes</span></span>|<span data-ttu-id="f0511-112">Données ASCII</span><span class="sxs-lookup"><span data-stu-id="f0511-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="f0511-113">Voici une analyse des exemples de données pour le flux PropertyDefinition:</span><span class="sxs-lookup"><span data-stu-id="f0511-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="f0511-114">Version: offset 0x0, 2 octets: 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="f0511-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="f0511-115">FieldDefinitionCount: offset 0X2, 4 octets: 0x1 (1).</span><span class="sxs-lookup"><span data-stu-id="f0511-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="f0511-116">FieldDefinitions: décalage 0x6, tableau de 1 FieldDefinition Stream.</span><span class="sxs-lookup"><span data-stu-id="f0511-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="f0511-117">Flags: décalage 0x6, 4 octets: 0x45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="f0511-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="f0511-118">VT: décalage 0xA, 2 octets: 0x8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="f0511-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="f0511-119">DispId: décalage 0xC, 4 octets: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="f0511-120">NmidNameLength: offset 0x10, 2 octets: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f0511-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="f0511-121">NmidName: offset 0x12, tableau de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="f0511-122">Valeur de chaîne Unicode: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="f0511-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f0511-123">NameANSI: décalage 0x26, flux de PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f0511-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f0511-124">Longueur: décalage 0x26, 1 octet: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f0511-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="f0511-125">Caractères: décalage 0x27, tableau de 10 caractères.</span><span class="sxs-lookup"><span data-stu-id="f0511-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="f0511-126">Valeur de chaîne ANSI: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="f0511-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f0511-127">FormulaANSI: décalage 0x31, flux de PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f0511-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f0511-128">Longueur: décalage 0x31, 1 octet: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f0511-129">Caractères: décalage 0x32, tableau de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="f0511-130">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="f0511-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f0511-131">ValidationRuleANSI: décalage 0x32, PackedAnsiString Stream.</span><span class="sxs-lookup"><span data-stu-id="f0511-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f0511-132">Longueur: décalage 0x32, 1 octet: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f0511-133">Caractères: décalage 0x33, tableau de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="f0511-134">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="f0511-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f0511-135">ValidationTextANSI: décalage 0x33, flux de PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f0511-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f0511-136">Longueur: décalage 0x33, 1 octet: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f0511-137">Caractères: décalage 0x34, tableau de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="f0511-138">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="f0511-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f0511-139">ErrorANSI: décalage 0x34, flux de PackedAnsiString.</span><span class="sxs-lookup"><span data-stu-id="f0511-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="f0511-140">Longueur: décalage 0x34, 1 octet: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="f0511-141">Caractères: décalage 0x35, tableau de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="f0511-142">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="f0511-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="f0511-143">InternalType: décalage 0x35, 4 octets: 0x0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="f0511-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="f0511-144">SkipBlocks: décalage 0x39, série de flux de SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="f0511-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="f0511-145">Première SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f0511-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="f0511-146">Taille: décalage 0x39, 4 octets: 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="f0511-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="f0511-147">Content: offset 0x3D, tableau de 21 octets.</span><span class="sxs-lookup"><span data-stu-id="f0511-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="f0511-148">Il s'agit du premier flux SkipBlock, de sorte que ce tableau contient un flux de FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="f0511-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="f0511-149">FieldName: offset 0x3D, PackedUnicodeString Stream.</span><span class="sxs-lookup"><span data-stu-id="f0511-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="f0511-150">Longueur: décalage 0x3D, 1 octet: 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="f0511-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="f0511-151">Caractères: décalage 0x3E, tableau de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="f0511-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="f0511-152">Valeur de chaîne Unicode: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="f0511-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="f0511-153">Deuxième SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f0511-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="f0511-154">Taille: décalage 0x52, 4 octets: 0x0 (0).</span><span class="sxs-lookup"><span data-stu-id="f0511-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="f0511-155">Il s'agit du flux de SkipBlock de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0511-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f0511-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0511-156">See also</span></span>

- [<span data-ttu-id="f0511-157">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="f0511-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="f0511-158">Structures de flux</span><span class="sxs-lookup"><span data-stu-id="f0511-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="f0511-159">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="f0511-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="f0511-160">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="f0511-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="f0511-161">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="f0511-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="f0511-162">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="f0511-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="f0511-163">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="f0511-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="f0511-164">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="f0511-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

