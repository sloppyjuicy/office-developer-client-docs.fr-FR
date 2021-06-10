---
title: Types de verrous (référence de base de données de bureau Access)
TOCTitle: Types of Locks
ms:assetid: 8276edca-f603-2487-a2ca-73e618c0f11e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249565(v=office.15)
ms:contentKeyID: 48545978
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47b212be1922f783889f1e5be436a616909dc5c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314160"
---
# <a name="types-of-locks"></a><span data-ttu-id="64b3f-102">Types de verrous</span><span class="sxs-lookup"><span data-stu-id="64b3f-102">Types of locks</span></span>


<span data-ttu-id="64b3f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64b3f-103">**Applies to**: Access 2013, Office 2013</span></span>



## <a name="adlockbatchoptimistic"></a><span data-ttu-id="64b3f-104">adLockBatchOptimistic</span><span class="sxs-lookup"><span data-stu-id="64b3f-104">adLockBatchOptimistic</span></span>

<span data-ttu-id="64b3f-p101">Indique des mises à jour par lot optimistes. Requis pour le mode de mise à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="64b3f-p101">Indicates optimistic batch updates. Required for batch update mode.</span></span>

<span data-ttu-id="64b3f-p102">Un grand nombre d'applications extraient simultanément une série de lignes puis doivent effectuer des mises à jour coordonnées (insertions, mises à jour ou suppressions) de tout le groupe de lignes. Les curseurs par lot permettent un seul accès (aller-retour) au serveur, ce qui améliore les performances de mise à jour et diminue le trafic réseau. Si vous utilisez une bibliothèque de curseurs par lot, vous pouvez créer un curseur statique, puis le déconnecter de la source de données. À ce stade, vous pouvez alors apporter les modifications appropriées aux lignes puis vous reconnecter et publier les modifications par lot dans la source de données.</span><span class="sxs-lookup"><span data-stu-id="64b3f-p102">Many applications fetch a number of rows at once and then need to make coordinated updates that include the entire set of rows to be inserted, updated, or deleted. With batch cursors, only one round trip to the server is needed, thus improving update performance and decreasing network traffic. Using a batch cursor library, you can create a static cursor and then disconnect from the data source. At this point you can make changes to the rows and subsequently reconnect and post the changes to the data source in a batch.</span></span>

## <a name="adlockoptimistic"></a><span data-ttu-id="64b3f-111">adLockOptimistic</span><span class="sxs-lookup"><span data-stu-id="64b3f-111">adLockOptimistic</span></span>

<span data-ttu-id="64b3f-p103">Indique que le fournisseur utilise le verrouillage optimiste . En d'autres termes, les enregistrements ne sont verrouillés qu'en cas d'appel de la méthode **Update**. Cela dit, il est toujours possible qu'un autre utilisateur ait modifié les données entre la modification de l'enregistrement et l'appel de la méthode **Update**, ce qui engendre des conflits. Il est donc préférable d'utiliser ce type de verrou uniquement dans les cas où les risques de collision sont réduits, ou si vous estimez que ces conflits peuvent être facilement résolus.</span><span class="sxs-lookup"><span data-stu-id="64b3f-p103">Indicates that the provider uses optimistic locking — locking records only when you call the **Update** method. This means that there is a chance that the data may be changed by another user between the time you edit the record and when you call **Update**, which creates conflicts. Use this lock type in situations where the chances of a collision are low or where collisions can be readily resolved.</span></span>

## <a name="adlockpessimistic"></a><span data-ttu-id="64b3f-115">adLockPessimistic</span><span class="sxs-lookup"><span data-stu-id="64b3f-115">adLockPessimistic</span></span>

<span data-ttu-id="64b3f-p104">Indique un verrouillage pessimiste, enregistrement par enregistrement. Le fournisseur effectue les opérations nécessaires à une modification sécurisée des enregistrements. En règle générale, les enregistrements sont verrouillés dans la source de données, immédiatement avant leur modification. Bien entendu, cela signifie que les enregistrements ne sont plus accessibles aux autres utilisateurs une fois la procédure de modification entamée, et qu'elles ne le seront qu'une fois déverrouillées, par l'appel de la méthode **Update.** Il est conseillé d'utiliser ce type de verrou dans un système dont les données ne peuvent faire l'objet de modifications concomitantes, comme un système de réservation, par exemple.</span><span class="sxs-lookup"><span data-stu-id="64b3f-p104">Indicates pessimistic locking, record by record. The provider does what is necessary to ensure successful editing of the records, usually by locking records at the data source immediately before editing. Of course, this means that the records are unavailable to other users once you begin to edit, until you release the lock by calling **Update.** Use this type of lock in a system where you cannot afford to have concurrent changes to data, such as in a reservation system.</span></span>

## <a name="adlockreadonly"></a><span data-ttu-id="64b3f-120">adLockReadOnly</span><span class="sxs-lookup"><span data-stu-id="64b3f-120">adLockReadOnly</span></span>

<span data-ttu-id="64b3f-p105">Indique des enregistrements en lecture seule. Vous ne pouvez pas modifier les données. Un verrou en lecture seule constitue le type de verrou le plus « rapide » car il ne requiert pas de verrouillage des enregistrements par le serveur.</span><span class="sxs-lookup"><span data-stu-id="64b3f-p105">Indicates read-only records. You cannot alter the data. A read-only lock is the "fastest" type of lock because it does not require the server to maintain a lock on the records.</span></span>

## <a name="adlockunspecified"></a><span data-ttu-id="64b3f-124">adLockUnspecified</span><span class="sxs-lookup"><span data-stu-id="64b3f-124">adLockUnspecified</span></span>

<span data-ttu-id="64b3f-125">Le type de verrou n'est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="64b3f-125">Does not specify a type of lock.</span></span>

