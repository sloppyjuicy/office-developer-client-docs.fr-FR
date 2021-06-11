---
title: DECIMALSEP, fonction
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251883
localization_priority: Normal
ms.assetid: 091fe401-05b2-464f-9333-7bb7118cd7cd
description: Renvoie la chaîne de séparateur décimal pour les paramètres régionaux de l’utilisateur actuel.
ms.openlocfilehash: 8a59e7331fd51cf5426b5e2cdd64e3c5a22334b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360304"
---
# <a name="decimalsep-function"></a><span data-ttu-id="c6e84-103">Fonction DECIMALSEP</span><span class="sxs-lookup"><span data-stu-id="c6e84-103">DECIMALSEP Function</span></span>

<span data-ttu-id="c6e84-104">Renvoie la chaîne de séparateur décimal pour les paramètres régionaux de l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="c6e84-104">Returns the decimal separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c6e84-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6e84-105">Syntax</span></span>

<span data-ttu-id="c6e84-106">DECIMALSEP( )</span><span class="sxs-lookup"><span data-stu-id="c6e84-106">DECIMALSEP( )</span></span>
  
## <a name="example"></a><span data-ttu-id="c6e84-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="c6e84-107">Example</span></span>

<span data-ttu-id="c6e84-108">SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span><span class="sxs-lookup"><span data-stu-id="c6e84-108">SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span></span> 
  

