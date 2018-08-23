---
title: Exemple de flux de données FolderUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30e5e887-a324-4ed2-ba2a-eb4c19ba38d2
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 76ad693b05e3989bd64ba66565ae4def22110ad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564898"
---
# <a name="folderuserfields-stream-sample"></a><span data-ttu-id="99ea1-103">Exemple de flux de données FolderUserFields</span><span class="sxs-lookup"><span data-stu-id="99ea1-103">FolderUserFields stream sample</span></span>

<span data-ttu-id="99ea1-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99ea1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99ea1-105">Cette rubrique décrit un exemple d’un flux FolderUserFields.</span><span class="sxs-lookup"><span data-stu-id="99ea1-105">This topic describes an example of a FolderUserFields stream.</span></span> <span data-ttu-id="99ea1-106">Le flux contient une définition d’un champ défini par l’utilisateur, `TextField1`.</span><span class="sxs-lookup"><span data-stu-id="99ea1-106">The stream contains a definition of a user-defined field,  `TextField1`.</span></span> <span data-ttu-id="99ea1-107">Le type est **texte**, et le flux FolderUserFields contient des composants WebPart à la fois FolderUserFieldsAnsi et FolderUserFieldsUnicode.</span><span class="sxs-lookup"><span data-stu-id="99ea1-107">The type is **Text**, and the FolderUserFields stream contains both FolderUserFieldsAnsi and FolderUserFieldsUnicode parts.</span></span> <span data-ttu-id="99ea1-108">Pour plus d’informations, voir [Dossier champs Stream Structures](folder-fields-stream-structures.md).</span><span class="sxs-lookup"><span data-stu-id="99ea1-108">For more information see [Folder Fields Stream Structures](folder-fields-stream-structures.md).</span></span>
  
## <a name="data-dump"></a><span data-ttu-id="99ea1-109">Vidage des données</span><span class="sxs-lookup"><span data-stu-id="99ea1-109">Data dump</span></span>

<span data-ttu-id="99ea1-110">Vous trouverez ci-dessous un vidage des données de l’objet stream tel qu’il doit être affiché dans un éditeur binaire.</span><span class="sxs-lookup"><span data-stu-id="99ea1-110">The following is a data dump of the stream as it would be displayed in a binary editor.</span></span>
  
|<span data-ttu-id="99ea1-111">Décalage de flux</span><span class="sxs-lookup"><span data-stu-id="99ea1-111">Stream offset</span></span>|<span data-ttu-id="99ea1-112">Octets de données</span><span class="sxs-lookup"><span data-stu-id="99ea1-112">Data bytes</span></span>|<span data-ttu-id="99ea1-113">Données ASCII</span><span class="sxs-lookup"><span data-stu-id="99ea1-113">ASCII data</span></span>|
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
   

<span data-ttu-id="99ea1-114">Vous trouverez ci-dessous une analyse des données pour le flux **FolderUserFields** :</span><span class="sxs-lookup"><span data-stu-id="99ea1-114">The following is a parse of the sample data for the **FolderUserFields** stream:</span></span>
  
- <span data-ttu-id="99ea1-115">FolderUserFieldsAnsi : Décalage 0 x 0.</span><span class="sxs-lookup"><span data-stu-id="99ea1-115">FolderUserFieldsAnsi: Offset 0x0.</span></span>
    
  - <span data-ttu-id="99ea1-116">FieldDefinitionCount : Décalage de 0 x 0, 4 octets : 0 x 00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="99ea1-116">FieldDefinitionCount: Offset 0x0, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="99ea1-117">FieldDefinitions : Décalage 0 x 4, tableau des flux de FolderFieldDefinitionA 2.</span><span class="sxs-lookup"><span data-stu-id="99ea1-117">FieldDefinitions: Offset 0x4, array of 2 FolderFieldDefinitionA streams.</span></span>
    
    <span data-ttu-id="99ea1-118">**Premier élément du tableau**:</span><span class="sxs-lookup"><span data-stu-id="99ea1-118">**First array element**:</span></span>
    
    - <span data-ttu-id="99ea1-119">FieldType : Décalage de 0 x 4, 4 octets : 0 x 00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="99ea1-119">FieldType: Offset 0x4, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="99ea1-120">FieldNameLength : Décalage 0 x 8, 2 octets : 0x000A (10)</span><span class="sxs-lookup"><span data-stu-id="99ea1-120">FieldNameLength: Offset 0x8, 2 bytes: 0x000A (10)</span></span>
      
    - <span data-ttu-id="99ea1-121">FieldName : Décalage 0xA, tableau de 10 caractères.</span><span class="sxs-lookup"><span data-stu-id="99ea1-121">FieldName: Offset 0xA, array of 10 CHARs.</span></span> <span data-ttu-id="99ea1-122">Valeur de chaîne ANSI : « TextField1 ».</span><span class="sxs-lookup"><span data-stu-id="99ea1-122">ANSI string value: "TextField1".</span></span>
      
    - <span data-ttu-id="99ea1-123">Courants : Décalage 0 x 14.</span><span class="sxs-lookup"><span data-stu-id="99ea1-123">Common: Offset 0x14.</span></span>
    
      - <span data-ttu-id="99ea1-124">PropSetGuid : Décalage 0 x 14, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="99ea1-124">PropSetGuid: Offset 0x14, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="99ea1-125">fcapm : décalage de 0 x 24, 4 octets : 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="99ea1-125">fcapm: Offset 0x24, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="99ea1-126">dwString : 0 x 28, 4 octets de décalage : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-126">dwString: Offset 0x28, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-127">dwBitmap : décalage 0x2C, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-127">dwBitmap: Offset 0x2C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-128">dwDisplay : 0 x 30, 4 octets de décalage : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-128">dwDisplay: Offset 0x30, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-129">iFmt : 0 x 34, 4 octets de décalage : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-129">iFmt: Offset 0x34, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-130">wszFormulaLength : 0 x 38, 2 octets de décalage : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-130">wszFormulaLength: Offset 0x38, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-131">wszFormula : décalage 0x3A, le tableau de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-131">wszFormula: Offset 0x3A, array of 0 WCHARs.</span></span> <span data-ttu-id="99ea1-132">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-132">Empty string value.</span></span>
    
    <span data-ttu-id="99ea1-133">**Deuxième élément du tableau**:</span><span class="sxs-lookup"><span data-stu-id="99ea1-133">**Second array element**:</span></span>
    
    - <span data-ttu-id="99ea1-134">FieldType : Décalage 0x3A, 4 octets : 0 x 00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="99ea1-134">FieldType: Offset 0x3A, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="99ea1-135">FieldNameLength : Décalage 0x3E, 2 octets : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-135">FieldNameLength: Offset 0x3E, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="99ea1-136">FieldName : Décalage 0 x 40, du tableau de caractères de 0.</span><span class="sxs-lookup"><span data-stu-id="99ea1-136">FieldName: Offset 0x40, array of 0 CHARs.</span></span> <span data-ttu-id="99ea1-137">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-137">Empty string value.</span></span>
      
    - <span data-ttu-id="99ea1-138">Courantes : 0 x 40 décalage.</span><span class="sxs-lookup"><span data-stu-id="99ea1-138">Common: Offset 0x40.</span></span>
    
      - <span data-ttu-id="99ea1-139">PropSetGuid : Décalage 0 x 40, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="99ea1-139">PropSetGuid: Offset 0x40, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="99ea1-140">fcapm : 0 x 50, 4 octets de décalage : 0 x 00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-140">fcapm: Offset 0x50, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-141">dwString : 0 x 54, 4 octets de décalage : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-141">dwString: Offset 0x54, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-142">dwBitmap : décalage 0x58, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-142">dwBitmap: Offset 0x58, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-143">dwDisplay : décalage 0x5C, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-143">dwDisplay: Offset 0x5C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-144">iFmt : 0 x 60, 4 octets de décalage : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-144">iFmt: Offset 0x60, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-145">wszFormulaLength : 0 x 64, 2 octets de décalage : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-145">wszFormulaLength: Offset 0x64, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-146">wszFormula : décalage 0x66, le tableau de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-146">wszFormula: Offset 0x66, array of 0 WCHARs.</span></span> <span data-ttu-id="99ea1-147">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-147">Empty string value.</span></span>
    
- <span data-ttu-id="99ea1-148">FolderUserFieldsUnicode : Décalage 0x66.</span><span class="sxs-lookup"><span data-stu-id="99ea1-148">FolderUserFieldsUnicode: Offset 0x66.</span></span>
    
  - <span data-ttu-id="99ea1-149">FieldDefinitionCount : Décalage 0x66, 4 octets : 0 x 00000002 (2).</span><span class="sxs-lookup"><span data-stu-id="99ea1-149">FieldDefinitionCount: Offset 0x66, 4 bytes: 0x00000002 (2).</span></span>
    
  - <span data-ttu-id="99ea1-150">FieldDefinitions : Décalage 0x6A, tableau des flux de FolderFieldDefinitionW 2.</span><span class="sxs-lookup"><span data-stu-id="99ea1-150">FieldDefinitions: Offset 0x6A, array of 2 FolderFieldDefinitionW streams.</span></span>
    
    <span data-ttu-id="99ea1-151">**Premier élément du tableau**:</span><span class="sxs-lookup"><span data-stu-id="99ea1-151">**First array element**:</span></span>
    
    - <span data-ttu-id="99ea1-152">FieldType : Décalage 0x6A, 4 octets : 0 x 00000001 (ftString).</span><span class="sxs-lookup"><span data-stu-id="99ea1-152">FieldType: Offset 0x6A, 4 bytes: 0x00000001 (ftString).</span></span>
      
    - <span data-ttu-id="99ea1-153">FieldNameLength : Décalage 0x6E, 2 octets : 0x000A (10).</span><span class="sxs-lookup"><span data-stu-id="99ea1-153">FieldNameLength: Offset 0x6E, 2 bytes: 0x000A (10).</span></span>
      
    - <span data-ttu-id="99ea1-154">FieldName : Décalage 0 x 70, tableau de 10 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-154">FieldName: Offset 0x70, array of 10 WCHARs.</span></span> <span data-ttu-id="99ea1-155">Valeur de chaîne Unicode : « TextField1 ».</span><span class="sxs-lookup"><span data-stu-id="99ea1-155">Unicode string value: "TextField1".</span></span>
      
    - <span data-ttu-id="99ea1-156">Courantes : 0 x 84 décalage.</span><span class="sxs-lookup"><span data-stu-id="99ea1-156">Common: Offset 0x84.</span></span>
    
      - <span data-ttu-id="99ea1-157">PropSetGuid : Décalage de 0 x 84, 16 octets : {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span><span class="sxs-lookup"><span data-stu-id="99ea1-157">PropSetGuid: Offset 0x84, 16 bytes: {00020329-0000-0000-C000-000000000046} (PS_PUBLIC_STRINGS).</span></span>
        
      - <span data-ttu-id="99ea1-158">fcapm : décalage 0x94, 4 octets : 0x80000007 (FCAPM_CAN_EDIT | FCAPM_CAN_SORT | FCAPM_CAN_GROUP | FCAPM_CAN_EDIT_IN_ITEM).</span><span class="sxs-lookup"><span data-stu-id="99ea1-158">fcapm: Offset 0x94, 4 bytes: 0x80000007 (FCAPM_CAN_EDIT| FCAPM_CAN_SORT| FCAPM_CAN_GROUP|FCAPM_CAN_EDIT_IN_ITEM).</span></span>
        
      - <span data-ttu-id="99ea1-159">dwString : décalage 0x98, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-159">dwString: Offset 0x98, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-160">dwBitmap : décalage 0x9C, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-160">dwBitmap: Offset 0x9C, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-161">dwDisplay : décalage 0xA0, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-161">dwDisplay: Offset 0xA0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-162">iFmt : décalage 0xA4, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-162">iFmt: Offset 0xA4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-163">wszFormulaLength : décalage 0xA8, 2 octets : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-163">wszFormulaLength: Offset 0xA8, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-164">wszFormula : décalage 0xAA, le tableau de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-164">wszFormula: Offset 0xAA, array of 0 WCHARs.</span></span> <span data-ttu-id="99ea1-165">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-165">Empty string value.</span></span>
    
    <span data-ttu-id="99ea1-166">**Deuxième élément du tableau**:</span><span class="sxs-lookup"><span data-stu-id="99ea1-166">**Second array element**:</span></span>
    
    - <span data-ttu-id="99ea1-167">FieldType : Décalage 0xAA, 4 octets : 0 x 00000000 (ftNone).</span><span class="sxs-lookup"><span data-stu-id="99ea1-167">FieldType: Offset 0xAA, 4 bytes: 0x00000000 (ftNone).</span></span>
      
    - <span data-ttu-id="99ea1-168">FieldNameLength : Décalage 0xAE, 2 octets : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-168">FieldNameLength: Offset 0xAE, 2 bytes: 0x0000 (0).</span></span>
      
    - <span data-ttu-id="99ea1-169">FieldName : Décalage 0xB0, tableau de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-169">FieldName: Offset 0xB0, array of 0 WCHARs.</span></span> <span data-ttu-id="99ea1-170">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-170">Empty string value.</span></span>
      
    - <span data-ttu-id="99ea1-171">Courantes : Décalage 0xB0.</span><span class="sxs-lookup"><span data-stu-id="99ea1-171">Common: Offset 0xB0.</span></span>
    
      - <span data-ttu-id="99ea1-172">PropSetGuid : Décalage 0xB0, 16 octets : {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span><span class="sxs-lookup"><span data-stu-id="99ea1-172">PropSetGuid: Offset 0xB0, 16 bytes: {00000000-0000-0000-0000-000000000000} (GUID_NULL).</span></span>
        
      - <span data-ttu-id="99ea1-173">fcapm : décalage 0xC0, 4 octets : 0 x 00000000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-173">fcapm: Offset 0xC0, 4 bytes: 0x00000000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-174">dwString : décalage 0xC4, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-174">dwString: Offset 0xC4, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-175">dwBitmap : décalage 0xC8, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-175">dwBitmap: Offset 0xC8, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-176">dwDisplay : décalage 0xCC, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-176">dwDisplay: Offset 0xCC, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-177">iFmt : décalage 0xD0, 4 octets : 0 x 00000000.</span><span class="sxs-lookup"><span data-stu-id="99ea1-177">iFmt: Offset 0xD0, 4 bytes: 0x00000000.</span></span>
        
      - <span data-ttu-id="99ea1-178">wszFormulaLength : décalage 0xD4, 2 octets : 0 x 0000 (0).</span><span class="sxs-lookup"><span data-stu-id="99ea1-178">wszFormulaLength: Offset 0xD4, 2 bytes: 0x0000 (0).</span></span>
        
      - <span data-ttu-id="99ea1-179">wszFormula : décalage 0xD6, le tableau de 0 WCHAR.</span><span class="sxs-lookup"><span data-stu-id="99ea1-179">wszFormula: Offset 0xD6, array of 0 WCHARs.</span></span> <span data-ttu-id="99ea1-180">Valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="99ea1-180">Empty string value.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99ea1-181">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99ea1-181">See also</span></span>

- [<span data-ttu-id="99ea1-182">Champs et éléments Outlook</span><span class="sxs-lookup"><span data-stu-id="99ea1-182">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
- [<span data-ttu-id="99ea1-183">Structure de flux PropertyDefinition</span><span class="sxs-lookup"><span data-stu-id="99ea1-183">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
- [<span data-ttu-id="99ea1-184">Structure de flux FieldDefinition</span><span class="sxs-lookup"><span data-stu-id="99ea1-184">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
- [<span data-ttu-id="99ea1-185">Structure de flux SkipBlock</span><span class="sxs-lookup"><span data-stu-id="99ea1-185">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
- [<span data-ttu-id="99ea1-186">Structure de flux FirstSkipBlockContent</span><span class="sxs-lookup"><span data-stu-id="99ea1-186">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
- [<span data-ttu-id="99ea1-187">Structure de flux PackedAnsiString</span><span class="sxs-lookup"><span data-stu-id="99ea1-187">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
- [<span data-ttu-id="99ea1-188">Structure de flux PackedUnicodeString</span><span class="sxs-lookup"><span data-stu-id="99ea1-188">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)

