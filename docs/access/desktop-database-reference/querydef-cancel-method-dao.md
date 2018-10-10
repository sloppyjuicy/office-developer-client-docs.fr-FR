---
title: QueryDef.Cancel Method (DAO)
TOCTitle: Cancel Method
ms:assetid: 91e61012-c01c-4c24-185c-bdadb7f33a58
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197642(v=office.15)
ms:contentKeyID: 48546364
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055470
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 17e6c98851aa20a6a094223eeabb68fe40e719d5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469850"
---
# <a name="querydefcancel-method-dao"></a><span data-ttu-id="c1537-102">QueryDef.Cancel Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="c1537-102">QueryDef.Cancel Method (DAO)</span></span>


<span data-ttu-id="c1537-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1537-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="c1537-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1537-104">Syntax</span></span>

<span data-ttu-id="c1537-105">*expression* . Annuler</span><span class="sxs-lookup"><span data-stu-id="c1537-105">*expression* .Cancel</span></span>

<span data-ttu-id="c1537-106">*expression* Variable qui représente un objet **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="c1537-106">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1537-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1537-107">Remarks</span></span>

<span data-ttu-id="c1537-108">Utilisez la méthode **Cancel** pour mettre fin à l’exécution d’un appel de méthode **Execute** ou **OpenConnection** asynchrone (autrement dit, la méthode a été appelée avec l’option dbRunAsync).</span><span class="sxs-lookup"><span data-stu-id="c1537-108">Use the **Cancel** method to terminate execution of an asynchronous **Execute** or **OpenConnection** method call (that is, the method was invoked with the dbRunAsync option).</span></span> <span data-ttu-id="c1537-109">**Annuler** renvoie une erreur d’exécution si dbRunAsync n’a pas été utilisé dans la méthode que vous essayez d’interrompre.</span><span class="sxs-lookup"><span data-stu-id="c1537-109">**Cancel** will return a run-time error if dbRunAsync was not used in the method you're trying to terminate.</span></span>

