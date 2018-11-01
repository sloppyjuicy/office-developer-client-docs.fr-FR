---
title: Database.Close Method (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 92b4075f09bb34eca465f49d30a9ba8777b3e583
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869651"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="c6ef8-102">Database.Close Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c6ef8-102">Database.Close Method (DAO)</span></span>


<span data-ttu-id="c6ef8-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c6ef8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c6ef8-104">Ferme un objet **Database** ouvert.</span><span class="sxs-lookup"><span data-stu-id="c6ef8-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6ef8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c6ef8-105">Syntax</span></span>

<span data-ttu-id="c6ef8-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="c6ef8-106">*expression* .Close</span></span>

<span data-ttu-id="c6ef8-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="c6ef8-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6ef8-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="c6ef8-108">Remarks</span></span>

<span data-ttu-id="c6ef8-109">Si l'objet **Database** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="c6ef8-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="c6ef8-110">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="c6ef8-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

