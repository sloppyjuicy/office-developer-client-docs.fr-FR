---
title: Try_Convert Function (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea514f19-4742-4eb4-823d-6f2494668106
description: Convertit une valeur en un type de données spécifié ou renvoie la valeur Null si la conversion n’est pas valide.
ms.openlocfilehash: 473d9063da46652afa88dc974cb4c4036e1c326c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410895"
---
# <a name="try_convert-function-access-custom-web-app"></a><span data-ttu-id="c19fe-103">Try_Convert Function (Application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="c19fe-103">Try_Convert Function (Access custom web app)</span></span>

<span data-ttu-id="c19fe-104">Convertit une valeur en un type de données spécifié ou renvoie la valeur Null si la conversion n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c19fe-104">Converts a value to a specified data type or returns Null if the conversion is not valid.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c19fe-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c19fe-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c19fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c19fe-107">Syntax</span></span>

 <span data-ttu-id="c19fe-108">**Try_Convert** (*DataType*, *Expression*)</span><span class="sxs-lookup"><span data-stu-id="c19fe-108">**Try_Convert** (*DataType*, *Expression*)</span></span> 
  
<span data-ttu-id="c19fe-109">La **Try_Convert** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="c19fe-109">The **Try_Convert** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c19fe-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="c19fe-110">**Argument name**</span></span>|<span data-ttu-id="c19fe-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c19fe-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c19fe-112">*DataType*</span><span class="sxs-lookup"><span data-stu-id="c19fe-112">*DataType*</span></span>  <br/> |<span data-ttu-id="c19fe-113">Type de données dans lequel convertir  *Expression*  .</span><span class="sxs-lookup"><span data-stu-id="c19fe-113">The data type into which to convert  *Expression*  .</span></span>  <br/> |
| <span data-ttu-id="c19fe-114">*Expression*</span><span class="sxs-lookup"><span data-stu-id="c19fe-114">*Expression*</span></span>  <br/> |<span data-ttu-id="c19fe-115">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="c19fe-115">The value to be converted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c19fe-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c19fe-116">Remarks</span></span>

 <span data-ttu-id="c19fe-117">**Try_Convert** prend la valeur qui lui est passée et tente de la convertir en *DataType spécifié.*</span><span class="sxs-lookup"><span data-stu-id="c19fe-117">**Try_Convert** takes the value passed to it and tries to convert it to the specified  *DataType*  .</span></span> <span data-ttu-id="c19fe-118">Si la conversion réussit, **Try_Convert** renvoie la valeur en tant que  *DataType spécifié ;*  si une erreur se produit, la valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c19fe-118">If the conversion succeeds, **Try_Convert** returns the value as the specified  *DataType*  ; if an error occurs, null is returned.</span></span> <span data-ttu-id="c19fe-119">Toutefois, si vous demandez une conversion qui n’est explicitement pas autorisée, **Try_Convert** échoue avec une erreur.</span><span class="sxs-lookup"><span data-stu-id="c19fe-119">However if you request a conversion that is explicitly not permitted, then **Try_Convert** fails with an error.</span></span> 
  

