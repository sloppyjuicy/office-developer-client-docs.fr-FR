---
title: LANGUAGE Function
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e372c670-e9a0-4352-b70a-3a054b036124
description: Autorise les opérations de comparaison entre différentes représentations de langue. Il est préférable de convertir les valeurs de balises de langue IETF (Internet Engineering Task Force) en valeurs d'ID de paramètres régionaux (LCID).
ms.openlocfilehash: 9c2dc96cefe7a1cfcd06947dcc54453dcef276fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327817"
---
# <a name="language-function"></a><span data-ttu-id="02549-104">LANGUAGE Function</span><span class="sxs-lookup"><span data-stu-id="02549-104">LANGUAGE Function</span></span>

<span data-ttu-id="02549-105">Autorise les opérations de comparaison entre différentes représentations de langue.</span><span class="sxs-lookup"><span data-stu-id="02549-105">Allows comparison operations between different language representations.</span></span> <span data-ttu-id="02549-106">Il est préférable de convertir les valeurs de balises de langue IETF (Internet Engineering Task Force) en valeurs d'ID de paramètres régionaux (LCID).</span><span class="sxs-lookup"><span data-stu-id="02549-106">It is best used for converting Internet Engineering Task Force language tags (BCP 47) values to locale id (LCID) values.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="02549-107">Informations de version</span><span class="sxs-lookup"><span data-stu-id="02549-107">Version Information</span></span>

<span data-ttu-id="02549-108">Version ajoutée : Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="02549-108">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="02549-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02549-109">Syntax</span></span>

 <span data-ttu-id="02549-110">**Langue** ( _lcid_or_bcp47_)</span><span class="sxs-lookup"><span data-stu-id="02549-110">**LANGUAGE**( _lcid_or_bcp47_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="02549-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02549-111">Parameters</span></span>

|<span data-ttu-id="02549-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="02549-112">**Name**</span></span>|<span data-ttu-id="02549-113">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="02549-113">**Required/Optional**</span></span>|<span data-ttu-id="02549-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02549-114">**Data Type**</span></span>|<span data-ttu-id="02549-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="02549-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="02549-116">_lcid_or_bcp47_</span><span class="sxs-lookup"><span data-stu-id="02549-116">_lcid_or_bcp47_</span></span> <br/> |<span data-ttu-id="02549-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="02549-117">Required</span></span>  <br/> |<span data-ttu-id="02549-118">**String**</span><span class="sxs-lookup"><span data-stu-id="02549-118">**String**</span></span> <br/> |<span data-ttu-id="02549-119">Valeur LCID ou BCP 47 de la langue.</span><span class="sxs-lookup"><span data-stu-id="02549-119">The LCID or BCP 47 value for the language.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="02549-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02549-120">Return value</span></span>

<span data-ttu-id="02549-121">Entier</span><span class="sxs-lookup"><span data-stu-id="02549-121">Integer</span></span>
  
## <a name="example"></a><span data-ttu-id="02549-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="02549-122">Example</span></span>

 `LANGUAGE("en-us")`
  
<span data-ttu-id="02549-123">Renvoie la valeur «1033».</span><span class="sxs-lookup"><span data-stu-id="02549-123">Returns a value of '1033'.</span></span>
  
 `LANGUAGE("es-es")`
  
<span data-ttu-id="02549-124">Renvoie la valeur «3082».</span><span class="sxs-lookup"><span data-stu-id="02549-124">Returns a value of '3082'.</span></span>
  

