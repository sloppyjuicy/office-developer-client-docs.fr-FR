---
title: DOCMD, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60100
localization_priority: Normal
ms.assetid: 6574edeb-eb6f-afd9-89c4-eb5996dffa30
description: Exécute la commande identifiée.
ms.openlocfilehash: 9e5c02c9a90f3aab66c5d582c83d7d9d892f964c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315231"
---
# <a name="docmd-function"></a><span data-ttu-id="83021-103">Fonction DOCMD</span><span class="sxs-lookup"><span data-stu-id="83021-103">DOCMD Function</span></span>

<span data-ttu-id="83021-104">Exécute la commande identifiée.</span><span class="sxs-lookup"><span data-stu-id="83021-104">Performs the identified command.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="83021-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83021-105">Syntax</span></span>

 <span data-ttu-id="83021-106">**DoCmd** ( _CommandID_)</span><span class="sxs-lookup"><span data-stu-id="83021-106">**DOCMD**( _commandID_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="83021-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83021-107">Parameters</span></span>

|<span data-ttu-id="83021-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="83021-108">**Name**</span></span>|<span data-ttu-id="83021-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="83021-109">**Required/Optional**</span></span>|<span data-ttu-id="83021-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="83021-110">**Data Type**</span></span>|<span data-ttu-id="83021-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="83021-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="83021-112">_CommandID_</span><span class="sxs-lookup"><span data-stu-id="83021-112">_commandID_</span></span> <br/> |<span data-ttu-id="83021-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="83021-113">Required</span></span>  <br/> |<span data-ttu-id="83021-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="83021-114">**Number**</span></span> <br/> | <span data-ttu-id="83021-115">Commande à exécuter</span><span class="sxs-lookup"><span data-stu-id="83021-115">The command to perform.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83021-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="83021-116">Remarks</span></span>

<span data-ttu-id="83021-117">Pour obtenir la liste des commandes prises en charge par la fonction DOCMD, voir la rubrique relative aux commandes DoCmd/DOCMD dans la référence d'Automation de Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="83021-117">For a list of commands that are supported with the DOCMD function, see the topic "DoCmd/DOCMD commands" in the Microsoft Visio 2013 Automation Reference.</span></span> 
  
## <a name="example"></a><span data-ttu-id="83021-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="83021-118">Example</span></span>

 `DOCMD (1312)`
  
<span data-ttu-id="83021-119">Entraîne l’affichage de la boîte de dialogue **Données de forme** dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83021-119">Causes the **Shape Data** dialog box to appear in the user interface.</span></span> 
  

