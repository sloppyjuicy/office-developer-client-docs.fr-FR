---
title: IsolationLevel, propriété (ADO)
TOCTitle: IsolationLevel Property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7424258f4b5a69764189f33a902956f370a56094
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470891"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="58f0d-102">IsolationLevel, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="58f0d-102">IsolationLevel Property (ADO)</span></span>


<span data-ttu-id="58f0d-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="58f0d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58f0d-104">Indique le niveau d'isolation d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="58f0d-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="58f0d-105">Paramètres et valeurs renvoyées</span><span class="sxs-lookup"><span data-stu-id="58f0d-105">Settings and Return Values</span></span>

<span data-ttu-id="58f0d-p101">Définit ou renvoie une valeur [IsolationLevelEnum](isolationlevelenum.md). La valeur par défaut est **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="58f0d-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="58f0d-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="58f0d-108">Remarks</span></span>

<span data-ttu-id="58f0d-p102">Utilisez la propriété **IsolationLevel** pour définir le niveau d'isolation d'un objet **Connection**. Le paramètre ne prend effet qu'à l'appel suivant de la méthode [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si le niveau d'isolation que vous demandez n'est pas disponible, le fournisseur peut renvoyer le meilleur niveau d'isolation suivant.</span><span class="sxs-lookup"><span data-stu-id="58f0d-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="58f0d-112">La propriété **IsolationLevel** est en accessible lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="58f0d-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="58f0d-113">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet de connexion côté client, la propriété **IsolationLevel** peut être définie uniquement aux **: adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="58f0d-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="58f0d-p103">Parce que les utilisateurs travaillent avec des objets **Recordset** déconnectés, stockés dans un cache client, il peut y avoir des problèmes liés à la multiplicité des utilisateurs. Par exemple lorsque deux utilisateurs différents tentent de mettre à jour le même enregistrement, Remote Data Service exécute la mise à jour de l'utilisateur dont la requête lui parvient en premier. La demande de mise à jour du second utilisateur échoue et une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="58f0d-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

