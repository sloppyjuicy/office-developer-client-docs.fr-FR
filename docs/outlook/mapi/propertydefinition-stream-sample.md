---
title: Exemple de flux de la définition PropertyDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7919f4d7-04df-4a96-a5b1-b7b460890486
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3d0c337bd3e5a73bbbcbb72a109320cfb84efd50
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786952"
---
# <a name="propertydefinition-stream-sample"></a><span data-ttu-id="9e620-103">Exemple de flux de la définition PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="9e620-103">PropertyDefinition stream sample</span></span>

<span data-ttu-id="9e620-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9e620-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9e620-105">Cette rubrique décrit un exemple d’un flux de la définition PropertyDefinition.</span><span class="sxs-lookup"><span data-stu-id="9e620-105">This topic describes an example of a PropertyDefinition stream.</span></span> <span data-ttu-id="9e620-106">Le flux contient une définition d’un champ défini par l’utilisateur, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="9e620-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="9e620-107">Le type est **texte**, et la définition est au format PropDefV2.</span><span class="sxs-lookup"><span data-stu-id="9e620-107">The type is **Text**, and the definition is in the PropDefV2 format.</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="9e620-108">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="9e620-108">Data dump</span></span>

<span data-ttu-id="9e620-109">Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="9e620-109">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="9e620-110">Décalage de flux</span><span class="sxs-lookup"><span data-stu-id="9e620-110">Stream offset</span></span>|<span data-ttu-id="9e620-111">Octets de données</span><span class="sxs-lookup"><span data-stu-id="9e620-111">Data bytes</span></span>|<span data-ttu-id="9e620-112">Données ASCII</span><span class="sxs-lookup"><span data-stu-id="9e620-112">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `03 01 01 00 00 00 45 00 00 00 08 00 00 00 00 00` <br/> | `???...E...?.....` <br/> |
| `0000000010` <br/> | `0A 00 54 00 65 00 78 00 74 00 46 00 69 00 65 00` <br/> | `?.T.e.x.t.F.i.e.` <br/> |
| `0000000020` <br/> | `6C 00 64 00 31 00 0A 54 65 78 74 46 69 65 6C 64` <br/> | `l.d.1.?TextField` <br/> |
| `0000000030` <br/> | `31 00 00 00 00 00 00 00 00 15 00 00 00 0A 54 00` <br/> | `1........?...?T.` <br/> |
| `0000000040` <br/> | `65 00 78 00 74 00 46 00 69 00 65 00 6C 00 64 00` <br/> | `e.x.t.F.i.e.l.d.` <br/> |
| `0000000050` <br/> | `31 00 00 00 00 00` <br/> | `1.....` <br/> |
   
<span data-ttu-id="9e620-113">Vous trouverez ci-dessous une analyse des données pour le flux de la définition PropertyDefinition :</span><span class="sxs-lookup"><span data-stu-id="9e620-113">The following is a parse of the sample data for the PropertyDefinition stream:</span></span>
  
- <span data-ttu-id="9e620-114">Version : Décalage de 0 x 0, 2 octets : 0x0103 (PropDefV2).</span><span class="sxs-lookup"><span data-stu-id="9e620-114">Version: Offset 0x0, 2 bytes: 0x0103 (PropDefV2).</span></span>
    
- <span data-ttu-id="9e620-115">FieldDefinitionCount : Décalage 0 x 2, 4 octets : 0 x 1 (1).</span><span class="sxs-lookup"><span data-stu-id="9e620-115">FieldDefinitionCount: Offset 0x2, 4 bytes: 0x1 (1).</span></span>
    
- <span data-ttu-id="9e620-116">FieldDefinitions : Décalage 0 x 6, tableau des flux de FieldDefinition 1.</span><span class="sxs-lookup"><span data-stu-id="9e620-116">FieldDefinitions: Offset 0x6, array of 1 FieldDefinition stream.</span></span>
    
  - <span data-ttu-id="9e620-117">Indicateurs : Décalage 0 x 6, 4 octets : 0 x 45 (PDO_IS_CUSTOM | PDO_PRINT_SAVEAS | PDO_PRINT_SAVEAS_DEF).</span><span class="sxs-lookup"><span data-stu-id="9e620-117">Flags: Offset 0x6, 4 bytes: 0x45 (PDO_IS_CUSTOM|PDO_PRINT_SAVEAS|PDO_PRINT_SAVEAS_DEF).</span></span>
    
  - <span data-ttu-id="9e620-118">VT : Décalage 0xA, 2 octets : 0 x 8 (**VT_BSTR**).</span><span class="sxs-lookup"><span data-stu-id="9e620-118">VT: Offset 0xA, 2 bytes: 0x8 (**VT_BSTR**).</span></span>
    
  - <span data-ttu-id="9e620-119">DispId : Décalage 0xC, 4 octets : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-119">DispId: Offset 0xC, 4 bytes: 0x0 (0).</span></span>
    
  - <span data-ttu-id="9e620-120">NmidNameLength : Décalage de 0 x 10, 2 octets : 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="9e620-120">NmidNameLength: Offset 0x10, 2 bytes: 0xA (10).</span></span>
    
  - <span data-ttu-id="9e620-121">NmidName : Décalage 0 x 12, tableau de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="9e620-121">NmidName: Offset 0x12, array of 10 WCHARs.</span></span> <span data-ttu-id="9e620-122">Valeur de chaîne Unicode : « TextField1 ».</span><span class="sxs-lookup"><span data-stu-id="9e620-122">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="9e620-123">NameANSI : Décalage 0 x 26, PackedAnsiString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-123">NameANSI: Offset 0x26, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="9e620-124">Longueur : Décalage de la 0 x 26, 1 octet : 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="9e620-124">Length: Offset 0x26, 1 byte: 0xA (10).</span></span>
      
    - <span data-ttu-id="9e620-125">De caractères : Décalage 0 x 27, tableau de 10 caractères.</span><span class="sxs-lookup"><span data-stu-id="9e620-125">Characters: Offset 0x27, array of 10 CHARs.</span></span> <span data-ttu-id="9e620-126">Valeur de chaîne ANSI : « TextField1 ».</span><span class="sxs-lookup"><span data-stu-id="9e620-126">ANSI string value: "TextField1".</span></span>
    
  - <span data-ttu-id="9e620-127">FormulaANSI : Décalage 0 x 31, PackedAnsiString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-127">FormulaANSI: Offset 0x31, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="9e620-128">Longueur : Décalage de la 0 x 31, 1 octet : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-128">Length: Offset 0x31, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="9e620-129">De caractères : Décalage 0 x 32, tableau de caractères de 0.</span><span class="sxs-lookup"><span data-stu-id="9e620-129">Characters: Offset 0x32, array of 0 CHARs.</span></span> <span data-ttu-id="9e620-130">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="9e620-130">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="9e620-131">ValidationRuleANSI : Décalage 0 x 32, PackedAnsiString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-131">ValidationRuleANSI: Offset 0x32, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="9e620-132">Longueur : Décalage de la 0 x 32, 1 octet : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-132">Length: Offset 0x32, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="9e620-133">De caractères : Décalage 0 x 33, tableau de caractères de 0.</span><span class="sxs-lookup"><span data-stu-id="9e620-133">Characters: Offset 0x33, array of 0 CHARs.</span></span> <span data-ttu-id="9e620-134">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="9e620-134">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="9e620-135">ValidationTextANSI : Décalage 0 x 33, PackedAnsiString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-135">ValidationTextANSI: Offset 0x33, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="9e620-136">Longueur : Décalage de la 0 x 33, 1 octet : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-136">Length: Offset 0x33, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="9e620-137">De caractères : Décalage 0 x 34, tableau de caractères de 0.</span><span class="sxs-lookup"><span data-stu-id="9e620-137">Characters: Offset 0x34, array of 0 CHARs.</span></span> <span data-ttu-id="9e620-138">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="9e620-138">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="9e620-139">ErrorANSI : Décalage 0 x 34, PackedAnsiString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-139">ErrorANSI: Offset 0x34, PackedAnsiString stream.</span></span>
    
    - <span data-ttu-id="9e620-140">Longueur : Décalage de la 0 x 34, 1 octet : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-140">Length: Offset 0x34, 1 byte: 0x0 (0).</span></span>
      
    - <span data-ttu-id="9e620-141">Caractères : Décalage 0x35, du tableau de caractères de 0.</span><span class="sxs-lookup"><span data-stu-id="9e620-141">Characters: Offset 0x35, array of 0 CHARs.</span></span> <span data-ttu-id="9e620-142">Chaîne ANSI vide.</span><span class="sxs-lookup"><span data-stu-id="9e620-142">Empty ANSI string.</span></span>
    
  - <span data-ttu-id="9e620-143">InternalType : Décalage 0x35, 4 octets : 0 x 0 (iTypeString).</span><span class="sxs-lookup"><span data-stu-id="9e620-143">InternalType: Offset 0x35, 4 bytes: 0x0 (iTypeString).</span></span>
    
  - <span data-ttu-id="9e620-144">SkipBlocks : Décalage 0 x 39, série de flux de données SkipBlock.</span><span class="sxs-lookup"><span data-stu-id="9e620-144">SkipBlocks: Offset 0x39, series of SkipBlock streams.</span></span>
    
  - <span data-ttu-id="9e620-145">Première SkipBlock</span><span class="sxs-lookup"><span data-stu-id="9e620-145">First SkipBlock</span></span>
    
    - <span data-ttu-id="9e620-146">Taille : Décalage 0 x 39, 4 octets : 0x15 (21).</span><span class="sxs-lookup"><span data-stu-id="9e620-146">Size: Offset 0x39, 4 bytes: 0x15 (21).</span></span>
      
    - <span data-ttu-id="9e620-147">Contenu : Décalage 0x3D, tableau d’octets 21.</span><span class="sxs-lookup"><span data-stu-id="9e620-147">Content: Offset 0x3D, array of 21 bytes.</span></span> <span data-ttu-id="9e620-148">Il s’agit du premier flux SkipBlock, afin que ce tableau contient un flux FirstSkipBlockContent.</span><span class="sxs-lookup"><span data-stu-id="9e620-148">This is the first SkipBlock stream, so this array contains a FirstSkipBlockContent stream.</span></span>
      
      - <span data-ttu-id="9e620-149">FieldName : Décalage 0x3D, PackedUnicodeString flux.</span><span class="sxs-lookup"><span data-stu-id="9e620-149">FieldName: Offset 0x3D, PackedUnicodeString stream.</span></span>
        
        - <span data-ttu-id="9e620-150">Durée : Décalage 0x3D, 1 octet : 0xA (10).</span><span class="sxs-lookup"><span data-stu-id="9e620-150">Length: Offset 0x3D, 1 byte: 0xA (10).</span></span>
          
        - <span data-ttu-id="9e620-151">De caractères : Décalage 0x3E, tableau de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="9e620-151">Characters: Offset 0x3E, array of 10 WCHARs.</span></span> <span data-ttu-id="9e620-152">Valeur de chaîne Unicode : « TextField1 ».</span><span class="sxs-lookup"><span data-stu-id="9e620-152">Unicode string value: "TextField1".</span></span>
    
  - <span data-ttu-id="9e620-153">Deuxième SkipBlock</span><span class="sxs-lookup"><span data-stu-id="9e620-153">Second SkipBlock</span></span>
    
    - <span data-ttu-id="9e620-154">Taille : Décalage 0 x 52, 4 octets : 0 x 0 (0).</span><span class="sxs-lookup"><span data-stu-id="9e620-154">Size: Offset 0x52, 4 bytes: 0x0 (0).</span></span> <span data-ttu-id="9e620-155">Il s’agit du flux SkipBlock rencontrée.</span><span class="sxs-lookup"><span data-stu-id="9e620-155">This is the terminating SkipBlock stream.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9e620-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9e620-156">See also</span></span>

- [<span data-ttu-id="9e620-157">Les champs et les éléments outlook</span><span class="sxs-lookup"><span data-stu-id="9e620-157">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="9e620-158">Structures de flux de données</span><span class="sxs-lookup"><span data-stu-id="9e620-158">Stream Structures</span></span>](stream-structures.md)
- [<span data-ttu-id="9e620-159">La définition PropertyDefinition flux Structure</span><span class="sxs-lookup"><span data-stu-id="9e620-159">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="9e620-160">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="9e620-160">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="9e620-161">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="9e620-161">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="9e620-162">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="9e620-162">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="9e620-163">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="9e620-163">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="9e620-164">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="9e620-164">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

