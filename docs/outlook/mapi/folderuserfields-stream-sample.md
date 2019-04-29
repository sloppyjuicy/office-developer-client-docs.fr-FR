---
title: Exemple de flux FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e5251a619c70221987847830897ba349d63fd9cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433975"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="cffeb-103">Exemple de flux FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="cffeb-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="cffeb-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cffeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cffeb-105">Cette rubrique décrit un exemple de flux FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="cffeb-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="cffeb-106">Le flux contient une définition d'un champ défini par l'utilisateur `TextField1`,.</span><span class="sxs-lookup"><span data-stu-id="cffeb-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="cffeb-107">Le type est **Text**et le flux FolderUserFields contient à la fois des composants FolderUserFieldsAnsi et FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="cffeb-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="cffeb-108">Pour plus d'informations, consultez la rubrique [champs de dossier structures de flux](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="cffeb-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="cffeb-109">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="cffeb-109">Data dump</span></span>

<span data-ttu-id="cffeb-110">Voici un dump des données du flux tel qu'il s'afficherait dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="cffeb-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="cffeb-111">Décalage de flux</span><span class="sxs-lookup"><span data-stu-id="cffeb-111">Stream offset</span></span>|<span data-ttu-id="cffeb-112">Octets de données</span><span class="sxs-lookup"><span data-stu-id="cffeb-112">Data bytes</span></span>|<span data-ttu-id="cffeb-113">Données ASCII</span><span class="sxs-lookup"><span data-stu-id="cffeb-113">ASCII data</span></span>|
|:-----|:-----|:-----|
| `0000000000` <br/> | `02 00 00 00 01 00 00 00 0A 00 54 65 78 74 46 69` <br/> | `..........TextFi` <br/> |
| `0000000010` <br/> | `65 6C 64 31 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `eld1).......A...` <br/> |
| `0000000020` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `0000000030` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000040` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000050` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `0000000060` <br/> | `00 00 00 00 00 00 02 00 00 00 01 00 00 00 0A 00` <br/> | `................` <br/> |
| `0000000070` <br/> | `54 00 65 00 78 00 74 00 46 00 69 00 65 00 6C 00` <br/> | `T.e.x.t.F.i.e.l.` <br/> |
| `0000000080` <br/> | `64 00 31 00 29 03 02 00 00 00 00 00 C0 00 00 00` <br/> | `d.1.).......A...` <br/> |
| `0000000090` <br/> | `00 00 00 46 07 00 00 80 00 00 00 00 00 00 00 00` <br/> | `...F............` <br/> |
| `00000000A0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000B0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000C0` <br/> | `00 00 00 00 00 00 00 00 00 00 00 00 00 00 00 00` <br/> | `................` <br/> |
| `00000000D0` <br/> | `00 00 00 00 00 00` <br/> | `......` <br/> |
   

<span data-ttu-id="cffeb-114">Voici une analyse des exemples de données pour le flux **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="cffeb-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="cffeb-115">FolderUserFieldsAnsi: offset 0x0.</span><span class="sxs-lookup"><span data-stu-id="cffeb-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="cffeb-116">FieldDefinitionCount: offset 0x0, 4 octets: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="cffeb-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="cffeb-117">FieldDefinitions: offset 0x4, tableau de 2 flux de FolderFieldDefinitionA.</span><span class="sxs-lookup"><span data-stu-id="cffeb-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="cffeb-118">**Premier élément de tableau**:</span><span class="sxs-lookup"><span data-stu-id="cffeb-118">**First array element**:</span></span>
    
    - <span data-ttu-id="cffeb-119">FieldType: offset 0x4, 4 octets: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="cffeb-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="cffeb-120">FieldNameLength: décalage 0x8, 2 octets: 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="cffeb-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="cffeb-121">FieldName: offset 0xA, tableau de 10 caractères.</span><span class="sxs-lookup"><span data-stu-id="cffeb-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="cffeb-122">Valeur de chaîne ANSI: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="cffeb-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="cffeb-123">Common: offset 0x14.</span><span class="sxs-lookup"><span data-stu-id="cffeb-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="cffeb-124">PropSetGuid: offset 0x14, 16 octets: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="cffeb-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="cffeb-125">fcapm: offset 0x24, 4 octets: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="cffeb-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="cffeb-126">dwString: décalage 0x28, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-127">dwBitmap: décalage 0x2C, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-128">dwDisplay: décalage 0x30, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-129">iFmt: décalage 0x34, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-130">wszFormulaLength: décalage 0x38, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-131">wszFormula: décalage 0x3A, tableau de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="cffeb-132">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-132">Empty string value.</span></span>
    
    <span data-ttu-id="cffeb-133">**Deuxième élément de tableau**:</span><span class="sxs-lookup"><span data-stu-id="cffeb-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="cffeb-134">FieldType: décalage 0x3A, 4 octets: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="cffeb-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="cffeb-135">FieldNameLength: décalage 0x3E, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="cffeb-136">FieldName: offset 0x40, tableau de 0 CHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="cffeb-137">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-137">Empty string value.</span></span>
      
    - <span data-ttu-id="cffeb-138">Commun: décalage 0x40.</span><span class="sxs-lookup"><span data-stu-id="cffeb-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="cffeb-139">PropSetGuid: offset 0x40, 16 octets: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="cffeb-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="cffeb-140">fcapm: décalage 0x50, 4 octets: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-141">dwString: décalage 0x54, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-142">dwBitmap: décalage 0x58, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-143">dwDisplay: décalage 0x5C, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-144">iFmt: décalage 0x60, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-145">wszFormulaLength: décalage 0x64, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-146">wszFormula: décalage 0x66, tableau de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="cffeb-147">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-147">Empty string value.</span></span>
    
- <span data-ttu-id="cffeb-148">FolderUserFieldsUnicode: décalage 0x66.</span><span class="sxs-lookup"><span data-stu-id="cffeb-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="cffeb-149">FieldDefinitionCount: décalage 0x66, 4 octets: 0x00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="cffeb-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="cffeb-150">FieldDefinitions: décalage 0x6A, tableau de 2 flux de FolderFieldDefinitionW.</span><span class="sxs-lookup"><span data-stu-id="cffeb-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="cffeb-151">**Premier élément de tableau**:</span><span class="sxs-lookup"><span data-stu-id="cffeb-151">**First array element**:</span></span>
    
    - <span data-ttu-id="cffeb-152">FieldType: décalage 0x6A, 4 octets: 0x00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="cffeb-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="cffeb-153">FieldNameLength: décalage 0x6E, 2 octets: 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="cffeb-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="cffeb-154">Nom_champ: décalage 0x70, tableau de 10 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="cffeb-155">Valeur de chaîne Unicode: «TextField1».</span><span class="sxs-lookup"><span data-stu-id="cffeb-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="cffeb-156">Common: offset 0x84.</span><span class="sxs-lookup"><span data-stu-id="cffeb-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="cffeb-157">PropSetGuid: décalage 0x84, 16 octets: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="cffeb-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="cffeb-158">fcapm: décalage 0x94, 4 octets: 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="cffeb-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="cffeb-159">dwString: décalage 0x98, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-160">dwBitmap: décalage 0x9C, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-161">dwDisplay: décalage 0xA0, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-162">iFmt: décalage 0xA4, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-163">wszFormulaLength: décalage 0xA8, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-164">wszFormula: décalage 0xAA, tableau de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="cffeb-165">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-165">Empty string value.</span></span>
    
    <span data-ttu-id="cffeb-166">**Deuxième élément de tableau**:</span><span class="sxs-lookup"><span data-stu-id="cffeb-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="cffeb-167">FieldType: décalage 0xAA, 4 octets: 0x00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="cffeb-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="cffeb-168">FieldNameLength: décalage 0xAE, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="cffeb-169">FieldName: offset 0xB0, tableau de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="cffeb-170">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-170">Empty string value.</span></span>
      
    - <span data-ttu-id="cffeb-171">Common: offset 0xB0.</span><span class="sxs-lookup"><span data-stu-id="cffeb-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="cffeb-172">PropSetGuid: décalage 0xB0, 16 octets: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="cffeb-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="cffeb-173">fcapm: décalage 0xC0, 4 octets: 0x00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-174">dwString: décalage 0xC4, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-175">dwBitmap: décalage 0xC8, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-176">dwDisplay: décalage 0xCC, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-177">iFmt: décalage 0xD0, 4 octets: 0x00000000.</span><span class="sxs-lookup"><span data-stu-id="cffeb-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="cffeb-178">wszFormulaLength: décalage 0xD4, 2 octets: 0x0000 (0).</span><span class="sxs-lookup"><span data-stu-id="cffeb-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="cffeb-179">wszFormula: décalage 0xD6, tableau de 0 WCHARs.</span><span class="sxs-lookup"><span data-stu-id="cffeb-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="cffeb-180">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="cffeb-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cffeb-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cffeb-181">See also</span></span>

- [<span data-ttu-id="cffeb-182">Éléments et champs Outlook</span><span class="sxs-lookup"><span data-stu-id="cffeb-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="cffeb-183">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="cffeb-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="cffeb-184">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="cffeb-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="cffeb-185">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="cffeb-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="cffeb-186">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="cffeb-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="cffeb-187">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="cffeb-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="cffeb-188">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="cffeb-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

