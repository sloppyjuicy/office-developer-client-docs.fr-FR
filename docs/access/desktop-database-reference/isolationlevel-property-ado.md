---
title: IsolationLevel, propriété (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4eb46fa97b831030617916d03557b5bf9af9606d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291148"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="c670b-102">IsolationLevel, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="c670b-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="c670b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c670b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c670b-104">Indique le niveau d'isolation d'un objet [Connection](connection-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c670b-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="c670b-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c670b-105">Settings and return values</span></span>

<span data-ttu-id="c670b-106">Définit ou renvoie une valeur [IsolationLevelEnum](isolationlevelenum.md).</span><span class="sxs-lookup"><span data-stu-id="c670b-106">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value.</span></span> <span data-ttu-id="c670b-107">La valeur par défaut est **adXactChaos**.</span><span class="sxs-lookup"><span data-stu-id="c670b-107">The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c670b-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="c670b-108">Remarks</span></span>

<span data-ttu-id="c670b-p102">Utilisez la propriété **IsolationLevel** pour définir le niveau d'isolation d'un objet **Connection**. Le paramètre ne prend effet qu'à l'appel suivant de la méthode [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md). Si le niveau d'isolation que vous demandez n'est pas disponible, le fournisseur peut renvoyer le meilleur niveau d'isolation suivant.</span><span class="sxs-lookup"><span data-stu-id="c670b-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="c670b-112">La propriété **IsolationLevel** est en accessible lecture et en écriture.</span><span class="sxs-lookup"><span data-stu-id="c670b-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="c670b-113">**Utilisation des services de données à distance** Lorsqu'elle est utilisée sur un objet Connection côté client, la propriété **IsolationLevel** ne peut être définie que sur **adXactUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="c670b-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="c670b-p103">Parce que les utilisateurs travaillent avec des objets **Recordset** déconnectés, stockés dans un cache client, il peut y avoir des problèmes liés à la multiplicité des utilisateurs. Par exemple lorsque deux utilisateurs différents tentent de mettre à jour le même enregistrement, Remote Data Service exécute la mise à jour de l'utilisateur dont la requête lui parvient en premier. La demande de mise à jour du second utilisateur échoue et une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="c670b-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

