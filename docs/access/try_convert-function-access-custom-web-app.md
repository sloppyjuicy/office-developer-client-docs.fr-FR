---
title: Fonction Try_Convert (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convertit une valeur en un type de données spécifiée ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: ce942c1f444da7bfcbff76077a5a9d75dd611336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782018"
---
# <a name="tryconvert-function-access-custom-web-app"></a><span data-ttu-id="f12dc-103">Fonction Try_Convert (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="f12dc-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="f12dc-104">Convertit une valeur en un type de données spécifiée ou renvoie la valeur Null si la conversion n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f12dc-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f12dc-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f12dc-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f12dc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f12dc-107">Syntax</span></span>

 <span data-ttu-id="f12dc-108">**Try_Convert** (*Type de données*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="f12dc-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="f12dc-109">La fonction **Try_Convert** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="f12dc-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="f12dc-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="f12dc-110">**Argument name**</span></span>|<span data-ttu-id="f12dc-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f12dc-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f12dc-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="f12dc-112">*DataType*</span></span>  <br/> |<span data-ttu-id="f12dc-113">Le type de données dans lequel convertir *l’Expression* .</span><span class="sxs-lookup"><span data-stu-id="f12dc-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="f12dc-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="f12dc-114">*Expression*</span></span>  <br/> |<span data-ttu-id="f12dc-115">La valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="f12dc-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f12dc-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f12dc-116">Remarks</span></span>

 <span data-ttu-id="f12dc-117">**Try_Convert** prend la valeur qui lui sont transmise et tente de convertir le *type de données* de spécifié.</span><span class="sxs-lookup"><span data-stu-id="f12dc-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="f12dc-118">Si la conversion réussit, **Try_Convert** renvoie la valeur en tant que le *type de données* d' spécifié ; Si une erreur se produit, la valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="f12dc-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="f12dc-119">Toutefois si vous avez demandé une conversion qui n’est pas explicitement autorisée, **Try_Convert** échoue avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="f12dc-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

