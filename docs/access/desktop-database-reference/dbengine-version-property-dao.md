---
title: DBEngine.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: b2807dc1-604f-4423-289a-ff38a3d9f31b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822024(v=office.15)
ms:contentKeyID: 48547171
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052986
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 865942cdf4cca81cb0d5348725164a4a75a845fb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870911"
---
# <a name="dbengineversion-property-dao"></a><span data-ttu-id="b154c-102">DBEngine.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="b154c-102">DBEngine.Version Property (DAO)</span></span>


<span data-ttu-id="b154c-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b154c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b154c-p101">Renvoie la version de DAO en cours d'utilisation. Valeur de type **String** en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b154c-p101">Rreturns the version of DAO currently in use. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b154c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b154c-106">Syntax</span></span>

<span data-ttu-id="b154c-107">*expression* . Version</span><span class="sxs-lookup"><span data-stu-id="b154c-107">*expression* .Version</span></span>

<span data-ttu-id="b154c-108">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="b154c-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b154c-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="b154c-109">Remarks</span></span>

<span data-ttu-id="b154c-p102">La valeur renvoyée est une chaîne (type String) correspondant à un numéro de version au format « principale.secondaire ». Par exemple, « 3.0 ». Le numéro de version du produit comprend le numéro de version principale (3), un point, puis le numéro de version secondaire (0).</span><span class="sxs-lookup"><span data-stu-id="b154c-p102">The return value is a String that evaluates to a version number in the form "major.minor". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

