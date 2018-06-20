---
title: Fonction de la langue
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Permet les opérations de comparaison entre les représentations de langue différente. Il convient de conversion des valeurs de balises (BCP 47) langue Internet Engineering Task Force en identifiants de paramètres régionaux (LCID).
ms.openlocfilehash: 6a05a850f5908ac5a4f6a4a72b2ce56b4c98f137
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788921"
---
# <a name="language-function"></a><span data-ttu-id="75707-104">Fonction de la langue</span><span class="sxs-lookup"><span data-stu-id="75707-104">LANGUAGE Function</span></span>

<span data-ttu-id="75707-105">Permet les opérations de comparaison entre les représentations de langue différente.</span><span class="sxs-lookup"><span data-stu-id="75707-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="75707-106">Il convient de conversion des valeurs de balises (BCP 47) langue Internet Engineering Task Force en identifiants de paramètres régionaux (LCID).</span><span class="sxs-lookup"><span data-stu-id="75707-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="75707-107">Informations de version</span><span class="sxs-lookup"><span data-stu-id="75707-107">Version Information</span></span>

<span data-ttu-id="75707-108">Version ajoutée : Visio 2013</span><span class="sxs-lookup"><span data-stu-id="75707-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="75707-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75707-109">Syntax</span></span>

 <span data-ttu-id="75707-110">**Langue** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="75707-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="75707-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75707-111">Parameters</span></span>

|<span data-ttu-id="75707-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="75707-112">**Name**</span></span>|<span data-ttu-id="75707-113">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="75707-113">**Required/Optional**</span></span>|<span data-ttu-id="75707-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="75707-114">**Data Type**</span></span>|<span data-ttu-id="75707-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="75707-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="75707-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="75707-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="75707-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="75707-117">Required</span></span>  <br/> |<span data-ttu-id="75707-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="75707-118">**String**</span></span> <br/> |<span data-ttu-id="75707-119">La valeur LCID ou norme BCP 47 pour la langue.</span><span class="sxs-lookup"><span data-stu-id="75707-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="75707-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="75707-120">Return value</span></span>

<span data-ttu-id="75707-121">Entier</span><span class="sxs-lookup"><span data-stu-id="75707-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="75707-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="75707-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="75707-123">Renvoie la valeur « 1033 ».</span><span class="sxs-lookup"><span data-stu-id="75707-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="75707-124">Renvoie la valeur « 3082 ».</span><span class="sxs-lookup"><span data-stu-id="75707-124">Returns a value of '3082'.</span></span>
  

