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
description: Renvoie la chaîne de séparateur décimal pour les paramètres régionaux utilisateur.
ms.openlocfilehash: a47bc20702262ab7d4a072694c36e424e6949919
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788442"
---
# <a name="decimalsep-function"></a><span data-ttu-id="d2955-103">DECIMALSEP, fonction</span><span class="sxs-lookup"><span data-stu-id="d2955-103">DECIMALSEP Function</span></span>

<span data-ttu-id="d2955-104">Renvoie la chaîne de séparateur décimal pour les paramètres régionaux utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d2955-104">Returns the decimal separator string for the current user locale.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d2955-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d2955-105">Syntax</span></span>

<span data-ttu-id="d2955-106">DECIMALSEP( )</span><span class="sxs-lookup"><span data-stu-id="d2955-106">DECIMALSEP( )</span></span>
  
## <a name="example"></a><span data-ttu-id="d2955-107">Exemple</span><span class="sxs-lookup"><span data-stu-id="d2955-107">Example</span></span>

<span data-ttu-id="d2955-108">SETF(GETREF(User.Size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span><span class="sxs-lookup"><span data-stu-id="d2955-108">SETF(GETREF(user.size), user.wholePart &amp; DECIMALSEP() &amp; user.fracPart)</span></span> 
  

