---
title: Méthode Database.Close (DAO)
TOCTitle: Close Method
ms:assetid: b777ee92-172a-3342-31fc-76e7361c47fd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822418(v=office.15)
ms:contentKeyID: 48547296
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c97786db2e909074f1a1e0d81e4af03d34301602
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25920682"
---
# <a name="databaseclose-method-dao"></a><span data-ttu-id="2282b-102">Méthode Database.Close (DAO)</span><span class="sxs-lookup"><span data-stu-id="2282b-102">Database.Close method (DAO)</span></span>


<span data-ttu-id="2282b-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2282b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2282b-104">Ferme un objet **Database** ouvert.</span><span class="sxs-lookup"><span data-stu-id="2282b-104">Closes an open **Database**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2282b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2282b-105">Syntax</span></span>

<span data-ttu-id="2282b-106">*expression* . Fermer</span><span class="sxs-lookup"><span data-stu-id="2282b-106">*expression* .Close</span></span>

<span data-ttu-id="2282b-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="2282b-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2282b-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2282b-108">Remarks</span></span>

<span data-ttu-id="2282b-109">Si l'objet **Database** est déjà fermé lorsque vous utilisez **Close**, une erreur d'exécution se produit.</span><span class="sxs-lookup"><span data-stu-id="2282b-109">If the **Database** object is already closed when you use **Close**, a run-time error occurs.</span></span>

<span data-ttu-id="2282b-110">Une alternative à la méthode **Close** est la valeur d’une variable d’objet sur **Nothing** (Set dbsTemp = Nothing).</span><span class="sxs-lookup"><span data-stu-id="2282b-110">An alternative to the **Close** method is to set the value of an object variable to **Nothing** (Set dbsTemp = Nothing).</span></span>

