---
title: MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (RDS)
TOCTitle: MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)
ms:assetid: 32ef8fa9-c096-b4e7-3396-b88a6a9bd1a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249101(v=office.15)
ms:contentKeyID: 48544092
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 02c6bc5ab4cc8357d7f349eb1698c2e6a026e173
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602852"
---
# <a name="movefirst-movelast-movenext-and-moveprevious-methods-rds"></a><span data-ttu-id="d9c70-102">MoveFirst, MoveLast, MoveNext et MovePrevious, méthodes (RDS)</span><span class="sxs-lookup"><span data-stu-id="d9c70-102">MoveFirst, MoveLast, MoveNext, and MovePrevious Methods (RDS)</span></span>


<span data-ttu-id="d9c70-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d9c70-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d9c70-104">Accède au premier ou dernier enregistrement, à l'enregistrement suivant ou précédent d'un objet [Recordset](recordset-object-ado.md) spécifié.</span><span class="sxs-lookup"><span data-stu-id="d9c70-104">Moves to the first, last, next, or previous record in a specified [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c70-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9c70-105">Syntax</span></span>

<span data-ttu-id="d9c70-106">*DataControl*. Jeu d’enregistrements. {</span><span class="sxs-lookup"><span data-stu-id="d9c70-106">*DataControl*.Recordset.{</span></span> <span data-ttu-id="d9c70-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span><span class="sxs-lookup"><span data-stu-id="d9c70-107">MoveFirst | MoveLast | MoveNext | MovePrevious}</span></span>

## <a name="parameters"></a><span data-ttu-id="d9c70-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d9c70-108">Parameters</span></span>

  - <span data-ttu-id="d9c70-109">*DataControl*</span><span class="sxs-lookup"><span data-stu-id="d9c70-109">*DataControl*</span></span>

  - <span data-ttu-id="d9c70-110">Une variable objet qui représente un objet [RDS.DataControl](datacontrol-object-rds.md).</span><span class="sxs-lookup"><span data-stu-id="d9c70-110">An object variable that represents an [RDS.DataControl](datacontrol-object-rds.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9c70-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d9c70-111">Remarks</span></span>

<span data-ttu-id="d9c70-112"><<<<<<< HEAD vous pouvez utiliser les méthodes **Move** avec le **RDS. DataControl** objet pour parcourir les enregistrements de données dans les contrôles liés aux données sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="d9c70-112"><<<<<<< HEAD You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a Web page.</span></span> <span data-ttu-id="d9c70-113">Supposons, par exemple, que vous affichez un objet **Recordset** dans une grille en le liant à un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="d9c70-113">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="d9c70-114">Vous pouvez ensuite inclure des boutons Premier, Dernier, Suivant et Précédent sur lesquels les utilisateurs peuvent cliquer pour accéder au premier ou dernier enregistrement, ou encore à l'enregistrement suivant ou précédent de l'objet **Recordset** affiché.</span><span class="sxs-lookup"><span data-stu-id="d9c70-114">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="d9c70-115">Pour ce faire, appelez les méthodes **MoveFirst**, **MoveLast**, **MoveNext** et **MovePrevious** de l'objet **RDS.DataControl** dans les procédures onClick, respectivement pour les boutons Premier, Dernier, Suivant et Précédent.</span><span class="sxs-lookup"><span data-stu-id="d9c70-115">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="d9c70-116">L' [exemple du Carnet d'adresses](address-book-navigation-buttons.md) illustre cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d9c70-116">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
<span data-ttu-id="d9c70-117">=== Vous pouvez utiliser les méthodes **Move** avec le **RDS. DataControl** objet pour parcourir les enregistrements de données dans les contrôles liés aux données sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="d9c70-117">======= You can use the **Move** methods with the **RDS.DataControl** object to navigate through the data records in the data-bound controls on a webpage.</span></span> <span data-ttu-id="d9c70-118">Supposons, par exemple, que vous affichez un objet **Recordset** dans une grille en le liant à un objet **RDS.DataControl**.</span><span class="sxs-lookup"><span data-stu-id="d9c70-118">For example, suppose you display a **Recordset** in a grid by binding to an **RDS.DataControl** object.</span></span> <span data-ttu-id="d9c70-119">Vous pouvez ensuite inclure des boutons Premier, Dernier, Suivant et Précédent sur lesquels les utilisateurs peuvent cliquer pour accéder au premier ou dernier enregistrement, ou encore à l'enregistrement suivant ou précédent de l'objet **Recordset** affiché.</span><span class="sxs-lookup"><span data-stu-id="d9c70-119">You can then include First, Last, Next, and Previous buttons that users can click to move to the first, last, next, or previous record in the displayed **Recordset**.</span></span> <span data-ttu-id="d9c70-120">Pour ce faire, appelez les méthodes **MoveFirst**, **MoveLast**, **MoveNext** et **MovePrevious** de l'objet **RDS.DataControl** dans les procédures onClick, respectivement pour les boutons Premier, Dernier, Suivant et Précédent.</span><span class="sxs-lookup"><span data-stu-id="d9c70-120">You do this by calling the **MoveFirst**, **MoveLast**, **MoveNext**, and **MovePrevious** methods of the **RDS.DataControl** object in the onClick procedures for the First, Last, Next, and Previous buttons, respectively.</span></span> <span data-ttu-id="d9c70-121">L' [exemple du Carnet d'adresses](address-book-navigation-buttons.md) illustre cette procédure.</span><span class="sxs-lookup"><span data-stu-id="d9c70-121">The [Address Book example](address-book-navigation-buttons.md) shows how to do this.</span></span>
>>>>>>> <span data-ttu-id="d9c70-122">master</span><span class="sxs-lookup"><span data-stu-id="d9c70-122">master</span></span>

