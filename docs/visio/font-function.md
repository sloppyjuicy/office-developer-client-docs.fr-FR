---
title: Fonction FONT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 20b587ee-87bf-4648-99ec-ddedd703d9fd
description: Renvoie la valeur de type integer de l’identificateur unique d’une police, spécifié par son nom.
ms.openlocfilehash: 7ae6fe6dc8bb9c718a358d11d4a6a0227eaf18df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422172"
---
# <a name="font-function"></a><span data-ttu-id="d7071-103">Fonction FONT</span><span class="sxs-lookup"><span data-stu-id="d7071-103">FONT Function</span></span>

<span data-ttu-id="d7071-104">Renvoie la valeur de type integer de l’identificateur unique d’une police, spécifié par son nom.</span><span class="sxs-lookup"><span data-stu-id="d7071-104">Returns the integer value of the unique identifier for a font, specified by name.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d7071-105">Dans la plupart des cas, l’identificateur de police est propre au système.</span><span class="sxs-lookup"><span data-stu-id="d7071-105">In most cases, the font identifier is system-specific.</span></span> <span data-ttu-id="d7071-106">Bien que la police reste établie une fois utilisée dans un fichier, la **fonction FONT** fournit un accès cohérent à une police particulière entre les systèmes et les versions de Visio.</span><span class="sxs-lookup"><span data-stu-id="d7071-106">Although the font remains established once used in a file, the **FONT** function provides consistent access to a particular font across systems and versions of Visio.</span></span> <span data-ttu-id="d7071-107">Il est recommandé d’utiliser la **fonction FONT** pour affecter des polices au lieu de faire référence directement aux identificateurs de police.</span><span class="sxs-lookup"><span data-stu-id="d7071-107">It is recommended that you use the **FONT** function to assign fonts instead of referring to font identifiers directly.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="d7071-108">Informations de version</span><span class="sxs-lookup"><span data-stu-id="d7071-108">Version Information</span></span>

<span data-ttu-id="d7071-109">Version ajoutée : Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="d7071-109">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d7071-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7071-110">Syntax</span></span>

 <span data-ttu-id="d7071-111">**FONT**( _« font_name_string »_)</span><span class="sxs-lookup"><span data-stu-id="d7071-111">**FONT**( _"font_name_string"_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="d7071-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7071-112">Parameters</span></span>

|<span data-ttu-id="d7071-113">**Nom**</span><span class="sxs-lookup"><span data-stu-id="d7071-113">**Name**</span></span>|<span data-ttu-id="d7071-114">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d7071-114">**Required/Optional**</span></span>|<span data-ttu-id="d7071-115">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d7071-115">**Data Type**</span></span>|<span data-ttu-id="d7071-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7071-116">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d7071-117">_font_name_string_</span><span class="sxs-lookup"><span data-stu-id="d7071-117">_font_name_string_</span></span> <br/> |<span data-ttu-id="d7071-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d7071-118">Required</span></span>  <br/> |<span data-ttu-id="d7071-119">**chaîne**</span><span class="sxs-lookup"><span data-stu-id="d7071-119">**string**</span></span> <br/> |<span data-ttu-id="d7071-120">Nom de la police.</span><span class="sxs-lookup"><span data-stu-id="d7071-120">The name of the font.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="d7071-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d7071-121">Return value</span></span>

<span data-ttu-id="d7071-122">Entier</span><span class="sxs-lookup"><span data-stu-id="d7071-122">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7071-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7071-123">Remarks</span></span>

<span data-ttu-id="d7071-124">Si la chaîne fournie pour  *font_name_string*  ne correspond pas à une police connue, cette fonction renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="d7071-124">If the string provided for  *font_name_string*  does not match a known font, this function returns a #VALUE!</span></span> <span data-ttu-id="d7071-125">erreur.</span><span class="sxs-lookup"><span data-stu-id="d7071-125">error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d7071-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="d7071-126">Example</span></span>

 `FONT("Calibri")`
  
<span data-ttu-id="d7071-127">Renvoie la valeur de type integer (4) qui représente l’ID unique de la police « Calibri ».</span><span class="sxs-lookup"><span data-stu-id="d7071-127">Returns the integer value (4) representing the unique ID for the "Calibri" font.</span></span>
  

