---
title: CreateParameter, méthode (ADO)
TOCTitle: CreateParameter Method (ADO)
ms:assetid: cf080a0b-75d2-dcdf-2715-10af147358e9
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250026(v=office.15)
ms:contentKeyID: 48547799
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231042
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 00a2c5e2eb8613434b80c80e2a51cbf5d1deb644
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605484"
---
# <a name="createparameter-method-ado"></a><span data-ttu-id="12b74-102">CreateParameter, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="12b74-102">CreateParameter Method (ADO)</span></span>


<span data-ttu-id="12b74-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="12b74-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="12b74-104">Crée un objet [Parameter](parameter-object-ado.md) avec les propriétés spécifiées.</span><span class="sxs-lookup"><span data-stu-id="12b74-104">Creates a new [Parameter](parameter-object-ado.md) object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="12b74-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="12b74-105">Syntax</span></span>

<span data-ttu-id="12b74-106">**La valeur** *paramètre*  =  *commande*. CreateParameter (*nom*, *Type*, *orientation*, *taille*, *valeur*)</span><span class="sxs-lookup"><span data-stu-id="12b74-106">**Set** *parameter* = *command*.CreateParameter (*Name*, *Type*, *Direction*, *Size*, *Value*)</span></span>

<span data-ttu-id="12b74-107"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="12b74-107"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="12b74-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12b74-108">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="12b74-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="12b74-109">Return value</span></span>
>>>>>>> <span data-ttu-id="12b74-110">master</span><span class="sxs-lookup"><span data-stu-id="12b74-110">master</span></span>

<span data-ttu-id="12b74-111">Retourne un objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="12b74-111">Returns a **Parameter** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="12b74-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="12b74-112">Parameters</span></span>

  - <span data-ttu-id="12b74-113">*Name*</span><span class="sxs-lookup"><span data-stu-id="12b74-113">*Name*</span></span>

  - <span data-ttu-id="12b74-p101">Facultatif. Valeur de type **String** contenant le nom de l'objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="12b74-p101">Optional. A **String** value that contains the name of the **Parameter** object.</span></span>

  - <span data-ttu-id="12b74-116">*Type*</span><span class="sxs-lookup"><span data-stu-id="12b74-116">*Type*</span></span>

  - <span data-ttu-id="12b74-p102">Facultatif. Valeur [DataTypeEnum](datatypeenum.md) qui spécifie le type de données de l'objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="12b74-p102">Optional. A [DataTypeEnum](datatypeenum.md) value that specifies the data type of the **Parameter** object.</span></span>

  - <span data-ttu-id="12b74-119">*Direction*</span><span class="sxs-lookup"><span data-stu-id="12b74-119">*Direction*</span></span>

  - <span data-ttu-id="12b74-p103">Facultatif. Valeur [ParameterDirectionEnum](parameterdirectionenum.md) qui spécifie le type de l'objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="12b74-p103">Optional. A [ParameterDirectionEnum](parameterdirectionenum.md) value that specifies the type of **Parameter** object.</span></span>

  - <span data-ttu-id="12b74-122">*Size*</span><span class="sxs-lookup"><span data-stu-id="12b74-122">*Size*</span></span>

  - <span data-ttu-id="12b74-p104">Facultatif. Valeur de type **Long** qui spécifie la longueur maximale de la valeur du paramètre en caractères ou en octets.</span><span class="sxs-lookup"><span data-stu-id="12b74-p104">Optional. A **Long** value that specifies the maximum length for the parameter value in characters or bytes.</span></span>

  - <span data-ttu-id="12b74-125">*Value*</span><span class="sxs-lookup"><span data-stu-id="12b74-125">*Value*</span></span>

  - <span data-ttu-id="12b74-p105">Facultatif. **Variant** qui spécifie la valeur de l'objet **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="12b74-p105">Optional. A **Variant** that specifies the value for the **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="12b74-128">Notes</span><span class="sxs-lookup"><span data-stu-id="12b74-128">Remarks</span></span>

<span data-ttu-id="12b74-p106">Utilisez la méthode **CreateParameter** pour créer un objet **Parameter** avec un nom, un type, une direction, une taille et une valeur spécifiques. Toutes les valeurs passées dans les arguments sont écrites dans les propriétés **Parameter** correspondantes.</span><span class="sxs-lookup"><span data-stu-id="12b74-p106">Use the **CreateParameter** method to create a new **Parameter** object with a specified name, type, direction, size, and value. Any values you pass in the arguments are written to the corresponding **Parameter** properties.</span></span>

<span data-ttu-id="12b74-p107">Cette méthode n'ajoute pas automatiquement l'objet **Parameter** à la collection **Parameters** d'un objet [Command](command-object-ado.md). Ceci vous permet de définir des propriétés supplémentaires dont ADO validera les valeurs lorsque vous ajouterez l'objet **Parameter** à la collection.</span><span class="sxs-lookup"><span data-stu-id="12b74-p107">This method does not automatically append the **Parameter** object to the **Parameters** collection of a [Command](command-object-ado.md) object. This lets you set additional properties whose values ADO will validate when you append the **Parameter** object to the collection.</span></span>

<span data-ttu-id="12b74-133">Si vous spécifiez un type de données de longueur variable dans l’argument *Type* , vous devez passer un argument *Size* ou définir la propriété [Size](size-property-ado.md) de l’objet **Parameter** avant de l’ajouter à la collection **Parameters** . dans le cas contraire, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="12b74-133">If you specify a variable-length data type in the *Type* argument, you must either pass a *Size* argument or set the [Size](size-property-ado.md) property of the **Parameter** object before appending it to the **Parameters** collection; otherwise, an error occurs.</span></span>

<span data-ttu-id="12b74-134">Si vous spécifiez un type de données numérique (**adNumeric** ou **adDecimal**) dans l’argument *Type*, vous devez également définir les propriétés [NumericScale](numericscale-property-ado.md) et [Precision](precision-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="12b74-134">If you specify a numeric data type (**adNumeric** or **adDecimal**) in the *Type* argument, then you must also set the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties.</span></span>

