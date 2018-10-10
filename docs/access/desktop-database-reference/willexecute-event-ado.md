---
title: WillExecute, événement (ADO)
TOCTitle: WillExecute Event (ADO)
ms:assetid: 9f516bfd-246d-9817-4ca3-64598ab466f7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249732(v=office.15)
ms:contentKeyID: 48546686
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8a5c739ffd408a1f53539c88a3bdc4169eb4cebe
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469420"
---
# <a name="willexecute-event-ado"></a><span data-ttu-id="32d24-102">WillExecute, événement (ADO)</span><span class="sxs-lookup"><span data-stu-id="32d24-102">WillExecute Event (ADO)</span></span>


<span data-ttu-id="32d24-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="32d24-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="32d24-104">L'événement **WillExecute** est appelé juste avant l'exécution d'une commande en attente sur une connexion.</span><span class="sxs-lookup"><span data-stu-id="32d24-104">The **WillExecute** event is called just before a pending command executes on a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32d24-105">Syntax</span></span>

<span data-ttu-id="32d24-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *Connection*, *pConnection*</span><span class="sxs-lookup"><span data-stu-id="32d24-106">WillExecute*Source*, *CursorType*, *LockType*, *Options*, *adStatus*, *pCommand*, *pRecordset*, *pConnection*</span></span>

## <a name="parameters"></a><span data-ttu-id="32d24-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="32d24-107">Parameters</span></span>

  - <span data-ttu-id="32d24-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="32d24-108">*Source*</span></span>

  - <span data-ttu-id="32d24-109">Valeur de type **String** reprenant le nom d'une commande SQL ou d'une procédure stockée.</span><span class="sxs-lookup"><span data-stu-id="32d24-109">A **String** that contains an SQL command or a stored procedure name.</span></span>

  - <span data-ttu-id="32d24-110">*CursorType*</span><span class="sxs-lookup"><span data-stu-id="32d24-110">*CursorType*</span></span>

  - <span data-ttu-id="32d24-111">Valeur [CursorTypeEnum](cursortypeenum.md) contenant le type de curseur pour l'objet **Recordset** qui sera ouvert.</span><span class="sxs-lookup"><span data-stu-id="32d24-111">A [CursorTypeEnum](cursortypeenum.md) that contains the type of cursor for the **Recordset** that will be opened.</span></span> <span data-ttu-id="32d24-112">Avec ce paramètre, vous pouvez modifier le curseur à n’importe quel type pendant une opération [d’ouverture](open-method-ado-recordset.md) de **jeu d’enregistrements** .</span><span class="sxs-lookup"><span data-stu-id="32d24-112">With this parameter, you can change the cursor to any type during a **Recordset** [Open](open-method-ado-recordset.md) operation.</span></span> <span data-ttu-id="32d24-113">*CursorType* est ignorée pour tout autre opération.</span><span class="sxs-lookup"><span data-stu-id="32d24-113">*CursorType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="32d24-114">*LockType*</span><span class="sxs-lookup"><span data-stu-id="32d24-114">*LockType*</span></span>

  - <span data-ttu-id="32d24-115">Valeur [LockTypeEnum](locktypeenum.md) contenant le type de verrouillage de l'objet **Recordset** qui sera ouvert.</span><span class="sxs-lookup"><span data-stu-id="32d24-115">A [LockTypeEnum](locktypeenum.md) that contains the lock type for the **Recordset** that will be opened.</span></span> <span data-ttu-id="32d24-116">Ce paramètre permet de changer le type de verrouillage pendant l'exécution d'une opération **Open** sur un objet **Recordset** ).</span><span class="sxs-lookup"><span data-stu-id="32d24-116">With this parameter, you can change the lock to any type during a **Recordset** **Open** operation.</span></span> <span data-ttu-id="32d24-117">*LockType* est ignorée pour tout autre opération.</span><span class="sxs-lookup"><span data-stu-id="32d24-117">*LockType* will be ignored for any other operation.</span></span>

  - <span data-ttu-id="32d24-118">*Options*</span><span class="sxs-lookup"><span data-stu-id="32d24-118">*Options*</span></span>

  - <span data-ttu-id="32d24-119">Valeur de type **Long** indiquant les options qui peuvent être utilisées pour exécuter la commande ou ouvrir l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="32d24-119">A **Long** value that indicates options that can be used to execute the command or open the **Recordset**.</span></span>

  - <span data-ttu-id="32d24-120">*adStatus*</span><span class="sxs-lookup"><span data-stu-id="32d24-120">*adStatus*</span></span>

  - [<span data-ttu-id="32d24-121">EventStatusEnum</span><span class="sxs-lookup"><span data-stu-id="32d24-121">EventStatusEnum</span></span>](eventstatusenum.md)
    
    <span data-ttu-id="32d24-122">Avant que cet événement soit retourné, définissez ce paramètre à **adStatusUnwantedEvent** pour éviter toute notification ultérieure ou à **adStatusCancel** pour demander l'annulation de l'opération à l'origine de l'événement.</span><span class="sxs-lookup"><span data-stu-id="32d24-122">Before this event returns, set this parameter to **adStatusUnwantedEvent** to prevent subsequent notifications, or **adStatusCancel** to request cancellation of the operation that caused this event.</span></span>

  - <span data-ttu-id="32d24-123">*pCommand*</span><span class="sxs-lookup"><span data-stu-id="32d24-123">*pCommand*</span></span>

  - <span data-ttu-id="32d24-124">Objet [Command](command-object-ado.md) auquel cette notification d'événement s'applique.</span><span class="sxs-lookup"><span data-stu-id="32d24-124">The [Command](command-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="32d24-125">*Connection*</span><span class="sxs-lookup"><span data-stu-id="32d24-125">*pRecordset*</span></span>

  - <span data-ttu-id="32d24-126">Objet [Recordset](recordset-object-ado.md) auquel cette notification d'événement s'applique.</span><span class="sxs-lookup"><span data-stu-id="32d24-126">The [Recordset](recordset-object-ado.md) object for which this event notification applies.</span></span>

  - <span data-ttu-id="32d24-127">*pConnection*</span><span class="sxs-lookup"><span data-stu-id="32d24-127">*pConnection*</span></span>

  - <span data-ttu-id="32d24-128">Objet [Connection](connection-object-ado.md) auquel cette notification d'événement s'applique.</span><span class="sxs-lookup"><span data-stu-id="32d24-128">The [Connection](connection-object-ado.md) object for which this event notification applies.</span></span>

## <a name="remarks"></a><span data-ttu-id="32d24-129">Notes</span><span class="sxs-lookup"><span data-stu-id="32d24-129">Remarks</span></span>

<span data-ttu-id="32d24-130">Un événement **WillExecute** peut se produire suite à une **connexion.** [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **commande.** [Exécuter](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), ou **Recordset.** La méthode [Open](open-method-ado-recordset.md) le paramètre *pConnection* doit toujours contenir une référence valide à un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="32d24-130">A **WillExecute** event may occur due to a **Connection.**[Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)), **Command.**[Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)), or **Recordset.**[Open](open-method-ado-recordset.md) method The *pConnection* parameter should always contain a valid reference to a **Connection** object.</span></span> <span data-ttu-id="32d24-131">Si l’événement est en raison de **Connection.Execute**, les paramètres *pRecordset* et *pCommand* sont définies sur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="32d24-131">If the event is due to **Connection.Execute**, the *pRecordset* and *pCommand* parameters are set to **Nothing**.</span></span> <span data-ttu-id="32d24-132">Si l’événement est en raison de la **méthode Recordset.Open**, le paramètre *Connection* référence à l’objet **Recordset** et le paramètre *pCommand* est défini sur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="32d24-132">If the event is due to **Recordset.Open**, the *pRecordset* parameter will reference the **Recordset** object and the *pCommand* parameter is set to **Nothing**.</span></span> <span data-ttu-id="32d24-133">Si l’événement est en raison de **Command.Execute**, le paramètre *pCommand fait* référence à l’objet **Command** et le paramètre *Connection* est défini sur **Nothing**.</span><span class="sxs-lookup"><span data-stu-id="32d24-133">If the event is due to **Command.Execute**, the *pCommand* parameter will reference the **Command** object and the *pRecordset* parameter is set to **Nothing**.</span></span>

<span data-ttu-id="32d24-p104">**WillExecute** permet de passer en revue et de modifier les paramètres d'exécution en attente. Il se peut que cet événement retourne une demande d'annulation de la commande en attente.</span><span class="sxs-lookup"><span data-stu-id="32d24-p104">**WillExecute** allows you to examine and modify the pending execution parameters. This event may return a request that the pending command be canceled.</span></span>

