---
title: Est égale à (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compare l’égalité de deux expressions.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781839"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="7c0ec-103">Est égale à (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="7c0ec-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="7c0ec-104">Compare l’égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7c0ec-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7c0ec-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c0ec-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="7c0ec-108">*expression*  =  *expression*</span><span class="sxs-lookup"><span data-stu-id="7c0ec-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="7c0ec-109">*expression*  Peut être toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="7c0ec-110">Si les expressions ne sont pas du même type de données, le type de données pour une expression doit être implicitement convertible au type de données de l’autre.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="7c0ec-111">La conversion dépend des règles de priorité des types de données.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="7c0ec-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="7c0ec-112">Return Type</span></span>

<span data-ttu-id="7c0ec-113">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="7c0ec-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7c0ec-114">Notes</span><span class="sxs-lookup"><span data-stu-id="7c0ec-114">Remarks</span></span>

<span data-ttu-id="7c0ec-115">Lorsque vous comparez deux expressions NULL, le résultat est TRUE.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="7c0ec-116">Comparaison toujours NULL pour une valeur non NULL donne FALSE.</span><span class="sxs-lookup"><span data-stu-id="7c0ec-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

