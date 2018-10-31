---
title: BeginTrans, CommitTrans et RollbackTrans, méthodes (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 719c495e18fb769a2d3f994542ab8d9e93a469f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860377"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="02b42-102">BeginTrans, CommitTrans et RollbackTrans, méthodes (ADO)</span><span class="sxs-lookup"><span data-stu-id="02b42-102">BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)</span></span>


<span data-ttu-id="02b42-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="02b42-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="02b42-104">Ces méthodes de transaction gèrent le traitement des transactions dans un objet [Connection](connection-object-ado.md) de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="02b42-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

  - <span data-ttu-id="02b42-105">**BeginTrans**: lance une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-105">**BeginTrans** — Begins a new transaction.</span></span>

  - <span data-ttu-id="02b42-p101">**CommitTrans**: enregistre les modifications apportées et termine la transaction active. Lance aussi parfois une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

  - <span data-ttu-id="02b42-p102">**RollbackTrans**: annule les modifications apportées pendant la transaction active et termine celle-ci. Lance aussi parfois une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="02b42-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02b42-110">Syntax</span></span>

<span data-ttu-id="02b42-111">*niveau* = *objet*. BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="02b42-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="02b42-112">*objet*. BeginTrans</span><span class="sxs-lookup"><span data-stu-id="02b42-112">*object*.BeginTrans</span></span>

<span data-ttu-id="02b42-113">*objet*. CommitTrans</span><span class="sxs-lookup"><span data-stu-id="02b42-113">*object*.CommitTrans</span></span>

<span data-ttu-id="02b42-114">*objet*. RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="02b42-114">*object*.RollbackTrans</span></span>

<span data-ttu-id="02b42-115"><<<<<<< EN-TÊTE</span><span class="sxs-lookup"><span data-stu-id="02b42-115"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="02b42-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02b42-116">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="02b42-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="02b42-117">Return value</span></span>
>>>>>>> <span data-ttu-id="02b42-118">master</span><span class="sxs-lookup"><span data-stu-id="02b42-118">master</span></span>

<span data-ttu-id="02b42-119">**BeginTrans** peut être appelée en tant que fonction qui retourne une variable de type **Long** indiquant le niveau d'imbrication de la transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-119">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="02b42-120">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02b42-120">Parameters</span></span>

  - <span data-ttu-id="02b42-121">*object*</span><span class="sxs-lookup"><span data-stu-id="02b42-121">*object*</span></span>

  - <span data-ttu-id="02b42-122">Objet **Connection**.</span><span class="sxs-lookup"><span data-stu-id="02b42-122">A **Connection** object.</span></span>

<span data-ttu-id="02b42-123">**Connection**</span><span class="sxs-lookup"><span data-stu-id="02b42-123">**Connection**</span></span>

<span data-ttu-id="02b42-p103">Utilisez ces méthodes avec un objet **Connection** lorsque vous voulez enregistrer ou annuler en bloc une série de modifications apportées aux données source. Par exemple, pour transférer de l'argent entre des comptes, vous soustrayez le montant transféré d'un compte et vous ajoutez ce même montant à l'autre compte. Si l'opération échoue d'un côté, les comptes ne seront plus équilibrés. Lorsque vous effectuez des modifications de ce type dans une transaction ouverte, vous êtes assuré que toutes les modifications ou aucune d'elles sont validées.</span><span class="sxs-lookup"><span data-stu-id="02b42-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <span data-ttu-id="02b42-p104">Tous les fournisseurs ne prennent pas en charge les transactions. Vérifiez que la propriété « **Transaction DDL** », définie par le fournisseur, apparaît dans la collection [Properties](properties-collection-ado.md) de l’objet **Connection** ; elle indique que le fournisseur prend en charge les transactions. Si ce n’est pas le cas, l’appel de l’une de ces méthodes retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="02b42-p104">Not all providers support transactions. Verify that the provider-defined property "**Transaction DDL**" appears in the **Connection** object's [Properties](properties-collection-ado.md) collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span>

<span data-ttu-id="02b42-131">Une fois que vous appelez la méthode **BeginTrans**, le fournisseur ne valide plus instantanément les modifications que vous apportez jusqu'à ce que vous appeliez **CommitTrans** ou **RollbackTrans** pour mettre fin à la transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-131">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="02b42-p105">Pour les fournisseurs qui prennent en charge les transactions imbriquées, l'appel de la méthode **BeginTrans** dans une transaction ouverte lance une nouvelle transaction imbriquée. La valeur de retour indique le niveau d'imbrication ; ainsi, la valeur 1 indique que vous avez ouvert une transaction de niveau supérieur (la transaction n'est pas imbriquée dans une autre), la valeur 2 que vous avez ouvert une transaction de deuxième niveau (une transaction imbriquée dans une transaction de niveau supérieur), etc. L'appel de la méthode **CommitTrans** ou **RollbackTrans** n'affecte que les dernières transactions ouvertes ; vous devez fermer ou annuler la transaction active pour pouvoir résoudre des transactions de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="02b42-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="02b42-p106">L'appel de la méthode **CommitTrans** enregistre les modifications apportées dans une transaction ouverte sur la connexion et clôture la transaction. La méthode **RollbackTrans**, quant à elle, annule les modifications apportées dans une transaction ouverte et met fin à la transaction. Si aucune transaction n'est ouverte, l'appel de ces méthodes génère une erreur.</span><span class="sxs-lookup"><span data-stu-id="02b42-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="02b42-138">En fonction de la propriété [Attributes](attributes-property-ado.md) de l’objet **Connection** , l’appel de la méthode **CommitTrans** ou **RollbackTrans** peut démarrer automatiquement une nouvelle transaction.</span><span class="sxs-lookup"><span data-stu-id="02b42-138">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction.</span></span> <span data-ttu-id="02b42-139">Si la propriété **Attributes** a la valeur **adXactCommitRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **CommitTrans**.</span><span class="sxs-lookup"><span data-stu-id="02b42-139">If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call.</span></span> <span data-ttu-id="02b42-140">Si la propriété **Attributes** a la valeur **adXactAbortRetaining**, le fournisseur lance automatiquement une nouvelle transaction après un appel à **RollbackTrans**.</span><span class="sxs-lookup"><span data-stu-id="02b42-140">If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

<span data-ttu-id="02b42-141">**RDS (Remote Data Service)**</span><span class="sxs-lookup"><span data-stu-id="02b42-141">**Remote Data Service**</span></span>

<span data-ttu-id="02b42-142">Les méthodes **BeginTrans**, **CommitTrans** et **RollbackTrans** ne sont pas disponibles sur un objet **Connection** côté client.</span><span class="sxs-lookup"><span data-stu-id="02b42-142">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>

