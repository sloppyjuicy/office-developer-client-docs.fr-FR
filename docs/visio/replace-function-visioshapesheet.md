---
title: REPLACE, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60108
localization_priority: Normal
ms.assetid: 70c9fc1d-6e7b-479f-effd-0d4bc8ae0f72
description: Remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.
ms.openlocfilehash: 4112339d772248ac033674808d97c3f9c55b6f0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789438"
---
# <a name="replace-function-visioshapesheet"></a><span data-ttu-id="3a554-103">REPLACE, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3a554-103">REPLACE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3a554-104">Cette méthode remplace une partie de chaîne de texte, selon le nombre de caractères que vous spécifiez, par une chaîne de texte différente.</span><span class="sxs-lookup"><span data-stu-id="3a554-104">Replaces part of a text string, based on the number of characters you specify, with a different text string.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3a554-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3a554-105">Syntax</span></span>

<span data-ttu-id="3a554-106">Remplacer (** *old_text* **, ** *start_num* **, ** *nb_cars* **, ** *new_text* **)</span><span class="sxs-lookup"><span data-stu-id="3a554-106">REPLACE (** *old_text* **, ** *start_num* **, ** *num_chars* **, ** *new_text* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3a554-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3a554-107">Parameters</span></span>

|<span data-ttu-id="3a554-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3a554-108">**Name**</span></span>|<span data-ttu-id="3a554-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3a554-109">**Required/Optional**</span></span>|<span data-ttu-id="3a554-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3a554-110">**Data Type**</span></span>|<span data-ttu-id="3a554-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3a554-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3a554-112">_old_text_</span><span class="sxs-lookup"><span data-stu-id="3a554-112">_old_text_</span></span> <br/> |<span data-ttu-id="3a554-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3a554-113">Required</span></span>  <br/> |<span data-ttu-id="3a554-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a554-114">**String**</span></span> <br/> |<span data-ttu-id="3a554-115">Texte dans lequel vous souhaitez remplacer certains caractères.</span><span class="sxs-lookup"><span data-stu-id="3a554-115">The text in which you want to replace some characters.</span></span>  <br/> |
| <span data-ttu-id="3a554-116">_Start_num_</span><span class="sxs-lookup"><span data-stu-id="3a554-116">_start_num_</span></span> <br/> |<span data-ttu-id="3a554-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3a554-117">Required</span></span>  <br/> |<span data-ttu-id="3a554-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="3a554-118">**Number**</span></span> <br/> |<span data-ttu-id="3a554-119">Position du caractère dans _old_text_ que vous souhaitez remplacer par _new_text_.</span><span class="sxs-lookup"><span data-stu-id="3a554-119">The position of the character in  _old_text_ that you want to replace with  _new_text_.</span></span> <span data-ttu-id="3a554-120">Le premier caractère de la chaîne est la position 1.</span><span class="sxs-lookup"><span data-stu-id="3a554-120">The first character in the string is position 1.</span></span>  <br/> |
| <span data-ttu-id="3a554-121">_nb_cars_</span><span class="sxs-lookup"><span data-stu-id="3a554-121">_num_chars_</span></span> <br/> |<span data-ttu-id="3a554-122">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3a554-122">Required</span></span>  <br/> |<span data-ttu-id="3a554-123">**Number**</span><span class="sxs-lookup"><span data-stu-id="3a554-123">**Number**</span></span> <br/> |<span data-ttu-id="3a554-124">Le nombre de caractères dans _old_text_ que vous souhaitez remplacer</span><span class="sxs-lookup"><span data-stu-id="3a554-124">The number of characters in  _old_text_ that you want to replace</span></span>  <br/> |
| <span data-ttu-id="3a554-125">_new_text_</span><span class="sxs-lookup"><span data-stu-id="3a554-125">_new_text_</span></span> <br/> |<span data-ttu-id="3a554-126">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3a554-126">Required</span></span>  <br/> |<span data-ttu-id="3a554-127">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="3a554-127">**String**</span></span> <br/> |<span data-ttu-id="3a554-128">Le texte qui remplace des caractères dans _old_text_.</span><span class="sxs-lookup"><span data-stu-id="3a554-128">The text that will replace characters in  _old_text_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3a554-129">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3a554-129">Return value</span></span>

<span data-ttu-id="3a554-130">Chaîne</span><span class="sxs-lookup"><span data-stu-id="3a554-130">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3a554-131">Remarques</span><span class="sxs-lookup"><span data-stu-id="3a554-131">Remarks</span></span>

<span data-ttu-id="3a554-p102">Utilisez la fonction REPLACE lorsque vous souhaitez remplacer du texte qui apparaît à un endroit spécifique dans une chaîne de texte. Pour remplacer un texte spécifique dans une chaîne de texte, utilisez la fonction SUBSTITUTE.</span><span class="sxs-lookup"><span data-stu-id="3a554-p102">Use the REPLACE function when you want to replace text that occurs in a specific location in a text string. If you want to replace specific text in a text string, use the SUBSTITUTE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="3a554-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="3a554-134">Example</span></span>

<span data-ttu-id="3a554-135">REPLACE ("01/03/2002",9,2,"03")</span><span class="sxs-lookup"><span data-stu-id="3a554-135">REPLACE ("01/03/2002",9,2,"03")</span></span> 
  
<span data-ttu-id="3a554-136">Renvoie le 01.03.03.</span><span class="sxs-lookup"><span data-stu-id="3a554-136">Returns 01/03/2003.</span></span> 
  

