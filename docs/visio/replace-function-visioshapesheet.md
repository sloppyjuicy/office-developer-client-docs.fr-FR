---
title: REPLACE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 75a156d720ca276e75fccf932124ae905e4350b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320159"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="0363d-103">REPLACE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0363d-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0363d-104">Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.</span><span class="sxs-lookup"><span data-stu-id="0363d-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="0363d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0363d-105">Syntax</span></span>

<span data-ttu-id="0363d-106">RePLACE (\* \* *ancien_texte* \* \*, \* \* *no_départ* \* \*, \* \* *no_car* \* \*, \* \* *nouveau_texte* \* \*)</span><span class="sxs-lookup"><span data-stu-id="0363d-106">REPLACE (\*\* *old_text* \*\*, \*\* *start_num* \*\*, \*\* *num_chars* \*\*, \*\* *new_text* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0363d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0363d-107">Parameters</span></span>

|<span data-ttu-id="0363d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="0363d-108">**Name**</span></span>|<span data-ttu-id="0363d-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0363d-109">**Required/Optional**</span></span>|<span data-ttu-id="0363d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0363d-110">**Data Type**</span></span>|<span data-ttu-id="0363d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="0363d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0363d-112">_ancien_texte_</span><span class="sxs-lookup"><span data-stu-id="0363d-112">_old_text_</span></span> <br/> |<span data-ttu-id="0363d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0363d-113">Required</span></span>  <br/> |<span data-ttu-id="0363d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="0363d-114">**String**</span></span> <br/> |<span data-ttu-id="0363d-115">Texte dans lequel vous souhaitez remplacer certains caractères.</span><span class="sxs-lookup"><span data-stu-id="0363d-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="0363d-116">_no_départ_</span><span class="sxs-lookup"><span data-stu-id="0363d-116">_start_num_</span></span> <br/> |<span data-ttu-id="0363d-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0363d-117">Required</span></span>  <br/> |<span data-ttu-id="0363d-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="0363d-118">**Number**</span></span> <br/> |<span data-ttu-id="0363d-119">Position du caractère d' _ancien_texte_ à remplacer par _nouveau_texte_.</span><span class="sxs-lookup"><span data-stu-id="0363d-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="0363d-120">Le premier caractère de la chaîne est à la position 1.</span><span class="sxs-lookup"><span data-stu-id="0363d-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="0363d-121">_no_car_</span><span class="sxs-lookup"><span data-stu-id="0363d-121">_num_chars_</span></span> <br/> |<span data-ttu-id="0363d-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0363d-122">Required</span></span>  <br/> |<span data-ttu-id="0363d-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="0363d-123">**Number**</span></span> <br/> |<span data-ttu-id="0363d-124">Nombre de caractères d' _ancien_texte_ à remplacer</span><span class="sxs-lookup"><span data-stu-id="0363d-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="0363d-125">_nouveau_texte_</span><span class="sxs-lookup"><span data-stu-id="0363d-125">_new_text_</span></span> <br/> |<span data-ttu-id="0363d-126">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0363d-126">Required</span></span>  <br/> |<span data-ttu-id="0363d-127">**String**</span><span class="sxs-lookup"><span data-stu-id="0363d-127">**String**</span></span> <br/> |<span data-ttu-id="0363d-128">Texte qui remplace les caractères d' _ancien_texte_.</span><span class="sxs-lookup"><span data-stu-id="0363d-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0363d-129">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0363d-129">Return value</span></span>

<span data-ttu-id="0363d-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="0363d-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0363d-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="0363d-131">Remarks</span></span>

<span data-ttu-id="0363d-p102">Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="0363d-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="0363d-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="0363d-134">Example</span></span>

<span data-ttu-id="0363d-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="0363d-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="0363d-136">Renvoie le 01.03.03.</span><span class="sxs-lookup"><span data-stu-id="0363d-136">Returns 01/03/2003.</span></span> 
  

