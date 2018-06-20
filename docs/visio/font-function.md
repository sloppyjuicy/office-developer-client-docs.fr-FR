---
title: Fonction de la police
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Renvoie la valeur d’entier de l’identificateur unique pour une police, spécifiée par nom.
ms.openlocfilehash: 4afd2aa05f2103675bf0df8db5cc7ea21f45fe71
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788673"
---
# <a name="font-function"></a><span data-ttu-id="f6b0e-103">Fonction de la police</span><span class="sxs-lookup"><span data-stu-id="f6b0e-103">FONT Function</span></span>

<span data-ttu-id="f6b0e-104">Renvoie la valeur d’entier de l’identificateur unique pour une police, spécifiée par nom.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f6b0e-105">Dans la plupart des cas, l’identificateur de la police est spécifiques au système.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="f6b0e-106">Bien que la police reste établie autrefois utilisé dans un fichier, la fonction de **police** offre un accès cohérent à une police spécifique sur les systèmes et les versions de Visio.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="f6b0e-107">Il est recommandé d’utiliser la fonction de la **police** pour affecter des polices au lieu de faire référence aux identificateurs de police directement.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="f6b0e-108">Informations de version</span><span class="sxs-lookup"><span data-stu-id="f6b0e-108">Version Information</span></span>

<span data-ttu-id="f6b0e-109">Version ajoutée : Visio 2013</span><span class="sxs-lookup"><span data-stu-id="f6b0e-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f6b0e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6b0e-110">Syntax</span></span>

 <span data-ttu-id="f6b0e-111">**Police** ( _« font_name_string »_)</span><span class="sxs-lookup"><span data-stu-id="f6b0e-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="f6b0e-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6b0e-112">Parameters</span></span>

|<span data-ttu-id="f6b0e-113">**Name**</span><span class="sxs-lookup"><span data-stu-id="f6b0e-113">**Name**</span></span>|<span data-ttu-id="f6b0e-114">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f6b0e-114">**Required/Optional**</span></span>|<span data-ttu-id="f6b0e-115">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f6b0e-115">**Data Type**</span></span>|<span data-ttu-id="f6b0e-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="f6b0e-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f6b0e-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="f6b0e-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="f6b0e-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f6b0e-118">Required</span></span>  <br/> |<span data-ttu-id="f6b0e-119">**string**</span><span class="sxs-lookup"><span data-stu-id="f6b0e-119">**string**</span></span> <br/> |<span data-ttu-id="f6b0e-120">Nom de la police.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="f6b0e-121">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="f6b0e-121">Return value</span></span>

<span data-ttu-id="f6b0e-122">Entier</span><span class="sxs-lookup"><span data-stu-id="f6b0e-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6b0e-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="f6b0e-123">Remarks</span></span>

<span data-ttu-id="f6b0e-124">Si la chaîne fournie pour *font_name_string* ne correspond pas à une police connue, cette fonction renvoie une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="f6b0e-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="f6b0e-125">erreur.</span><span class="sxs-lookup"><span data-stu-id="f6b0e-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f6b0e-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="f6b0e-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="f6b0e-127">Renvoie la valeur d’entier (4) qui représente l’identificateur unique pour la police « Calibri ».</span><span class="sxs-lookup"><span data-stu-id="f6b0e-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

